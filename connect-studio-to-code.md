# Connect Studio to Code

## **Using the Studio CLI and API**

This documentation provides a detailed guide on how to use the Studio CLI and API for managing design tokens efficiently.

{% stepper %}
{% step %}
### **Accessing the SDK and CLI Documentation**

1.  **Navigate to Studio:**

    * Open the Studio application.
    * Go to your **organization dashboard**.
    * Click the **SDK and CLI** button.

    <figure><img src="../.gitbook/assets/CleanShot 2025-02-17 at 12.35.31.png" alt=""><figcaption></figcaption></figure>
2. **Review the SDK Documentation:**
   * This page contains the **Studio Software Development Kit (SDK)** and CLI instructions.
   * It might seem overwhelming, but the focus is on pulling your tokens into your local file system via the CLI.
{% endstep %}

{% step %}
### **Creating an API Key**

1. **Generate a Key:**
   * Go to **Personal Settings** in Studio.
   * Select **API Keys** (below "Edit Profile").
   * Create a new API key (e.g., "Test Key").
2. **Copy and Store the Key:**
   * Copy the key string and **store it securely** (e.g., in a password manager or vault).
   * You won’t be able to view the key again after closing the window.

<figure><img src="../.gitbook/assets/CleanShot 2025-02-17 at 12.52.32.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### **Using the API Key with GraphQL**

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
### **Using Postman to Call the API**

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
### **Using the Token Studio CLI**

1. **Install the CLI:**
   * Run `npm install tokenstudio-sdk`.
   * If you don’t have a `package.json`, initialize it first with `npm init`.
2. **Run the CLI:**
   *   Use the `--help` flag to view available commands:

       ```bash
       npx tokenstudio --help
       ```
3. **Set Up the CLI:**
   *   Run the `setup` command:

       ```bash
       npx tokenstudio setup
       ```
   * Enter your API key when prompted.
   * Select the desired **organization** and **project**.
4. **Pull Tokens:**
   * Specify the folder to pull tokens into (relative to the config file).
   *   Use the `pull` command:

       ```bash
       npx tokenstudio pull
       ```
5. **Automate the CLI:**
   *   Pass the API key as an environment variable for automation:

       ```bash
       TOKENSSTUDIO_APIKEY=<API_KEY> npx tokenstudio pull
       ```
{% endstep %}

{% step %}
### **Key Features of the CLI**

1. **Current Features:**
   * Pull token sets into local files.
   * Simplify organization and project selection.
2. **Planned Features:**
   * **Watch Mode:** Automatically sync changes from Studio to local files.
   * **Release Artifacts:** Pull releases directly instead of token sets.
{% endstep %}

{% step %}
### **Best Practices**

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

