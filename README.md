# dp-700-lab-07-Real-Time-Stock-Market-Analytics-with-Microsoft-Fabric

https://github.com/user-attachments/assets/eb27a20e-1c1e-4b03-9757-56c57d98e007



# Real-Time Stock Market Analytics with Microsoft Fabric

This project demonstrates the use of **Real-Time Intelligence in Microsoft Fabric** to ingest, store, analyze, and visualize real-time stock market data.

## Overview

This lab exercise includes the following steps:

1. **Workspace Creation**  
   - Created a new Microsoft Fabric workspace with Fabric capacity enabled.

2. **Eventstream Setup**  
   - Connected to the **Stock market sample data** source.
   - Renamed the eventstream to `stock-data` and the associated stream to `stock-data-stream`.

3. **Eventhouse Creation**  
   - Created a new Eventhouse to store and query real-time data.
   - Configured a **KQL database** with a new table named `stock`.

4. **Stream-to-Table Connection**  
   - Set up a connection from the `stock-data` eventstream to the `stock` table.
   - Verified the connection and previewed live data ingestion.

5. **Data Analysis with KQL**  
   - Ran sample KQL queries, including:
     ```kql
     stock
     | take 100
     ```
     and
     ```kql
     stock
     | where ["time"] > ago(5m)
     | summarize avgPrice = avg(todecimal(bidPrice)) by symbol
     | project symbol, avgPrice
     ```

6. **Real-Time Dashboard**  
   - Created a dashboard named **Stock Dashboard**.
   - Pinned average stock prices as a **Column chart** for live data visualization.

7. **Alert Configuration with Activator**  
   - Configured an alert to trigger when average stock price **increases by 100**.
   - Action set to: **Send email notification**.

8. **Cleanup**  
   - All created resources can be deleted by removing the workspace from the Workspace Settings.

## Key Technologies Used

- **Microsoft Fabric Real-Time Hub**
- **Eventstream**
- **Eventhouse & KQL Database**
- **KQL (Kusto Query Language)**
- **Dashboards**
- **Activator for alerts**

## Notes

- This lab showcases a simplified real-time streaming solution.
- In real-world applications, you would typically include **data transformations**, **windowing functions**, and integrate with external actions or alerts.

## Author

This README was prepared based on the successful completion of the Microsoft Fabric lab titled **"Get started with Real-Time Intelligence in Microsoft Fabric"**.
![Screenshot 2025-05-05 at 19 33 12](https://github.com/user-attachments/assets/ff27928f-f920-4954-851f-b505657fd64c)
![Screenshot 2025-05-05 at 19 32 00](https://github.com/user-attachments/assets/c086ddde-c388-4919-9175-c7e78dd41653)
![Screenshot 2025-05-05 at 19 30 37](https://github.com/user-attachments/assets/73d9e017-d3bb-4d80-81e3-6b25a3ed0292)
![Screenshot 2025-05-05 at 19 30 02](https://github.com/user-attachments/assets/a26be504-4f94-4998-a72c-3950ac569a63)
![Screenshot 2025-05-05 at 19 29 20](https://github.com/user-attachments/assets/dbf11f7a-7f43-4b49-9ce5-ff9492fc40a2)
![Screenshot 2025-05-05 at 19 24 12](https://github.com/user-attachments/assets/2ce5e71e-d4f2-40e7-b7e9-853ede0fc671)
![Screenshot 2025-05-05 at 19 23 35](https://github.com/user-attachments/assets/408cc50c-d218-461c-9f72-64be7cddf230)
![Screenshot 2025-05-05 at 19 16 57](https://github.com/user-attachments/assets/46d6a8cd-b8f3-4659-a815-dc2dde6c6cee)
![Screenshot 2025-05-05 at 19 16 25](https://github.com/user-attachments/assets/05afe025-69e8-4aa7-9a1b-9acba54397d9)
![Screenshot 2025-05-05 at 19 16 14](https://github.com/user-attachments/assets/30b1486c-9e1a-4aa0-8265-613bebfaa701)
![Screenshot 2025-05-05 at 19 15 30](https://github.com/user-attachments/assets/cd15f110-93af-4e58-ab41-49bd9e496c81)
![Screenshot 2025-05-05 at 19 15 13](https://github.com/user-attachments/assets/869c0bd2-3acd-40e9-ae4d-725cf2ecf107)
![Screenshot 2025-05-05 at 19 12 05](https://github.com/user-attachments/assets/ce492abd-fed6-4c99-b898-e15ab11b40b5)
![Screenshot 2025-05-05 at 19 11 40](https://github.com/user-attachments/assets/c0d8d893-c0b3-47e6-b0f7-2266dbbbbb2e)

