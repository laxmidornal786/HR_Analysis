# HR_Analysis
An interactive HR Workforce &amp; Attrition Dashboard built in Power BI to track employee metrics, attrition trends, and workforce distribution. Helps HR and management make data-driven decisions for retention and workforce planning.


1.Dataset  
The dataset is stored in Excel with 3 main sheets:  

- **Data** → Employee details (Name, Gender, Age, Department, Salary, Hire Date, Exit Date, Attrition Risk, etc.)  
- **Summary** → KPI summary (Total Employees, Current Employees, Exits, Attrition Rate, Avg Salary)  
- **Dashboard** → Prepared data for visualization
  
2.Objectives  
- Perform **data cleaning & preprocessing**  
- Conduct **exploratory data analysis (EDA)**  
- Build **key HR KPIs** such as Total Employees, Attrition Rate, Avg Salary  
- Visualize workforce distribution and attrition trends  
- Provide **insights for HR strategy** and decision-making  

3.Sample DAX Measures  
DAX
- TotalEmployees = COUNTROWS(Data)
- CurrentEmployees = CALCULATE(COUNTROWS(Data), ISBLANK(Data[ExitDate]))
- Exits = CALCULATE(COUNTROWS(Data), NOT(ISBLANK(Data[ExitDate])))
- AttritionRate = DIVIDE([Exits], [TotalEmployees], 0)
- AvgSalary = AVERAGE(Data[Salary])

4.Visualizations (Charts & Graphs)
Bar Chart: Employees by Department
Pie Chart: Gender Distribution
Stacked Bar: Attrition Risk by Department
Line Chart: Attrition Trend by Year (Exit Date)
Map / Bar: Employees by Region

5.Slicers / Filters
- Department
- Gender
- Region
- Attrition Risk

6.How to Use
- Open the .pbix file in Power BI Desktop
- Load data from Excel and check data types
- Create measures using provided DAX formulas
- Design the dashboard layout based on the structure above
- Add slicers for drill-down analysis
- Publish to Power BI Service for sharing with stakeholders

7.Tools & Technologies
- Power BI Desktop → Dashboard & analysis
- Excel → Data preprocessing
- DAX → KPI & measures
- SQL (optional) → Data extraction/ETL

8.Business Value
This HR Dashboard enables organizations to:

- Monitor workforce distribution in real time
- Detect departments or regions with high attrition risk
- Track salary and employment trends
- Improve HR strategies for employee retention

