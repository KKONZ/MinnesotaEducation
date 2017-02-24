# MinnesotaEducation
 Scraping data from MDE site
 _Home page for the data center_
 
http://w20.education.state.mn.us/MDEAnalytics/Data.jsp

Currently setup using:
* Mozilla Firefox version 51.0.1
* geckodriver version v0.14.0 found here https://github.com/mozilla/geckodriver/releases
* Selenium version 3.0.2
* Python 3.6

Use following code to setup executable
I had set the geckodriver.exe file in the system PATH but was still not being recognized in the Python wrapper so I added these lines of code:

ff = "C:/Users/karlk/geckodriver.exe"

driver = webdriver.Firefox(executable_path=ff)


## Drop Down list for Student data in jsp w20 link
http://w20.education.state.mn.us/ibi_apps/WFServlet?IBIF_ex=mdea_ddl_driver&TOPICID=2&DDL_VARS=4&NoCache=13.43.26

Updated local script, rolls up individual files.
TODO: find max value and data type for each column. Add those values to sql meta-table create scripts.
SQL will DROP table; CREATE table; each execution.
