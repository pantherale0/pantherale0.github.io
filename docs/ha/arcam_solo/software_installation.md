
Once you've connected your Arcam Solo to your Home Assistant system using either the serial adapter (recommended) or the ESP32 method, you'll need to install the integration in Home Assistant. The easiest way to do this is using HACS (Home Assistant Community Store).

**Installation via HACS (Custom Repository):**

Because this is a custom repository, you'll need to add it to HACS manually before you can install the integration. If you don't have HACS installed, please follow the [HACS installation instructions](https://hacs.xyz/).

Once you have HACS installed:

1.  In Home Assistant, go to **HACS > Integrations**.
2.  Click the **three dots** in the top right corner and select **Custom repositories**.
3.  Add the following information:
    *   **Repository:** `https://github.com/pantherale0/ha-arcamsolo` (This is the repository URL)
    *   **Category:** `Integration`
4.  Click **Add**.
5.  Now, in **HACS > Integrations**, click the **+ Explore & Add Repositories** button.
6.  Search for `Arcam Solo`.
7.  Select the `Arcam Solo` integration and click **Install**.
8.  Restart Home Assistant.

After restarting, you can configure the integration through the Home Assistant Integrations page (Settings > Devices & Services > Add Integration).
