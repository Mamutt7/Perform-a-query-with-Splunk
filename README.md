# Perform a Query with Splunk

This project demonstrates how to use Splunk to analyze log data and identify failed SSH login attempts.

---

## Uploading Data

![Uploading Data](https://github.com/user-attachments/assets/ad6a4172-e1b5-4995-ad55-77691518e786)

Here, I uploaded `tutorialdata.zip` into Splunk using the **Add Data** interface. This process allows Splunk to index the data, making it searchable for analysis. The uploaded dataset is stored under the default `main` index.

---

## Performing the Initial Query

![Search & Reporting Tab](https://github.com/user-attachments/assets/905ce2ed-d5fa-41d0-a1f4-5739f9c879e3)

Using the **Search & Reporting** tab, I performed an initial query by searching for `index="main"`. This query retrieves all events stored in the `main` index. The **All Time** filter was applied to ensure all log data is included in the search results. This broad query serves as the foundation for narrowing down specific patterns or anomalies in the data.

---

## Identifying Failed Login Attempts

<img width="1211" alt="Failed Login Query" src="https://github.com/user-attachments/assets/a61a04eb-2817-4c4d-93d4-0fc15e6b757e" />

To detect failed SSH login attempts, I refined the query to:

```splunk
index="main" host="127.0.0.1" fail* root
```
---

## Key Takeaways

1. **Data Upload**: Successfully imported `tutorialdata.zip` into Splunk, making the logs accessible for analysis.
2. **Initial Search**: Performed a broad query to retrieve all events from the `main` index, establishing a baseline for further refinement.
3. **Focused Search**: Used a refined query with keywords `Failed` and `root` to identify failed SSH login attempts from the localhost (`127.0.0.1`).
4. **Log Insights**: Highlighted suspicious activity in log data, demonstrating the effectiveness of targeted searches.

---

## Summary

This project showcases Splunk’s ability to analyze log data for security insights. By starting with data upload and progressing to refined search queries, we successfully identified failed SSH login attempts. The structured approach and use of filters provided clear and actionable insights into system activity. Future improvements could include automated alerts, visualizations, and broader log analysis to enhance the monitoring capabilities.

