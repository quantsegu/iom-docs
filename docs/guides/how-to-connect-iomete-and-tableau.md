---
title: Tableau Connection
description: How to connect IOMETE and Tableau. This guide explains how to effortlessly integrate iomete with one of the most popular BI tools Tableau
last_update:
  date: 12/13/2022
  author: Lakshmi Segu
---
# IOMETE - Tableau Integration
<Img src="IOMETE%20-%20Tableau%20Integration%20529e31fe308f4194ac2164f96102e0da/Untitled.png" caption="Image label" alt="Alternative text" />

![IOMETE - Tableau](IOMETE%20-%20Tableau%20Integration%20529e31fe308f4194ac2164f96102e0da/Untitled.png)

Hi! In this guide, we will explain how to effortlessly integrate **IOMETE** with one of the most popular BI tools: Tableau.

## What is Tableau?[](https://iomete.com/docs/guides/how-to-connect-iomete-and-metabase-bi#what-is-metabase)

Tableau is an Business Intelligence, Reporting and Dashboarding tool. Data has limitless potential to transform businesses and the world as long as people are empowered to use it. Tableau is used to build a data culture and to change lives while providing access to the data.

### Tableau should be accessible from cloud[](https://iomete.com/docs/guides/how-to-connect-iomete-and-metabase-bi#how-to-run-metabase-locally)

Tableau can be directly connected from the tableau cloud page. 

### Add IOMETE as the data source[](https://iomete.com/docs/guides/how-to-connect-iomete-and-metabase-bi#add-iomete-as-the-data-source)

The next step is to connect the IOMETE Lakehouse to Tableau.

Create a new workbook in Tableau. Once new workbook interface is opened up, you will have the following menu, where you need to add a new data source:

![Untitled](IOMETE%20-%20Tableau%20Integration%20529e31fe308f4194ac2164f96102e0da/Untitled%201.png)

After clicking on the “New Data Source”, an option would be provided to select a source. Then click on “Connectors” tab. In the Connectors tab, select **Spark SQL** as your database:

![Untitled](IOMETE%20-%20Tableau%20Integration%20529e31fe308f4194ac2164f96102e0da/Untitled%202.png)

Once Spark SQL is selected following pop-up would be provided, and then you should be able to enter the details for connecting to IOMETE Lakehouse. Server details can be found in your “Lakehouse” which you want to connect for analytical purposes. 

![Untitled](IOMETE%20-%20Tableau%20Integration%20529e31fe308f4194ac2164f96102e0da/Untitled%203.png)

All connection properties can be extracted from the connection string, from the “lakehouse” details sheet in IOMETE (sample picture below):

| Connection | SparkThriftServer(Spark1.1 and later) |
| --- | --- |
| Server | <cloud_region>.iomete.com |
| Port | 443 (default) |
| Authentication | default (info) |
| username | {your user name} |
| password | {your password} |
| Transport | HTTP (Selection) |
| HTTP Path | lakehouse/{accountid}/{lakehousename} |

![Untitled](IOMETE%20-%20Tableau%20Integration%20529e31fe308f4194ac2164f96102e0da/Untitled%204.png)

Once the platform is connected, it would appear as a database as presented below with name “Fuad”. And then the “Schema” provides list of schemas from which tables can be selected for reporting purposes.

In the following example, “sample_db” schema is selected and then “employees_proxy” database is previewed before it’s used part of the report to be generated.

![Untitled](IOMETE%20-%20Tableau%20Integration%20529e31fe308f4194ac2164f96102e0da/Untitled%205.png)

Looking at the table details helps to understand the data types and based on which the reporting can take place. 

The report requirement is to generate the gender equality for recruitment within organization across years.

![Untitled](IOMETE%20-%20Tableau%20Integration%20529e31fe308f4194ac2164f96102e0da/Untitled%206.png)

Once table is selected we can add a report to the sheet, by adding a attribute (”Hire Date”) to the report Sheet. It’s done by clicking on the “Add to Sheet” after right-clicking on a attribute. Hire Date is important to understand which year an employee is recruited and on-boarded into the organization. 

![Untitled](IOMETE%20-%20Tableau%20Integration%20529e31fe308f4194ac2164f96102e0da/Untitled%207.png)

Gender provides the details on which gender has been recruited during that period. 

![Untitled](IOMETE%20-%20Tableau%20Integration%20529e31fe308f4194ac2164f96102e0da/Untitled%208.png)

Then we need to add number of employees onboarded each year, such that count of the number of employees joined is put on a table. 

![Untitled](IOMETE%20-%20Tableau%20Integration%20529e31fe308f4194ac2164f96102e0da/Untitled%209.png)

Once the counts are there, then in Tableau a visualization can be chosen to present the report.

A nice looking dashboard presenting the information of required report. Tableau and IOMETE work together seamlessly, lets get connected to take your data analytics to next level.

![Untitled](IOMETE%20-%20Tableau%20Integration%20529e31fe308f4194ac2164f96102e0da/Untitled%2010.png)