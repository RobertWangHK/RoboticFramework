# RoboticFramework

# Installation Steps
- Step 1
Install robot framework
pip install robotframework
to uninstall : pip uninstall robotframework
- Step 2
Download and install wxPython from this  [link](https://sourceforge.net/projects/wxpython/files/wxPython/2.8.12.1/)
check with  : pip freeze  
```Because robotframework-ride relies solely on wxPython with version 2.8.?, have to download from the official website```
- Step 3 
Install RIDE
pip install robotframework-ride
- Step 4 
ride or ride.py

# Basic Test
- Step 1
Create New Project - Test Suite - TestCase
- Step 2
Download and add SeleniumLibrary Goto - http://robotframework.org/ - LIBRARIES - External - SeleniumLibrary 
- Step 3
Add Import - Library - SeleniumLibrary. If it shows in Black that means its successfully imported else not (in red)
- Step 4
Now in the TC if you start typing Selenium and ```ctrl+space``` it will show you all the keywords of SeleniumLibrary. You can use full name - SeleniumLibrary.Open Browser OR only action - OpenBrowser
| Open Browser  |  https://www.google.com | chrome |  
| Close Browser  |  
|  Log To Console | Complete successfully  |  
- Step 5
Add keywords and run, Add browser drivers from this [link](https://www.seleniumhq.org/download/), put it under the Python27 Script folder
- Step 6
Run and see Reports, add Setup/Teardown/Documentation under the Setting tag

# Console and Variables
- 1: Create a SCALAR variable for url and refer in TestCase
             syntax : ${VariableName}
- 2 : Create a LIST variable for username and password and refer in TestCase
              syntax : @{VariableName}
- 3 : Create a DICTIONARY variable for username and password and refer inTestCase
              syntax : &{VariableName}
- 4 : Environment variable %{variable name}
- 5 : Built-in variables: http://robotframework.org/robotframework/latest/RobotFrameworkUserGuide.html#built-in-variables
- 6 : Example
Open Browser	| ${url}	| chrome
Input Text	| id=txtUsername	| &{Login}[Username]
Input Text	| id=txtPassword	| &{Login}[Password]
clickButton	| id=btnLogin	
Close Browser |		
Log To Console	| %{username} run this test on %{os}
- 7 : Footnote
${url} variable
@{Credential} list variable
&{Login} dictionary variable
