<div align="center">

## The Daily Newbie \- Using the Chr\(\) function


</div>

### Description

To show the usage of the Chr() function.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Matthew Roberts](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/matthew-roberts.md)
**Level**          |Beginner
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0, VB Script, ASP \(Active Server Pages\) , VBA MS Access, VBA MS Excel
**Category**       |[Coding Standards](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/coding-standards__1-43.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/matthew-roberts-the-daily-newbie-using-the-chr-function__1-22805/archive/master.zip)





### Source Code

<html>
<head>
<meta http-equiv="Content-Type"
content="text/html; charset=iso-8859-1">
<meta name="GENERATOR" content="Microsoft FrontPage Express 2.0">
<title>Daily Newbie - 04/29/2001</title>
</head>
<body bgcolor="#FFFFFF">
<p> </p>
<p class="MsoTitle"><img width="100%" height="3"
v:shapes="_x0000_s1027"></p>
<p align="center" class="MsoTitle"><font size="7"><strong>The
Daily Newbie</strong></font></p>
<p align="center" class="MsoTitle"><strong>&#8220;To Start Things
Off Right&#8221;</strong></p>
<p align="center" class="MsoTitle"><font size="1">Fourth
Edition                   
                                     
April 28,
2001                      
                                                  
Free</font></p>
<p align="center" class="MsoTitle"><img width="100%" height="3"
v:shapes="_x0000_s1027"></p>
<p align="center" class="MsoNormal" style="text-align:center"> </p>
<p align="center" class="MsoNormal" style="text-align:center"> </p>
<p class="MsoNormal"><font face="arial">Today's command, Chr() is almost a must-know for a lot of string manipulation and should be one of the fundimental tricks in your VB coding bags. If you have read the previous Newbie articles, you already know about the <a href="http://www.planetsourcecode.com/vb/scripts/ShowCode.asp?txtCodeId=22745&blnEditFeedback=TRUE&lngWId=1">Asc() function</a>. The Chr() function is a compliment of it. While the Asc() Function returns an ASCII code for a character, the Chr() function returns a character for an ASCII character.</font></p>
<p class="MsoNormal"><font size="2" face="Arial"></font></p>
<p class="MsoNormal" style="margin-left:135.0pt;text-indent:-135.0pt"><font size="2"
face="Arial"><strong>Today&#8217;s Keyword:</strong>
                             </font><font
size="4" face="Arial"> Chr()</font></p>
<p class="MsoNormal"
style="margin-left:135.0pt;text-indent:-135.0pt"><font size="2"
face="Arial"><strong>Name Derived
From:        </strong>
<font size="2" face="Arial"><strong>Character - </strong> a symbol (as a letter or number) that represents information; also : a representation of such a character that may be accepted by a computer - <em><a href="http://www.webster.com/">Webster's online
  dictionary.</a></em></font></p>
<p class="MsoNormal"
style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
margin-left:135.0pt;text-indent:-135.0pt"><font
size="2" face="Arial"><strong>Used for   </strong>                               
Converting an ASCII character to a string character.</font></p>
<p class="MsoNormal"
style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
margin-left:135.0pt;text-indent:-135.0pt"><font
size="2" face="Arial"><strong>VB Help Description: </strong>            Returns a String containing the character associated with the specified character code.
</font></p>
<p class="MsoNormal"
style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
margin-left:135.0pt;text-indent:-135.0pt"><font
size="2" face="Arial"><strong>Plain
English:    </strong>                       Takes a <a href="http://www.orst.edu/aw/tutorials/html/ascii-chart.html">ASCII Character code </a>and converts it to a "normal" text character. </font></p>
<p class="MsoNormal"
style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
margin-left:135.0pt;text-indent:-135.0pt"><font
size="2" face="Arial"><strong>Syntax:       </strong>                              Chr(ASCII Code)</font></p>
<p class="MsoNormal"
style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
margin-left:135.0pt;text-indent:-135.0pt"><font
size="2" face="Arial"><strong>Usage:       </strong>                               strCharacter =Chr(65)
 </font></p>
<p class="MsoNormal"
style="margin-left:135.35pt;text-indent:-135.35pt"><font size="2"
face="Arial"><strong>Copy & Paste Code:</strong></font></p>
<br>
<br>
Today's code snippet will print a list of ACII codes and their equivilent character values in the debug window.
<br>
<br>
<pre>
			Dim intASCII As Integer
			For intASCII = 49 To 122
				Debug.Print Chr(intASCII)
			Next intASCII
</pre>
 <p class="MsoNormal"
 style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
margin-left:135.0pt;text-indent:-135.0pt"> </p>
<p class="MsoNormal"
style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
margin-left:135.0pt;text-indent:-135.0pt"><font
size="2" face="Arial"><strong>Notes: </strong></p>
The reason that the Chr() function is so important is that a lot of things in Visual Basic as based on
ASCII values. For example, in the KeyPress() event of an object, the value that is passed in as the pressed
key is an ASCII value. If you are wanting to display each character on the keypress event, you can do it with this code:
<pre>
		Private Sub Form_KeyPress(KeyAscii As Integer)
			MsgBox Chr(KeyAscii)
		End Sub
</pre>
 Since the KeyAscii is a VB-defined parameter, the ability to convert it to a character value is pretty important. Chr() Makes this simple. I used Chr() in a simple "word scrambling" project that you can view
 by <a href="http://www.planetsourcecode.com/xq/ASP/txtCodeId.8373/lngWId.1/qx/vb/scripts/ShowCode.htm">clicking here.</a>
<br><br>
<br><br>
Tomorrow's Keyword:			Command()
</font></p>
</body>
</html>

