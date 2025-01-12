### `anglian_water.force_refresh_statistics` Service

This service allows you to manually trigger a refresh of your Anglian Water statistics within Home Assistant. This can be useful if you believe the data currently displayed in your dashboards or automations is outdated.

**How it works:**

When you call this service, it retrieves water consumption and cost data directly from Anglian Water's API. The retrieved data covers a specific timeframe based on the provided parameters. Here's a breakdown of the service functionality:

*   Retrieves historical data: By default, the service retrieves data for the previous day. You can optionally specify a custom start date using the `start` parameter in the service call.
*   Updates statistics: The retrieved consumption data is used to update the `anglian_water_previous_consumption` statistic.
*   Calculates costs: Based on the consumption data and your Anglian Water tariff rate, the service calculates and updates the `anglian_water_previous_costs` statistic, reflecting the estimated cost of your water usage.
*   Updates dashboards: The updated statistics should automatically reflect in your Home Assistant dashboards that display Anglian Water data.

**Service Call Parameters:**

*   `start`: This parameter allows you to specify the start date for retrieving data. The format should be YYYY-MM-DD (e.g., 2025-01-10).
*   `end`: This parameter allows you to specify the end date for retrieving data.

**Example Usage:**

To trigger a refresh of Anglian Water statistics for a specific date (e.g., December 31st, 2024):

```yaml
service: anglian_water.force_refresh_statistics
data:
  start: "2024-12-31"
  end: "2025-01-01"
```

**Important Notes:**

*   This service relies on the Anglian Water API, which may be unavailable at times due to maintenance or other reasons.
*   The Anglian Water API provides meter readings approximately once every 24 hours. This means the retrieved data may lag behind by up to a day.
*   This service estimates your water costs based on consumption data and your tariff rate. It does not account for waste water charges, so the calculated cost reflects your water supply costs only.

For troubleshooting and additional information about the Anglian Water integration in Home Assistant, refer to Getting Started and Troubleshooting pages.
