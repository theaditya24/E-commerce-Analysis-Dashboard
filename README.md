# 🛒 E-commerce Analysis Dashboard

An interactive **Power BI dashboard** for analyzing retail/e-commerce sales performance — built on a star-schema data model with fact and dimension tables covering transactions, customers, products, stores, and time.

---

## 📌 Overview

This project turns raw retail transaction data into an interactive Power BI report that helps identify sales trends, top-performing products/stores, and customer behavior patterns. It's designed as an end-to-end example of dimensional data modeling (star schema) combined with Power BI visualization and DAX-driven analysis.

**Key questions this dashboard answers:**
- What are our total sales, orders, and revenue trends over time?
- Which products, categories, and stores are top performers?
- Who are our most valuable customers, and how do they behave?
- How does performance vary by region, season, or time period?

---

## 🗂️ Data Model

The dataset follows a classic **star schema**, with one central fact table connected to descriptive dimension tables:

| File | Type | Description |
|------|------|-------------|
| `fact_table.csv` | Fact | Core transactional data — sales, quantities, revenue, and foreign keys linking to all dimension tables |
| `Trans_dim.csv` | Dimension | Transaction-level attributes (order/transaction details) |
| `customer_dim.csv` | Dimension | Customer profile and demographic attributes |
| `item_dim.csv` | Dimension | Product/item details (category, pricing, etc.) |
| `store_dim.csv` | Dimension | Store/location attributes |
| `time_dim.csv` | Dimension | Calendar attributes (day, month, quarter, year) for time intelligence |

```
                     ┌───────────────┐
                     │  customer_dim │
                     └───────┬───────┘
                             │
     ┌───────────┐   ┌───────┴───────┐   ┌───────────┐
     │  store_dim │──│  fact_table   │──│  item_dim  │
     └───────────┘   └───────┬───────┘   └───────────┘
                             │
                     ┌───────┴───────┐
                     │   time_dim    │
                     └───────────────┘
                     (Trans_dim provides transaction-level detail)
```

## 📁 Repository Structure

```
E-commerce-Analysis-Dashboard/
├── Retail Sales Analysis Dashboard.pbix   # Power BI report file (open with Power BI Desktop)
├── fact_table.csv                         # Fact table
├── Trans_dim.csv                          # Transaction dimension
├── customer_dim.csv                       # Customer dimension
├── item_dim.csv                           # Item/product dimension
├── store_dim.csv                          # Store dimension
├── time_dim.csv                           # Time/calendar dimension
├── template.png                           # Dashboard preview image
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free, Windows only)

### Steps
1. **Clone or download** this repository:
   ```bash
   git clone https://github.com/theaditya24/E-commerce-Analysis-Dashboard.git
   ```
2. Open **`Retail Sales Analysis Dashboard.pbix`** in Power BI Desktop.
3. If prompted, point the data source connections to the CSV files in the cloned folder (`fact_table.csv`, `customer_dim.csv`, `item_dim.csv`, `store_dim.csv`, `time_dim.csv`, `Trans_dim.csv`).
4. Click **Refresh** on the Home ribbon to load the latest data.
5. Explore the report pages and use the slicers/filters to drill into specific stores, products, time periods, or customer segments.

> 💡 To view the dashboard without Power BI Desktop, publish it to the [Power BI Service](https://app.powerbi.com) and share the link, or export report pages to PDF/images.

---

## 📊 Dashboard Highlights

- **Sales Overview** — total revenue, order volume, and trend lines over time
- **Product Performance** — best/worst-selling items and category breakdowns
- **Store Comparison** — revenue and performance by store/location
- **Customer Insights** — customer segmentation and purchasing behavior
- **Time Intelligence** — month-over-month and year-over-year comparisons using the time dimension

---

## 🛠️ Tech Stack

- **Power BI Desktop** — data modeling, DAX measures, and visualization
- **Power Query** — data transformation and cleaning
- **CSV** — flat-file data sources structured as a star schema

---

## 🤝 Contributing

Contributions are welcome! If you'd like to improve the data model, add new visuals, or extend the analysis:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes
4. Open a pull request

---

## 📄 License

This project is available for learning and portfolio purposes. Add a license of your choice (e.g., MIT) if you plan to distribute or reuse this work.

---

## 👤 Author

**Aditya** — [@theaditya24](https://github.com/theaditya24)
