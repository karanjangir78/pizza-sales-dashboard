# pizza-sales-dashboard
# 🍕 Pizza Sales Dashboard

An interactive **Power BI dashboard** analyzing pizza sales data across 5,000+ orders over 3 months. Tracks revenue, order volume, and customer trends with insights on top/least-selling pizzas, peak order times, and sales patterns — built to help optimize the menu, monitor KPIs, and drive data-backed decisions.

---

## 📊 Dashboard Preview

> Screenshots from the `dashboard preview/` folder
<img width="1343" height="732" alt="image" src="https://github.com/user-attachments/assets/8c71488b-4a43-426e-bbc3-bdbfa3c39b16" />
<img width="1348" height="778" alt="image" src="https://github.com/user-attachments/assets/ec785add-0a44-4891-a681-66b3a23ace7b" />

<!-- Add your dashboard screenshots here -->
<!-- ![Home Page](dashboard%20preview/home.png) -->
<!-- ![Best/Worst Sellers](dashboard%20preview/sellers.png) -->

---

## 🔍 Key Insights Tracked

- **Total Revenue** — overall and by category
- **Average Order Value** — across time periods
- **Total Pizzas Sold** — with daily & monthly trends
- **Peak Order Times** — by hour and day of week
- **Top 5 Best-Selling Pizzas** — by revenue and quantity
- **Bottom 5 Least-Selling Pizzas** — for menu optimization
- **Sales by Pizza Category & Size** — Classic, Supreme, Veggie, Chicken

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Dashboard design & visualization |
| **DAX** | Calculated measures & KPIs |
| **SQL** | Data extraction & preprocessing |
| **Microsoft Excel** | Initial data exploration |
| **Power BI Service** | Publishing & scheduled refresh |

---

## 📁 Repository Structure

```
pizza-sales-dashboard/
│
├── pizza_sales[1].csv                  # Raw sales dataset (~5,000 orders)
├── pizza_sales_report_(1)[1].pbix      # Power BI report file
├── dashboard preview/                  # Screenshots of dashboard pages
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
- [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) (free download)

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/karanjangir78/pizza-sales-dashboard.git
   ```

2. **Open the report**
   - Launch Power BI Desktop
   - Open `pizza_sales_report_(1)[1].pbix`

3. **Refresh data** (if needed)
   - Go to **Home → Refresh**
   - Ensure `pizza_sales[1].csv` is in the same directory

---

## 📐 DAX Measures Used

```dax
-- Total Revenue
Total Revenue = SUM(pizza_sales[total_price])

-- Average Order Value
Avg Order Value = [Total Revenue] / DISTINCTCOUNT(pizza_sales[order_id])

-- Total Pizzas Sold
Total Pizzas Sold = SUM(pizza_sales[quantity])

-- Total Orders
Total Orders = DISTINCTCOUNT(pizza_sales[order_id])

-- Average Pizzas Per Order
Avg Pizzas Per Order = [Total Pizzas Sold] / [Total Orders]
```

---

## 📈 Dashboard Pages

| Page | Description |
|------|-------------|
| **Home / KPI Overview** | Key metrics — revenue, orders, avg order value, load time <4s |
| **Best & Worst Sellers** | Top 5 and bottom 5 pizzas by revenue, quantity, and orders |

---

## 📦 Dataset

The dataset (`pizza_sales[1].csv`) contains ~5,000 pizza orders with the following columns:

| Column | Description |
|--------|-------------|
| `order_id` | Unique order identifier |
| `order_date` | Date of the order |
| `order_time` | Time of the order |
| `pizza_name` | Name of the pizza |
| `pizza_category` | Category (Classic, Supreme, Veggie, Chicken) |
| `pizza_size` | Size (S, M, L, XL, XXL) |
| `quantity` | Number of pizzas ordered |
| `unit_price` | Price per pizza |
| `total_price` | Total line item price |

---

## 🎯 Business Use Cases

- Identify **high-margin, high-demand** pizzas to prioritize in marketing
- Spot **underperforming items** for menu rationalization
- Schedule **staff and inventory** around peak order hours
- Monitor **daily/weekly revenue trends** for operations planning

---

## 🤝 Connect

**Karan Jangir** — Data Analyst

[![LinkedIn](https://img.shields.io/badge/LinkedIn-karanjangir-blue?style=flat&logo=linkedin)](https://linkedin.com/in/karanjangir)
[![GitHub](https://img.shields.io/badge/GitHub-karanjangir78-black?style=flat&logo=github)](https://github.com/karanjangir78)

---

*Built as part of a Data Analyst internship at Navodita Infotech, Jun–Jul 2025.*
