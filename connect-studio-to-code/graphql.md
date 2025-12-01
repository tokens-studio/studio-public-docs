---
description: How to access Tokens Studio data directly using GraphQL in your project.
---

# GraphQL

If you're looking to automate Tokens Studio data for build pipelines or pull it to another project or tool you're using, we offer a GraphQL endpoint that you can query directly.

**Prerequisites**:

* [api-keys.md](../settings/api-keys.md "mention")

## **Accessing the GraphQL endpoint**

{% stepper %}
{% step %}
### **Access the Apollo Sandbox:**

<figure><img src="../.gitbook/assets/CleanShot 2025-03-27 at 23.29.43@2x.png" alt=""><figcaption></figcaption></figure>

Open the **GraphQL endpoint** [**https://graphql.app.tokens.studio/graphql**](https://graphql.app.tokens.studio/graphql)
{% endstep %}

{% step %}
### **Configure the Authorization Header**

Open the **Connection settings** modal by clicking on the Gear icon in the top menu bar.&#x20;

<figure><img src="../.gitbook/assets/2025-07-17 at 12.10.25 - Screengrab@2x.png" alt=""><figcaption></figcaption></figure>

Within the **Connection settings** modal, there is a **Shared headers** section. Select "Authorization header" in the header key input.&#x20;

{% hint style="warning" %}
You will need an API key generated from the Tokens Studio platform. If you don't have this available, you can follow [these instructions to generate one](./#creating-an-api-key).
{% endhint %}

In the value input: `Bearer <API_KEY>` (replace `<API_KEY>` with your API key. Click save.

<figure><img src="../.gitbook/assets/CleanShot 2025-03-27 at 23.33.13@2x.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### **View the available queries:**

<figure><img src="../.gitbook/assets/CleanShot 2025-03-27 at 23.34.36@2x.png" alt=""><figcaption></figcaption></figure>

The query section will show the available queries as can be seen in the [SDK-CLI documentation > Query page](https://tokens-studio.github.io/studio-app/types/Query.html).

<figure><img src="../.gitbook/assets/CleanShot 2025-03-27 at 23.34.14@2x.png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

## Example: Running a Query

{% stepper %}
{% step %}
### Choose the query to use

<figure><img src="../.gitbook/assets/CleanShot 2025-03-28 at 00.04.12@2x (1).png" alt=""><figcaption></figcaption></figure>

Click on `projects(...): PaginatedProjects!` in the Fields section. This will automatically populate the base query in the Operations section of the Apollo playground.
{% endstep %}

{% step %}
### Add the model to return.

<figure><img src="../.gitbook/assets/CleanShot 2025-03-28 at 00.04.56@2x.png" alt=""><figcaption></figcaption></figure>

Add `data: [Project!]!`. Again, this will auto-populate the Operations field. This step is needed because the Projects list is a paginated response.
{% endstep %}

{% step %}
### Add the fields you want returned

<figure><img src="../.gitbook/assets/CleanShot 2025-03-28 at 00.05.33@2x.png" alt=""><figcaption></figcaption></figure>

Click on `name: String!` and `organizationId: String!` to add them to the query

Your query should be the following now:

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
{% endstep %}

{% step %}
### Add variables

In the "**Variables**" section, we need to add the organisation id. To get the organisation ID, Navigate to your organization in Studio. Copy the **Organization ID** from the URL (after `/org/`).

<figure><img src="../.gitbook/assets/CleanShot 2025-03-28 at 00.06.14@2x.png" alt=""><figcaption></figcaption></figure>

Return to the Apollo Sandbox, enter the organisation id in the "**Variables section**".

```json
{
    "organization": "<org-ID>"
}
```
{% endstep %}

{% step %}
### Run the Query

<figure><img src="../.gitbook/assets/CleanShot 2025-03-28 at 00.07.30@2x.png" alt=""><figcaption></figcaption></figure>

Click the button in the top right corner to receive a list of projects in the response.  The name  and organization id will be displayed for each item in the list.
{% endstep %}
{% endstepper %}

