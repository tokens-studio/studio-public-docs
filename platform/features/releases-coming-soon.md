# Releases (Coming soon)

The **Releases** feature in Tokens Studio allows you to create structured versions of your design tokens, enabling version control similar to Git workflows. With this feature, you can manage changes, track updates, and export token configurations for seamless integration with your projects.

### Creating a Release

Before you create a release, ensure that:

* Your design tokens are set up.
* Your themes are set up.
* Your export configurations (e.g., web, mobile, etc.) are defined.

To create a release:

1. Navigate to the **Releases** module in the left panel.
2. You will see a list of previously created releases.
3. Click **Create New Release**.

### Defining a Release Version

When creating a new release, you can select a versioning type:

* **Patch Version** – For minor fixes or adjustments.
* **Minor Version** – For small feature updates.
* **Major Version** – For significant changes or breaking updates.
* **Canary Version** – For testing purposes before full deployment.

Additionally, you can:

* Add **Release Notes** to document changes.
* Choose to **Export Style Dictionary Configurations**, which include all predefined configurations for various platforms.

### Publishing a Release

1. Review and select the desired configuration.
2. Click **Publish Release**.
3. The newly created release will now be visible in the Releases list.

### Reviewing and Downloading Releases

Once a release is published:

* Click on the release to view details, including:
  * Release notes
  * Date of publication
  * Publisher details
  * **Artifacts** (exportable files)

The release artifacts include:

* **Tokens (.json)** – A downloadable ZIP file containing all design tokens.
* **Style Dictionary Configuration** – A structured JSON file that defines token relationships and export settings.

<figure><img src="../../.gitbook/assets/CleanShot 2025-03-08 at 17.27.52.gif" alt=""><figcaption></figcaption></figure>

For more details, explore [**Configuration**](configuration.md) and [**Tokens**](tokens/).
