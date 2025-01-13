# Getting Started

This integration allows you to control your Arcam Solo music system directly from Home Assistant. You can use it to turn your Solo on and off, change the volume, select different inputs (like CD, streaming, or radio), and more, all from your Home Assistant interface.

## How it Works

This integration communicates with your Arcam Solo using its serial port. Because the Arcam Solo doesn't have built-in network connectivity, you'll need to set up a connection between your Solo and your Home Assistant system. The recommended method is using a USB-to-serial adapter connected to your Solo and then to a device running Home Assistant (or a device accessible by Home Assistant over the network).

While it's *possible* to use a hardware modification with an ESP32 microcontroller as a serial-to-network bridge (using software like ser2net), this method is *not recommended*. The Arcam Solo's VOUT pins can exhibit unexpected behavior when used with ESP microchips, potentially leading to instability or other issues.

**Important Note:** Connecting your Arcam Solo to Home Assistant using either method will disable the Solo's iPod functionality.

## What Can You Do?

With this integration, you can:

*   **Turn your Solo on and off:** Easily control the power state of your Arcam Solo.
*   **Adjust the volume:** Raise or lower the volume from Home Assistant.
*   **Select inputs:** Switch between different sources like CD, streaming services (if supported by your Solo), radio, and other connected devices.
*   **Use in automations:** Create automations in Home Assistant to control your Solo automatically. For example, you could have your Solo turn on when you arrive home or turn off when you go to bed.
*   **Control from your dashboards:** Add controls for your Solo to your Home Assistant dashboards for easy access.

## Important Notes

*   Your Arcam Solo needs to be connected to your Home Assistant system (or a device accessible by Home Assistant) using either a serial adapter (recommended) or a hardware modification (ESP32 - not recommended).
*   Using either of these methods will disable the Solo's iPod functionality.
*   The features available depend on the specific model of your Arcam Solo (although the serial protocol is the same for both variants).
