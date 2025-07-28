# TASK-8-Simple-Sales-Dashboard-Design


# 📊 Simple Sales Dashboard Project – README

## 🧾 Project Title:
**Superstore Sales Dashboard in Power BI**

---

## 📁 Dataset:
**Superstore_Sales.csv**

### 🔍 Key Columns Used:
- Order Date
- Region
- Category
- Sales
- Profit

---

## 🎯 Objective:
To build an **interactive and visual sales performance dashboard** using Power BI that shows:
- Sales trends over time  
- Performance by region  
- Category-level breakdown  
- User-driven interactivity with filters/slicers

---

## 🛠 Tools Used:
- Power BI Desktop
- Optional preprocessing with Power Query

---

## 🗂 Steps Performed:

### 1. Data Import & Cleaning
- Imported the Superstore dataset in `.csv` format.
- Removed unnecessary columns.
- Converted `Order Date` to `Month-Year` format using:


### 2. Visualizations Created

| Visual | Fields Used | Purpose |
|--------|-------------|---------|
| **Bar Chart** – Sales by Region | Region, Sales | Compare sales across regions |
| **Pie Chart** – Sales by Region | Region, Sales | Show percentage share by region |
| **Donut Chart** – Sales by Category | Category, Sales | Visualize category-wise sales |
| **Line Chart** – Sales over Time | Order Date, Sales | Show sales trend across months |

#### 🎛️ Slicer:
- Added a slicer for **Region** to filter data interactively.

---

## 🎨 Styling & Formatting
- **Colors**: Green for top-performing (e.g., West, Technology), red for lower performers.
- **Data Labels**: Enabled for all visuals.
- **Titles**: Renamed chart titles for clarity.

---

## 📈 Key Insights

1. **West Region Has the Highest Sales**  
 - 31.58% of total sales (Bar & Pie Charts)

2. **Technology Leads in Sales by Category**  
 - Highest share (11.53%) in Donut Chart

3. **Sales Trend Shows Decline Over Time**  
 - Downward trend seen in Line Chart (2017 to 2014)

4. **South Region Has the Lowest Sales**  
 - Only 17.05% of total sales

---

## 📦 Deliverables

| File | Description |
|------|-------------|
| `dashboard_screenshot.png` | Screenshot of the final dashboard |
| `sales_insights.docx` | Key insights extracted from the dashboard |
| *(Optional)* `dashboard.pbix` | Power BI source file |

---

## ✅ Outcome
- Built a clear and interactive dashboard.
- Practiced visual formatting and slicers in Power BI.
- Gained business insights from sales data using visuals.
