# LR_Jmeter_Converter
LoadRunner to JMeter converter V1.1  is built on python2.7.


**How to use the converter:**

Download the zip file,
Unzip to any desired location.
Run “LR_Parsing.exe”
Provide absolute path to the Loadrunner script
Provide a location to save the logs and converted file.
Converted requests are saved to “converted_lines.log”
And the jmx is saved as output.jmx.

**NOTE: warning/Errors will be displayed on the console and will not be saved to file**

On successful conversion, arrange the requests as per the desired flow.

Note: correlation and text checks are added as a parent node to the request.
	Error handling will be improved in next versions.
	
**Known issues:**
1.	Multiple line post (web_custom_request) are converted with missing “” and extra “\”
2.	lr_start_transaction with "'" in the transaction name is throwing error
3.	rearranging the samples is still required

**Fixed issues:**

1.	path will be processed only if {url}://{servername:port} is present in the action of either web_submit_data or web_custom_request
2. 	web_reg_save_param is misinterpreted at times
3.	ordinal in web_reg_save_param_regex										
4. 	warning will be dispalyed if web_reg_find has save_count

**New features:**

1. 	web_submit_form, web_link are handelled	
2.	Creates If and while condition with "true" as condition										
3.	Reads complete Loadrunner file to process all the .c files 
4.	CSV dataset read will be created with param names and file linking


**Reach to Shravanakula@ymail.com for more details or enhancements**
	
