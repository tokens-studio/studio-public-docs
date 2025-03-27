# Connect Studio to Code

**Using the Studio CLI and API**

This documentation provides a detailed guide on how to use the Studio CLI and API for managing design tokens efficiently.

{% stepper %}
{% step %}
#### **Accessing the SDK and CLI Documentation**

1.  **Navigate to Studio:**

    * Open the Studio application.
    * Go to your **organization dashboard**.
    * Click the **SDK and CLI** button.

    <figure><img src=".gitbook/assets/CleanShot 2025-02-17 at 12.35.31.png" alt=""><figcaption></figcaption></figure>
2. **Review the SDK Documentation:**
   * This [page](https://tokens-studio.github.io/studio-app/) contains the **Studio Software Development Kit (SDK)** and CLI instructions.
   * It might seem overwhelming, but the focus is on pulling your tokens into your local file system via the CLI.
{% endstep %}

{% step %}
#### **Creating an API Key**

1. **Generate a Key:**
   * Go to **Personal Settings** in Studio.
   * Select **API Keys** (below "Edit Profile").
   * Create a new API key (e.g., "Test Key").
2. **Copy and Store the Key:**
   * Copy the key string and **store it securely** (e.g., in a password manager or vault).
   * You won’t be able to view the key again after closing the window.

<figure><img src=".gitbook/assets/CleanShot 2025-02-17 at 12.52.32.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### **Using the API Key with GraphQL**

1. **Understanding GraphQL:**
   * The API operates on a **GraphQL interface**.
   * You can use tools like **Postman**, **Curl**, or the **Apollo Sandbox** to interact with it.
2. **Access the Apollo Sandbox:**
   * Open the **GraphQL endpoint**.
   * Use Apollo Sandbox to explore the API schema.
3. **Configuring the Authorization Header:**
   * In Apollo Sandbox:
     * Navigate to **Settings > Connection Settings**.
     * Add an authorization header: `Bearer <API_KEY>` (replace `<API_KEY>` with your API key).
4. **Run a Query:**
   * Use the query editor in Apollo Sandbox to explore data (e.g., list all projects).
   * Add required fields like `name` and `organization ID`.
5. **Get Organization ID:**
   * Navigate to your organization in Studio.
   * Copy the **Organization ID** from the URL (after `/org/`).
{% endstep %}

{% step %}
#### **Using Postman to Call the API**

1. **Set Up a Request:**
   * Create a new **POST request** in Postman.
   * Use the same endpoint as Apollo Sandbox.
2. **Add Authorization:**
   * In the **Authorization** tab, select **Bearer Token**.
   * Paste your API key into the token field.
3. **Define the Body:**
   * Use the query from Apollo Sandbox and convert it into a single-line string.
   * Provide necessary variables (e.g., `organization ID`) in the payload.
4. **Send the Request:**
   * Execute the request to receive JSON responses similar to the Apollo Sandbox.
{% endstep %}

{% step %}
#### **Using the Token Studio CLI**

1.  **Install the CLI:**

    * Run `npm install @tokens-studio/sdk`.
    * If you don’t have a `package.json`, initialize it first with `npm init`.
    * Ensure that the node.js version installed is v.22 or above.

    ```bash
    npm install @tokens-studio/sdk
    ```
2.  **Run the CLI:**

    Use the `--help` flag to view available commands:

    ```bash
    npx tokensstudio --help
    ```

    **This will list all the available options**

    ```bash
    Tokens Studio CLI  2.0.2

    Usage:
    $ tokensstudio 
       
    Commands: 
    pull
    setup

    For more info, run any command with the `--help` flag:
    $ tokensstudio --help
    $ tokensstudio pull --help
    $ tokensstudio setup --help 

    Options:
    --help       [boolean] Shows an overview of CLI usage
    --version    [boolean] Prints NPM version of the CLI
    ```
3.  **Set Up the CLI:**

    * Run the `setup` command:

    ```bash
    npx tokensstudio setup
    ```

    * Enter your API key when prompted. You can skip this step by Automating the CLI.

{% code overflow="wrap" %}
```bash
  Tokens Studio CLI  2.0.2

  You did not pass an API key in the environment variables, but you can paste one here.
        You can create an API key in Studio user settings by navigating to a project dashboard 
        and clicking the bottom left menu -> API keys.

                 API key: 
```
{% endcode %}

*   Select the desired **organization** and **project**.

    ```bash
    ✔  Done!
             ■ Fetched organizations
             ■ Fetched projects

    Select your organisation
    Hyma

    Select your project
    Tokens Zen Garden
    ```

    **The selected settings will be saved in the `.tokensstudio.json` config file.**

    ```json
    {
    "version": "2",
    "org": "7xxxxxx1-3xx5-4xxx-xxx6-xxxx4axxxxf2",
    "project": "xxxxfa7d-xxxx-4xxx-xxx2-xxxx0126xxxx",
    "branch": "main",
    "release": "",
    "output": "tokens"
    }
    ```



4. **Pull Tokens:**



* Specify the folder to pull tokens into (relative to the config file). This can be done in the `.tokensstudio.json` config file as `output`.
* Use the `pull` command:

```bash
npx tokensstudio pull
```

This will pull all the tokens in your project into the output specified in your config (.tokensstudio.json) file.

```bash
      ✔  Done!
         ■ Fetched tokensets

      ✔  Success Found 18 sets with 938 tokens in total.
         ◼   global.json
         ◼   semantic.json
         ◼   comp/button.json
         ◼   comp/list-item.json
         ◼   comp/menu-item.json
         ◼   comp/toggle.json
         ◼   pattern/menu-bar.json
         ◼   pattern/feature.json
         ◼   pattern/card-user.json
         ◼   pattern/card-pricing.json
         ◼   sections/nav.json
         ◼   sections/hero.json
         ◼   sections/features.json
         ◼   sections/team.json
         ◼   sections/pricing.json
         ◼   sections/footer.json
         ◼   theme/light.json
         ◼   theme/dark.json
```

* **Automate the CLI:**
* Pass the API key as an environment variable for automation. This will ensure that the API key is not prompted for everytime.

```bash
TOKENSSTUDIO_APIKEY=<API_KEY> npx tokensstudio pull
```
{% endstep %}

{% step %}
#### **Key Features of the CLI**

1. **Current Features:**
   * Pull token sets into local files.
   * Simplify organization and project selection.
2. **Planned Features:**
   * **Watch Mode:** Automatically sync changes from Studio to local files.
   * **Release Artifacts:** Pull releases directly instead of token sets.
{% endstep %}

{% step %}
#### **Best Practices**

1. **Secure API Key Storage:**
   * Use a password manager or secure vault.
   * Avoid storing keys in plain text.
2. **Automation:**
   * Use environment variables to prevent manual prompts in CI pipelines.
3. **Explore API Schema:**
   * Use Apollo Sandbox for schema introspection before creating complex queries.
{% endstep %}
{% endstepper %}

This documentation provides an overview of using Studio’s API and CLI effectively. For further assistance, refer to the official [SDK and CLI documentation page](https://tokens-studio.github.io/studio-app/).
