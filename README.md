<div align="center">
  <img height="800" src="https://github.com/krmsmsk/Resimler/blob/main/SSIS/1695032965655.gif?raw=true"  />
</div>

###

<div align="center">
  <a href="https://www.linkedin.com/in/ali-kerem-simsek/" target="_blank">
    <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="40" alt="linkedin logo"  />
  </a>
</div>

###

<h1 align="center">Let's Talk About ETL</h1>

###

<p align="center">In this article, I will tell you shortly about ETL.</p>

###

<h3 align="left">ETL (Extract, Transform, Load) :</h3>

###

<p align="left">ETL stands for extract, transform, and load. First, the ETL tool extracts the data from different sources. Next, it changes the data according to specific business rules, formats, and conventions. For example, the ETL tool could convert all transaction values to US dollars, even if the sales were in other currencies. Finally, it loads the transformed data to the target system, such as a data warehouse.</p>

###

<h3 align="left">ELT (Extract, Load, Transform) :</h3>

###

<p align="left">ELT stands for extract, load, and transform. It is similar to ETL, except that ELT switches the final two data processes on the sequence. All the data is loaded in an unstructured data system, like a data lake, and transformed only when required. ELT takes advantage of cloud computing’s processing power and scalability to provide real-time data integration capabilities.</p>

###

<h3 align="left">Why is ETL important?</h3>

###

<p align="left">Today, we obtain data from many different sources. ETL processes are very important for the quality, integration, comprehensibility and interpretability of these data.</p>

###

<h3 align="left">How does ETL work?</h3>

###

<p align="left">Extract, transform, and load (ETL) works by moving data from the source system to the destination system at periodic intervals. The ETL process works in three steps:<br><br>1 - Extract the relevant data from the source database<br>2 - Transform the data so that it is better suited for analytics<br>3 - Load the data into the target database</p>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/SSIS/ETL.png?raw=true"  />
</div>

###

<h3 align="left">Basic data transformation</h3>

###

<p align="left">- Data cleansing<br>Data cleansing removes errors and maps source data to the target data format. For example, you can map empty data fields to the number 0, map the data value “Parent” to “P,” or map “Child” to “C.”<br><br>- Data deduplication<br>Deduplication in data cleansing identifies and removes duplicate records.<br><br>- Data format revision<br>Format revision converts data, such as character sets, measurement units, and date/time values, into a consistent format. For example, a food company might have different recipe databases with ingredients measured in kilograms and pounds. ETL will convert everything to pounds.</p>

###

<h3 align="left">Advanced data transformation</h3>

###

<p align="left">- Derivation<br>Derivation applies business rules to your data to calculate new values from existing values. For example, you can convert revenue to profit by subtracting expenses or calculating the total cost of a purchase by multiplying the price of each item by the number of items ordered.<br><br>- Joining<br>In data preparation, joining links the same data from different data sources. For example, you can find the total purchase cost of one item by adding the purchase value from different vendors and storing only the final total in the target system.<br><br>- Splitting<br>You can divide a column or data attribute into multiple columns in the target system. For example, if the data source saves the customer name as “Jane John Doe,” you can split it into a first, middle, and last name.<br><br>- Summarization<br>Summarization improves data quality by reducing a large number of data values into a smaller dataset. For example, customer order invoice values can have many different small amounts. You can summarize the data by adding them up over a given period to build a customer lifetime value (CLV) metric.<br><br>- Encryption<br>You can protect sensitive data to comply with data laws or data privacy by adding encryption before the data streams to the target database.</p>

###

<p align="left"></p>

###

<h3 align="center">٭ Let's make a small application with SSIS. Here I will just make a simple example to show how the system works. Even so, it will take some time to explain.</h3>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/SSIS/1.png?raw=true"  />
</div>

###

<p align="center">At first, the Control Flow Pane welcomes us. We have more to do with the Data Flow Pane. Let's get there quickly.</p>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/SSIS/2.png?raw=true"  />
</div>

###

<p align="center">The Toolbox contains the tools necessary for our ETL operations.</p>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/SSIS/3.png?raw=true"  />
</div>

###

<p align="center">Let's start by adding an excel source for our extraction and double-clicking on it.<br>And then we need to click New Excel connection manager.</p>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/SSIS/4.png?raw=true"  />
</div>

###

<p align="center">When we clicked New... then this page  will welcome us. We need to select a destination for our excel file in this page.</p>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/SSIS/5.png?raw=true"  />
</div>

###

<p align="center">when we clicked OK then we need to choose an excel sheet to process</p>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/SSIS/9.png?raw=true"  />
</div>

###

<p align="center">And then we can preview our data with click to Preview button.</p>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/SSIS/6.png?raw=true"  />
</div>

###

<p align="center">If we have more source like text file. We can add them too. I accidentally selected Destination in this image. I then changed it to Source.</p>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/SSIS/13.png?raw=true"  />
</div>

###

<p align="center">If we don't need to transform our any data, we can load them our database or any destination.<br>If we need to transform them, we should use a tool from transform pane which i show you.</p>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/SSIS/11.png?raw=true"  />
</div>

###

<p align="center">I used Conditional Split for split our data with a specific filter.</p>

###

<div align="center">
  <img height="600" src="https://github.com/krmsmsk/Resimler/blob/main/SSIS/10.png?raw=true"  />
</div>

###

<p align="center">When i open the conditional split, I saw Columns folder and some ready-made functions which created automatically.<br>Then i clicked Columns folder for giving a filter.<br>I selected City column and gave two filter on there.</p>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/SSIS/15.png?raw=true"  />
</div>

###

<p align="center">And then I load filtered data to two different destination.<br>The city name is Bothell and loaded into a table I created in the database.<br>The city name is Dallas and loaded into an excel file that I created.</p>

###

<h3 align="center">★ In this article, I tried to explain the concept of ETL with SSIS in a simple way. My goal is to help you understand these concepts more easily. I hope it was educational and instructive for you. ★</h3>

###
