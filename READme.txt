CONSTRAINTS:
-----------

- Ubuntu 14.04[Works on latest version of ubuntu as well]
- used python 2.7.12 
- used urllib module
- instructions of set up:
	- python : apt-get install python
	- urllib2 : apt-get install python-urllib2
	- xlwt : pip install xlwt -> this module is used for creating an excel sheet [Not Mandatory]
- Program will run in the latest linux machines.


DESCRIPTION OF HOW I APPROACHED THE PROBLEM:
-------------------------------------------

- Given 500 urls to check whether they are ecommerce sites or not.
- We can decide whether a particular site is ecommerce or not, by searching for the common words usually present in e-commerce sites such as CART, BUY , SELL , SHOPPING etc.
- Hence, parsing the urls given and checking whether those words present in that page.
- If present , printing as True, else printing as False.

- We can use few methods for parsing:
	- beautiful soup
	- urllib2
	- scrapy 

- No limitations in the solution. We can use many parsing modules like urllib2, beautiful soup, scrapy, wget etc.

- Used urllib2, I can  write in beautiful soup,scrapy etc as well. But using scrapy the disadvantage is we can't able to parse the link which doesn't exist. Few links of the 500 urls are invalid links which doesn't exist. As we need to write all 500 urls along with True or False, its not preffered.Hence used urllib2 module to parse and writing into file.

-Out of the 500 urls given, few we didn't get any response, they didn't exist. Hence, written them as 'No response' under E-commerce.

- Distinguishing whether a site as e-commerce or not is calculated using few common words. As we can't distinguish by any other parameters.
Guess no improvements required.  


CODING PART:

Writing into an excel file- ecommerce_script.py
-----------------------------------------
	Written separate functions in one class.
	used get_filenames function to get the output file.
	used program_headers function to print the headers in the excel file.
	main function where we are taking all the 500 links from the websites.txt file and passing it through urllib module for getting the response. If its ecommerce site, Am writing as 'True' into the sheet else 'False'

	

Steps to run the code:
----------------------
* In order to run the file use command "python ecommerce_script.py"
* Ensure the file "websites.txt" is included in the same directory.
* Once the Code execution is done, the output file "output.xls" is generated in the same directory.

