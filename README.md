# 📊 Sales Analytics Dashboard using Power BI

![Sales Dashboard](https://github.com/Mosaad2010-star/Sales-Analytics-PBI/blob/main/Sales%20dashboard%20image.PNG?raw=true)



## 📄 ملخص المشروع (باللغة العربية)

يهدف هذا المشروع إلى تطوير لوحة معلومات احترافية باستخدام Power BI لتحليل أداء المبيعات داخل المؤسسة، وتمكين الإدارات المختلفة من اتخاذ قرارات دقيقة وسريعة بناءً على بيانات فعلية.

### 🔧 الخطوات التي تم تنفيذها:

1. **تجميع بيانات المبيعات**:
   - تم استخدام بيانات تحتوي على تفاصيل الطلبات مثل: رقم الطلب، تاريخ الطلب، اسم المنتج، الكمية، وإجمالي قيمة المبيعات.

2. **معالجة البيانات وتحميلها في Power BI**:
   - تم استيراد البيانات ومعالجتها داخل Power BI، مع التأكد من دقة الأنواع والارتباطات.

3. **إنشاء مقاييس تحليلية باستخدام DAX**:
   - تطوير مقاييس لحساب:
     - إجمالي المبيعات.
     - إجمالي الكمية المباعة.
     - عدد الطلبات.
     - المنتج الأعلى مبيعًا.

4. **تصميم لوحة المعلومات**:
   - تحتوي اللوحة على عدة عناصر تفاعلية:
     - مخطط زمني لتطور المبيعات.
     - رسم بياني للأداء حسب المنتج.
     - توزيع المبيعات عبر المنتجات.
     - مؤشرات رئيسية (KPIs) تعرض إجماليات العمليات.
     - أدوات تصفية حسب التاريخ والمنتج.

5. **تحليل النتائج واستخلاص رؤى قابلة للتنفيذ**:
   - تحديد المنتجات الأعلى والأقل أداءً.
   - التعرف على الاتجاهات الموسمية للمبيعات.
   - تحسين التخطيط للطلبيات المستقبلية.

    - تعزيز فهم سلوك العملاء في فترات مختلفة من السنة.

### 🧰 الأدوات المستخدمة:


- **Power BI Desktop** – لتصميم النموذج التحليلي ولوحة المعلومات.
- **DAX** – لحساب المقاييس والمؤشرات.
- **Excel** – لتنظيم وتنسيق البيانات المصدرية.

### 🎯 أثر المشروع:

ساهم هذا المشروع في تحسين جودة التقارير البيعية، وتوفير وقت التحليل اليدوي، وتقديم رؤى عميقة ساعدت على:
- اتخاذ قرارات مبنية على البيانات.
- تحسين الأداء البيعي والتسويقي.
- توجيه الجهود نحو المنتجات ذات العائد الأعلى.









## 🧠 Problem Statement

The sales team faced several challenges:
- Unclear visibility of top-performing products.
- No easy way to detect sales trends or seasonality.
- Static Excel reports with limited interactivity.
- Time-consuming reporting process.

These issues slowed down data-driven decision-making and operational agility.

---

## 🎯 Objective

To build an interactive Power BI dashboard that:
- Provides clear metrics like revenue, quantity, and order count.
- Visualizes top products and sales trends over time.
- Enables dynamic filtering by product or time.
- Enhances strategic decision-making through self-service analytics.

---

## 📈 Project Workflow: From Problem to Solution

### 1. 🧾 Data Creation
- A synthetic dataset was generated with **500 sales transactions** and the following columns:
  - `OrderID`
  - `OrderDate`
  - `Product`
  - `Quantity`
  - `TotalAmount`
- Products include: Laptop, Smartphone, Tablet, Monitor, Keyboard, Mouse, Headphones.

### 2. 📥 Data Import in Power BI
- The dataset (`sample_sales_data.xlsx`) was imported.
- Table name: `Sales`.
- Data types were validated and column formatting was adjusted.

### 3. 📊 DAX Measures

```DAX
Total Sales = SUM(Sales[TotalAmount])

Total Quantity = SUM(Sales[Quantity])

Number of Orders = DISTINCTCOUNT(Sales[OrderID])

MonthYear = FORMAT(Sales[OrderDate], "MMM YYYY")

Top Product = 
CALCULATE(
    FIRSTNONBLANK(Sales[Product], 1),
    TOPN(1, VALUES(Sales[Product]), CALCULATE(SUM(Sales[TotalAmount])), DESC)
)

### 4. 🧩 Dashboard Design

Visuals used:

- 📈 **Line Chart**: Sales trend over time.
- 📊 **Bar Chart**: Revenue by product.
- 🥧 **Pie Chart**: Sales distribution by product.
- 🧮 **Cards**: Total sales, total quantity, number of orders.
- 🔍 **Slicers**: Product & OrderDate filters for interactivity.

All visuals support cross-filtering for drill-down analysis.

---

## 💡 Insights Uncovered

- Most profitable products by revenue.
- Sales seasonality and monthly trends.
- Peak order periods and underperforming products.
- Quick comparison of product performance across time.

---


---

## 🛠️ Tools & Technologies Used

- **Power BI Desktop** – Data modeling & visual analytics.
- **DAX (Data Analysis Expressions)** – Custom measures and KPIs.
- **Excel** – Mock data generation.

---

## 🚀 Project Impact

This project illustrates how companies can:

- Automate reporting with zero manual effort.
- Enable real-time sales monitoring.
- Provide strategic insights for sales and marketing teams.
- Transition from static spreadsheets to interactive dashboards.

---

## 📬 Contact

For any suggestions or questions:

**GitHub:** [Mosaad2010-star](https://github.com/Mosaad2010-star)  
**Project Repo:** [Sales-Analytics-PBI](https://github.com/Mosaad2010-star/Sales-Analytics-PBI)

---

