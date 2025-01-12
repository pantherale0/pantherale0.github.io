# Getting Started

This integration allows you to monitor your Anglian Water usage and estimate your water costs directly within Home Assistant. It retrieves data such as your water consumption, meter readings, *and billing information*, providing you with insights into your water usage habits and spending.

## How it Works

This integration connects to Anglian Water using an existing, but now deprecated, mobile application's API. This allows it to access the same data that was previously available in the app. It then brings this data into Home Assistant as sensors, which you can use in your dashboards, automations, and other Home Assistant features.

**Important Note:** This integration relies on the API of a now-deprecated Anglian Water mobile application. While it currently functions, there is a possibility that Anglian Water may change or discontinue this API in the future, which could cause the integration to stop working. Please contact Anglian Water pushing for a OpenAPI to access your data.

## What Data is Available?

The integration provides the following data (subject to availability from the Anglian Water API):

*   **Water Consumption:** Shows your current and historical water usage.
*   **Meter Readings:** Displays your latest meter readings.
*   **Billing Information:** Provides data related to your water charges, allowing you to estimate your water costs.

This data is presented as sensors in Home Assistant. You can find these sensors by searching for entities related to "Anglian Water" in the Home Assistant developer tools or entity list.

## Calculating Water Costs

Using the available billing information, you can create calculations within Home Assistant to estimate your spending on water usage. This can be done using template sensors or other Home Assistant features that allow for mathematical operations.

**Important Note Regarding Waste:** *This cost estimation currently only considers your water consumption. It does not factor in waste water charges. Therefore, the calculated cost will be an estimate of your water supply costs only, and not your total water bill.*

## Using the Integration

Once configured, Anglian Water data will be automatically updated at regular intervals. You can then use this data in various ways within Home Assistant:

*   **Dashboards:** Create custom dashboards to visualize your water usage and estimated costs over time.
*   **Automations:** Set up automations to notify you of high water consumption, potential leaks, or unusual spending patterns.
*   **Energy Dashboard:** Track your water usage and estimated costs alongside your energy consumption.
