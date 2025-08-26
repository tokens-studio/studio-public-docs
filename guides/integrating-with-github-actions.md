---
description: >-
  Pull tokens directly from Tokens Studio into your Github Actions to compliment
  your build pipeline.
---

# Integrating with Github Actions

Github Actions provides tooling to create workflows for bundling assets, running tests, building for production and more. Tokens Studio fits in well with that process, allowing teams to pull the latest tokens directly from Tokens Studio into your projects.

#### Prerequisites

* [api-keys.md](../settings/api-keys.md "mention")
* [tokens-studio-cli.md](../connect-studio-to-code/tokens-studio-cli.md "mention")
* Working knowledge of Github and Git

## Example Workflow

Let's walk through a basic example of setting up a Github Action that will pull the latest updates from Tokens Studio using the [Tokens Studio CLI](../connect-studio-to-code/tokens-studio-cli.md).

{% stepper %}
{% step %}
### Get your API Key&#x20;

Create a new API Key in Tokens Studio. You can follow our guide to creating one - [#creating-a-new-api-key](../settings/api-keys.md#creating-a-new-api-key "mention"). Be sure to keep it safe and close by as we will need it.
{% endstep %}

{% step %}
### Save the API Key to your Github repo

<figure><img src="../.gitbook/assets/2025-07-30 at 12.59.26 - Screengrab@2x.png" alt=""><figcaption></figcaption></figure>

Inside the Github repository that contains your code, click the **Settings tab** in the top bar.&#x20;

Next, expand the **Secrets and variables** option in the sidebar to view **Actions**

{% hint style="warning" %}
**Don't see these options?**&#x20;

You may need to get permissions adjusted from the Github admin within your organization.
{% endhint %}

Click the **New repository secret** button to open the form to add your token.&#x20;

<figure><img src="../.gitbook/assets/2025-07-30 at 13.04.07 - Screengrab@2x.png" alt=""><figcaption></figcaption></figure>

In the form, add a **name** of `TOKENS_STUDIO_API_KEY` and paste the API token you created in the **Secret** field. Click **Add secret** to save it.
{% endstep %}

{% step %}
### Install the Tokens Studio CLI  to your project

In your project, install the Tokens Studio SDK package from NPM using your package manager of choice.&#x20;

```bash
npm install @tokens-studio/sdk
```

You can see the full instructions here - [#installing-the-cli](../connect-studio-to-code/tokens-studio-cli.md#installing-the-cli "mention")
{% endstep %}

{% step %}
### Set up your project with Tokens Studio

Once installed, you will need to configure the SDK to work with your account.

In your terminal run `npx @tokens-studio/sdk setup`

You will be asked to enter the API Token you created above and will have the ability to configure the organization you'd like to pull from. Once completed, there will be a `.tokensstudio.json` file created. Be sure to include this when you push your updates to Github.

You can find full instructions on how to set this up at [#using-the-cli](../connect-studio-to-code/tokens-studio-cli.md#using-the-cli "mention").
{% endstep %}

{% step %}
### Create an Node script to run the SDK&#x20;

Since we're going to be asking Github's tooling to run scripts on our behalf, we need to set up a script in our package.json that Github can run.

This may be unique depending on your project needs, but for this example, we'll just pull tokens into our project.&#x20;

In your package.json file, add a task to your `scripts` object named `tokens:sync`

```
{
    ...,
    "scripts": {
        ...,
        "tokens:sync": "npx @tokens-studio/sdk pull"
    },
    ...
}
```

{% hint style="info" %}
You can name the task whatever you'd like of course, we're just fans of declarative naming.
{% endhint %}
{% endstep %}

{% step %}
### Set up your Github action

At the root of your project, create a folder named `.github` with a subfolder named `workflows`

Create a file named `pull-tokens.yml` and include the contents below in it.

You'll notice that step 4 asks for a TOKENS\_STUDIO\_API\_KEY. This will use the key we saved in Github earlier.

{% hint style="info" %}
This is an example of course. You may need to use different versions of Node or change the process as needed. You can read more about Github Actions in their documentation - [https://docs.github.com/en/actions](https://docs.github.com/en/actions)
{% endhint %}

```
# .github/workflows/pull-tokens.yml

name: "Sync & Build Design Tokens"

on:
  workflow_dispatch:

jobs:
  sync-and-build-tokens:
    runs-on: ubuntu-latest
    permissions:
      contents: write
      pull-requests: write

    steps:
      # 1. Check out the repository code
      - name: Checkout repository
        uses: actions/checkout@v4

      # 2. Set up Node.js
      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: "22"
          cache: "npm"

      # 3. Install project dependencies
      - name: Install dependencies
        run: npm install

      # 4. Run the complete token sync process
      - name: Sync, Build, and Format Tokens
        run: npm run tokens:pull
        env:
          TOKENS_STUDIO_API_KEY: ${{ secrets.TOKENS_STUDIO_API_KEY }}

      # 5. Commit files and create PR
      - name: Commit and Create PR
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        run: |
          git config user.name "github-actions[bot]"
          git config user.email "github-actions[bot]@users.noreply.github.com"

          if ! git diff --quiet; then
            echo "Changes detected. Creating a new branch and PR."
            
            BRANCH_NAME="tokens/update-$(date +%s)"
            git checkout -b $BRANCH_NAME
            
            git add .
            git commit -m "chore(tokens): Sync and build design tokens"
            git push -u origin $BRANCH_NAME
            
            gh pr create \
              --title "🎨 Sync & Build Design Tokens" \
              --body "This PR was automatically generated and contains the latest token updates from Tokens Studio." \
              --base ${{ github.ref_name }} \
              --head $BRANCH_NAME
          else
            echo "No changes to commit."
          fi 
```
{% endstep %}

{% step %}
### Commit and Push your changes to Github

Once everything is completed locally, be sure to add these files to git, commit and push.
{% endstep %}
{% endstepper %}

