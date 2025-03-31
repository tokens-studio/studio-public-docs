# Connect Studio to Code

### **Using the Studio CLI and API**

This documentation provides a detailed guide on how to use the Studio CLI and API for managing design tokens efficiently.

### **Accessing the SDK and CLI Documentation**

1.  **Navigate to Studio:**

    * Open the Studio application.
    * Go to your **organization dashboard**.
    * Click the **SDK and CLI** button.

    <figure><img src=".gitbook/assets/CleanShot 2025-02-17 at 12.35.31.png" alt=""><figcaption></figcaption></figure>
2. **Review the SDK Documentation:**
   * This [page](https://tokens-studio.github.io/studio-app/) contains the **Studio Software Development Kit (SDK)** and CLI instructions.
   * It might seem overwhelming, but the focus is on pulling your tokens into your local file system via the CLI.
3. **Creating an API Key**
   * **Generate a Key:**
     * Go to **Personal Settings** in Studio.
       * Select **API Keys** (below "Edit Profile").
       * Create a new API key (e.g., "Test Key").
   * **Copy and Store the Key:**
     * Copy the key string and **store it securely** (e.g., in a password manager or vault).
       * You won’t be able to view the key again after closing the window.

<figure><img src=".gitbook/assets/CleanShot 2025-02-17 at 12.52.32.png" alt=""><figcaption></figcaption></figure>

### **Using the API Key with GraphQL**

The API operates on a **GraphQL interface**. You can use tools like **Postman**, **Curl**, or the **Apollo Sandbox** to interact with it.

1. **Access the Apollo Sandbox:**
   * Open the **GraphQL endpoint** [**https://graphql.app.tokens.studio/graphql**](https://graphql.app.tokens.studio/graphql)

<figure><img src=".gitbook/assets/CleanShot 2025-03-27 at 23.29.43@2x.png" alt=""><figcaption></figcaption></figure>

2. **Configuring the Authorization Header:**

* In Apollo Sandbox:
  * Navigate to **Settings > Connection Settings**.

<figure><img src=".gitbook/assets/CleanShot 2025-03-27 at 23.30.17@2x.png" alt=""><figcaption></figcaption></figure>

* Click on Edit on the Connection settings. A modal will open.

<figure><img src=".gitbook/assets/CleanShot 2025-03-27 at 23.32.33@2x.png" alt=""><figcaption></figcaption></figure>

* In the Shared headers section, select "Authorization header" in the header key input. In the value input: `Bearer <API_KEY>` (replace `<API_KEY>` with your API key). Click Save.

<figure><img src=".gitbook/assets/CleanShot 2025-03-27 at 23.33.13@2x.png" alt=""><figcaption></figcaption></figure>

3. **View the available queries:**

* The query section will show the available queries as can be seen in the [SDK-CLI documentation > Query page](https://tokens-studio.github.io/studio-app/types/Query.html).

<figure><img src=".gitbook/assets/CleanShot 2025-03-27 at 23.34.36@2x.png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/CleanShot 2025-03-27 at 23.34.14@2x.png" alt=""><figcaption></figcaption></figure>

4. **Run a Query:**

* Use the query editor in Apollo Sandbox to explore data (e.g., list all projects).&#x20;

**Example query - List of all projects in an Organization:**

* Click on "projects(...): PaginatedProjects!". The details will be filled in the Operation and Variables section.

<figure><img src=".gitbook/assets/CleanShot 2025-03-28 at 00.04.12@2x (1).png" alt=""><figcaption></figcaption></figure>

* Add "data: \[Project!]!. This step is done because the Projects list is a paginated response.

<figure><img src=".gitbook/assets/CleanShot 2025-03-28 at 00.04.56@2x.png" alt=""><figcaption></figcaption></figure>

* Add "name" to get the name of the project and "oragnizationId" to specify the organisation.&#x20;

<figure><img src=".gitbook/assets/CleanShot 2025-03-28 at 00.05.33@2x.png" alt=""><figcaption></figcaption></figure>

A query would be generated in the Operations panel.

```graphql
query Projects($organization: String!) {
  projects(organization: $organization) {
    data {
      organizationId
      name
    }
  }
}
```

* In the "**Variables**" section, we need to add the organisation id. To get the organisation ID, Navigate to your organization in Studio. Copy the **Organization ID** from the URL (after `/org/`).

<figure><img src=".gitbook/assets/CleanShot 2025-03-28 at 00.06.14@2x.png" alt=""><figcaption></figcaption></figure>

* Return to the Apollo Sandbox, enter the organisation id in the "**Variables section**".

```json
{
  "organization": "<org-ID>"
}
```

<figure><img src=".gitbook/assets/CleanShot 2025-03-28 at 00.07.06@2x.png" alt=""><figcaption></figcaption></figure>

* Run the query, the list of projects with the project name and the organisation id will be displayed in the right panel.

<figure><img src=".gitbook/assets/CleanShot 2025-03-28 at 00.07.30@2x.png" alt=""><figcaption></figcaption></figure>

### **Using Postman to Call the API**

1. **Set Up a Request:**
   * Create a new **POST request** in Postman.
   * Use the same endpoint as Apollo Sandbox.

<figure><img src=".gitbook/assets/CleanShot 2025-03-28 at 15.01.58@2x.png" alt=""><figcaption></figcaption></figure>

2. **Add Authorization:**

* In the **Authorization** tab, select **Bearer Token**.
* Paste your API key into the token field.

<figure><img src=".gitbook/assets/CleanShot 2025-03-28 at 15.02.45@2x.png" alt=""><figcaption></figcaption></figure>

3. **Check the Headers:**

* The headers will show  a predefined Authorisation.

<figure><img src=".gitbook/assets/CleanShot 2025-03-28 at 15.03.22@2x.png" alt=""><figcaption></figcaption></figure>

4. **Define the Body:**

* Go to the Body tab. Select the "raw" option. In the input enter the "operationName" and "variables" as we have defined in the [Apollo Sandbox](connect-studio-to-code.md#using-the-api-key-with-graphql).

<figure><img src=".gitbook/assets/CleanShot 2025-03-31 at 14.30.23@2x.png" alt=""><figcaption></figcaption></figure>

* Use the "query" in the "Operation" section of Apollo Sandbox and convert it into a single-line string. You can use this [tool](https://multi-to-single-string.netlify.app/) to convert the query from multi-line to single-line.

<figure><img src=".gitbook/assets/CleanShot 2025-03-31 at 14.20.05@2x.png" alt=""><figcaption></figcaption></figure>

The single line query will look like this:

```json
query Projects($organization: String!) {\n  projects(organization: $organization) {\n    data {\n      organizationId\n      name\n    }\n  }\n}
```

* Provide necessary variables (e.g., `organization ID`) in the payload. The final query will look something like this:

```json
{
    "operationName": "Projects",
    "variables": {
        "organization": "<Org-ID>"
    },
    "query": "query Projects($organization: String!) {\n  projects(organization: $organization) {\n    data {\n      organizationId\n      name\n    }\n  }\n}"
}
```

<figure><img src=".gitbook/assets/CleanShot 2025-03-31 at 14.13.33@2x.png" alt=""><figcaption></figcaption></figure>

5. **Send the Request:**

* Execute the request by clicking on "Send" to receive JSON responses similar to the Apollo Sandbox.

<figure><img src=".gitbook/assets/CleanShot 2025-03-31 at 14.13.33@2x (1).png" alt=""><figcaption></figcaption></figure>

### **Using the Token Studio CLI**

1.  **Install the CLI:**

    * Open the project that you want to connect Studio with.
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

    *   Enter your API key when prompted. You can skip this step by Automating the CLI.

        ```bash
        Tokens Studio CLI  2.0.2

        You did not pass an API key in the environment variables, but you can paste one here.
              You can create an API key in Studio user settings by navigating to a project dashboard 
              and clicking the bottom left menu -> API keys.

                       API key: 
        ```
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

        The selected settings will be saved in the `.tokensstudio.json` config file.

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
4.  **Pull Tokens:**

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
5.  **Automate the CLI:**

    * Pass the API key as an environment variable for automation. This will ensure that the API key is not prompted for everytime.

    ```bash
    TOKENSSTUDIO_APIKEY=<API_KEY> npx tokensstudio pull
    ```

### **Key Features of the CLI**

1. **Current Features:**
   * Pull token sets into local files.
   * Simplify organization and project selection.
2. **Planned Features:**
   * **Watch Mode:** Automatically sync changes from Studio to local files.
   * **Release Artifacts:** Pull releases directly instead of token sets.

### **Best Practices**

1. **Secure API Key Storage:**
   * Use a password manager or secure vault.
   * Avoid storing keys in plain text.
2. **Automation:**
   * Use environment variables to prevent manual prompts in CI pipelines.
3. **Explore API Schema:**
   * Use Apollo Sandbox for schema introspection before creating complex queries.

This documentation provides an overview of using Studio’s API and CLI effectively. For further assistance, refer to the official [SDK and CLI documentation page](https://tokens-studio.github.io/studio-app/).
