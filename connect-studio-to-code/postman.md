# Postman

**Prerequisites**:

* [api-keys.md](../settings/api-keys.md "mention")

### **Using Postman to Call the API**

1. **Set Up a Request:**
   * Create a new **POST request** in Postman.
   * Use the same endpoint as Apollo Sandbox.

<figure><img src="../.gitbook/assets/CleanShot 2025-03-28 at 15.01.58@2x.png" alt=""><figcaption></figcaption></figure>

2. **Add Authorization:**

* In the **Authorization** tab, select **Bearer Token**.
* Paste your API key into the token field.

<figure><img src="../.gitbook/assets/CleanShot 2025-03-28 at 15.02.45@2x.png" alt=""><figcaption></figcaption></figure>

3. **Check the Headers:**

* The headers will show  a predefined Authorisation.

<figure><img src="../.gitbook/assets/CleanShot 2025-03-28 at 15.03.22@2x.png" alt=""><figcaption></figcaption></figure>

4. **Define the Body:**

* Go to the Body tab. Select the "raw" option. In the input enter the "operationName" and "variables" as we have defined in the [Apollo Sandbox](postman.md#using-the-api-key-with-graphql).

<figure><img src="../.gitbook/assets/CleanShot 2025-03-31 at 14.30.23@2x.png" alt=""><figcaption></figcaption></figure>

* Use the "query" in the "Operation" section of Apollo Sandbox and convert it into a single-line string. You can use this [tool](https://multi-to-single-string.netlify.app/) to convert the query from multi-line to single-line.

<figure><img src="../.gitbook/assets/CleanShot 2025-03-31 at 14.20.05@2x.png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../.gitbook/assets/CleanShot 2025-03-31 at 14.13.33@2x.png" alt=""><figcaption></figcaption></figure>

5. **Send the Request:**

* Execute the request by clicking on "Send" to receive JSON responses similar to the Apollo Sandbox.

<figure><img src="../.gitbook/assets/CleanShot 2025-03-31 at 14.13.33@2x (1).png" alt=""><figcaption></figcaption></figure>
