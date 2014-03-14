validator-
==========

Tinsoft Validator + Plugin

Tinsoft Validator + is a free Validation plugin From Tinsoft Developed by Tintu C Raju. This plugin helps programmers to validate web forms and reduce the time required to validate. With this validation plugin a programmer doesn’t need to write a single bit of code for validation. It is light weight so that performance will be affordable. We are currently managed to implement the basic validations. Hopefully we can add more features to plugin on next releases. This documentation will give brief detail about the plug in. For More Details Logon to : http://www.tintuweb.weebly.com or email me at tintumon18@gmail.com we are expecting your feedback and update requests which make this plug in more powerful.


Versions

 	Validator + is available on 2 versions 

1. Validator + version 1
This is the simplest version which is more fast. Which doesn’t require any css file to be imported. This will provide the balloon type error notification.
		Requirements
1. Jquery Minimum version
2. Validator.js	
2. Validator + version 2

	This is the pro version of the plug in. Which contain 2 kinds of error reporting. Which includes a stylish alert as well  as balloon type error notification. User can choose the required one by specifying it.

	Requirement
1. Jquery Minimum version
2. Validator.js
3. Alertify Plugin -> Which is embedded on validator
4. Validator CSS - > For the style
Properties

	Here will explain only about the properties of Validator + Version2. Some of the properties are not applicable for version 1.










Form Properties 
 
1. validation = “false” to disable validation for a form
Eg: <form id=”frm1” validation=”none”> </form>
2. color_css Property allows the user to highlight the element with a particular color when validation error occurs on that object. 
Eg: <form color_css=”true”></form>
3. error_color : property used to specify the highlight color 
Eg: <form color_css=”true” error_color=”red”></form>

Element Properties and Validations
 
1. By Default every field has been checked against empty validation. It will check whether a value in the input field was empty or not. 
2. req this property allows the programmer to disable validation for a particular field. By default a field is required to make it discard on validation. Use req=”false” this will skip validation for that elements
Eg: <input type=”text”  req=”false”>
3. title : This property allows the user to set a title for the element. This property is mandatory for the better error message display. Title is a valid user friendly name for a field instead of psudo names. Based on the title property error messages are displayed. 
Eg: <input type=”text”  title=”Username”>
If this field is missing then the error message will be like “Please enter a valid Username”
4. validation this property allows to specify the type of validation. There are many kinds of Validations available. 
Syntax 
	validation = “Type of validation required”
Eg: <input type=”text”  title=”E-mail Id”  validation=”mail”>



Different kinds validations are as follows.
1) num stands for the numeric validation. Which allow the user to enter only numeric values without floating point.
Eg: <input type=”text”  title=”Phone Number”  validation=”num”>
2) mail stands for the email validation. Which allow the user to enter only valid email id.
Eg: <input type=”text”  title=”E-mail Id”  validation=”mail”>
3) alpha stands for the alphabet only validation. Which allow the user to enter only alphabets (a-z A-Z) without space
Eg: <input type=”text”  title=”name”  validation=”alpha”>
4) alpha+s stands for the (alphabet and space) only validation. Which allow the user to enter only alphabets (a-z A-Z) with space
Eg: <input type=”text”  title=”name”  validation=”alpha+s”>
5) string allow the user to enter alphabets, numbers and special characters
Eg: <input type=”text”  title=”name”  validation=”string”>
6) alphanum stands for the alpha numeric only validation. Which allow the user to enter only alphabets and numbers  without space
Eg: <input type=”text”  title=”name”  validation=”alphanum”>
7) alphanum+s stands for the alpha numeric and space validation. Which allow the user to enter only alphabets and numbers  with space
Eg: <input type=”text”  title=”Alpha Numeric  Space” validation=”alphanum+s”>
8) ymd stands for the date validation with the format YYYY-MM-DD (which support / and - )
Eg: <input type=”text”  title=”Date Of Birth”  validation=”ymd”>
9) dmy stands for the date validation with the format DD-MM-YYYY (which support / and - )
Eg: <input type=”text”  title=”Date Of Birth”  validation=”dmy”>



10) mdy stands for the date validation with the format MM-DD-YYYY (which support / and - )
Eg: <input type=”text”  title=”Date Of Birth”  validation=”mdy”>
11) url stands for the URL validation which checks the validity of a url in the required field.
Eg: <input type=”text”  title=”Website Address”  validation=”url”>
Other Options or validation constrains are 
1. min  stands for the minimum length of the field.  This can be useful for setting minimum length for password fields.
Eg: <input type=”password”  title=”Password”  min=”6”>
Above Statement  means the password must contain atleast 6 characters. 
2. max  stands for the maximum length of the field..
Eg 1: <input type=” Password”  title=”Password”  max=”10”>
Both min and max or any other property can be used together.
Eg 2: <input type=” Password”  title=”Password”  min=”2” max=”5”>
Minimum Length is 2 and Maximum Length is 5

Eg 3: <input type=” text”  title=”PIN CODE”  min=”6” max=”6”>
Length should be exactly 6. Useful for PINCODE and Mobile validation

Both min and max can be used to specify the minimum options that a user can choose from checkbox group.

<input type=” checkbox”  name=” chkbrand”    title=”Brand”  min=”1” max=”2”> NOKIA
<input type=” checkbox”  name=” chkbrand”> NOKIA
<input type=” checkbox”  name=” chkbrand”> SAMSUNG
<input type=” checkbox”  name=” chkbrand”> LG
Explanation of above example is “Atleast choose 1 brand. Maximum 2 brands can be selected”



3. min-value  stands for the minimum value of the field..
Eg: <input type=”text”  title=”Age”  validation=”num” min-value=”18”>
It will accept numbers >= 18 only

4. max-value  stands for the Maximum value of the field..
Eg: <input type=”text”  title=”Age”  validation=”num” max-value=”80”>
It will accept numbers <= 80 only

Eg: <input type=”text”  title=”Age”  validation=”num” min-value=”18” 
max-value=”80”>
It will accept numbers between 17 and 81

Eg: <input type=”text”  title=”Age”  validation=”num” min-value=”18” 
max-value=”18”>
It will accept only the value 18 

5. confirm  used to confirm that the contents of two elements are the same. Which is mainly used in password and email confirmation. The procedure was simple we need to specify confirm =”id of the field to be compared” 
Eg: 
<input type=”text”  id=”pass”  title=”Password”  >
<input type=”text”    title=”Confirm Password”  confirm=”pass”   >
It will the compare the contents of confirm password with contents of 
password with id pass;






