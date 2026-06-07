
# UPI Transactions Analytics Dashboard

### Project Link: https://app.powerbi.com/groups/me/reports/0853ecad-9960-4e45-afd6-41f5948a4c6c/b9feda440a06c9913cc4?experience=power-bi


![image alt](https://github.com/user-attachments/assets/c19d589a-6f60-4fe9-bc50-e0165aae6885)

## Situation (The Problem)

The adoption of digital payments has completely transformed how people spend, transfer, and manage their money. With the massive rise of UPI (Unified Payments Interface), financial institutions and merchants are sitting on a goldmine of transaction data. 

However, looking at raw Excel sheets full of transaction logs is overwhelming. The data was messy—account numbers were appearing in scientific, exponential formats, and time logs were corrupted with dummy dates. The management team needed to make sense of this raw data to understand exactly how their customers were interacting with the UPI ecosystem. They needed clear answers to operational questions:
* How much total money is moving through the system, and what is the success rate?
* What time of day is the busiest for digital payments?
* Are people using QR codes, Phone Numbers, or UPI IDs the most?
* What are people actually buying (Food, Travel, Bill Payments)?
* Which banks and merchants process the highest volume of transactions?

## Task (The Goal)

My mission was to take this messy, raw transaction data and engineer a clean, interactive data model. 

The goal was to build a comprehensive analytics hub where stakeholders could instantly evaluate the health of the UPI payment network over a specific period (May to June 2024). By cleaning the data and calculating core financial metrics, the team needed to shift from blindly processing transactions to strategically understanding consumer spending habits, technical failure rates, and peak usage hours.

## Action (How I Processed the Data)

To turn these raw payment logs into a strategic asset, I broke the project down into a step-by-step data processing and modeling workflow using Power Query and Power BI:

* **Step 1: Data Extraction & Deep Cleaning:** I imported the raw Excel data into Power Query. I immediately noticed that critical fields like Customer and Merchant Account Numbers were incorrectly formatted as exponential numbers. I manually converted these to text strings to prevent massive data loss and ensure no rogue zeros were added to the account numbers. 
* **Step 2: Time Intelligence Formatting:** The "Transaction Time" column was corrupted with an irrelevant date attached to every timestamp. I used delimiter splitting to isolate the exact time of day, discarding the broken date data so we could accurately track daily peak hours.
* **Step 3: Calculating Core Financial Metrics:** I established the big-picture numbers. I programmed calculations to track the absolute **Total Transactions**, the **Total Amount** of money moved, the **Average Remaining Balance** in users' accounts post-transaction, and the **Average Customer Age**.
* **Step 4: Mapping Consumer Behavior:** I grouped the transaction data by category to understand *why* people were spending. I categorized the spending purpose (Shopping, Travel, Food) and split the data by payment method (Instant vs. Scheduled, and QR Code vs. Phone Number).
* **Step 5: Ecosystem Tracking:** Finally, I linked the transactions to their respective hardware and networks. I tracked which devices (Mobile, Tablet, Laptop) were being used, which cities generated the most traffic, and which Sender/Receiver banks were handling the load.

## Result (The Business Impact)

By organizing and modeling the data, we uncovered several powerful insights regarding how consumers navigate the digital payment landscape:

### 1. Macro Financials & Network Health

![image alt](https://github.com/user-attachments/assets/c899b44c-559e-4faa-a9b3-cea3b26ad6c0)

The ecosystem is incredibly active. Over the tracked period, the network successfully processed **2,000 transactions** moving a massive **52.54 Million** in capital. The average user maintains a healthy remaining balance of around **8.16 Million**, and the system shows an overwhelmingly high success rate with very few failed transactions.

### 2. Peak Hours & Traffic Management
By isolating the exact transaction times, a clear daily pattern emerged. Transaction volume stays relatively low in the early morning but spikes aggressively late at night, hitting its absolute **peak at 21:00 (9:00 PM)**. Technical teams can use this insight to ensure server maintenance is never scheduled during the evening rush.

### 3. Consumer Spending Habits

![image alt](https://github.com/user-attachments/assets/4c80e3a1-9cce-48a1-bac4-b0ac56af3595)

* **The "Instant" Economy:** A staggering **80.1%** of all transactions are Instant Payments, proving that the modern consumer relies on immediate liquidity rather than Scheduled Payments (19.9%).
* **Balanced Spending:** Unlike some networks that heavily skew toward one industry, spending on this network is perfectly balanced. Shopping, Travel, Food, Bill Payments, and "Others" each capture roughly **20%** of the transaction volume.
* **The Hardware:** Unsurprisingly, **Mobile** devices completely dominate the transaction space, vastly outperforming Tablets and Laptops, reinforcing the need for mobile-first payment gateways.

### 4. Demographics & Equality
The data painted a clear picture of the user base. The average customer utilizing the network is **36 years old**. Furthermore, the financial footprint is incredibly balanced across genders, with Male, Female, and "Other" demographics all moving roughly equal amounts of capital (between 17M and 18M each), showing widespread, uniform adoption of digital payments.

## Future Enhancements

To make this data ecosystem even more powerful in the future, we could introduce:
* **Failure Point Analysis:** Linking failed transactions directly to specific Sender/Receiver banks or specific times of day to pinpoint exactly which financial institutions are causing network bottlenecks.
* **Merchant-Specific Trends:** Deep-diving into the merchant data to track exactly what time of day apps like Zomato, Swiggy, or Amazon experience their highest payment volumes.


