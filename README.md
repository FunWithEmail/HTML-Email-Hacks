 HTML-Email-Hacks
================

A series of HTML hacks for all those lovely Email clients out there.

This repo is a place to put all of the HTML Email hacks we all depend on so much to get our campaigns looking and feeling sweet and spiffy. 

---

##Click To Tap:
####   Change button text responsively
	
>@media screen and (max-width:600px) {<br>
>span[class=click] {display: none !important; max-height: 0 !important;}<br>
>span[class=tap]:after {content:”Tap”;}<br><br>

><a href=”#”&gt;<span class=”tap”&gt;<span class=”click”&gt;Click</span&gt;</span&gt; here</a&gt;

<em>-courtesy of Nicole Merlin</em>
  
##Kill Gmail App Zooming:
####	  Stop Gmail app from zooming text
	  
>style=”min-width:600px;”

<em>-courtesy of Chris Wise</em>
	 
##Target Webkit Clients:
####	  Webkit support is best support
	  
>@media screen and (-webkit-min-device-pixel-ratio:0) { }

<em>-courtesy of Kevin Mandeville</em>
  
##Margins and Float in Outlook:
####	  Use a capital “M” or “F”
	  
>style=”Margin: 20px; Float: left”

<em>-courtesy of Nicole Merlin</em>

##Interactive Email in Gmail:
####	No Class or ID selector support

Use lang as selector with "x-" prefix<br>
>\* [lang~="x-selector"] { }<br>
><div lang="x-selector"&gt;

<em>-courtesy of Justin at FreshInbox</em>

##Interactive Email con’t - Hover!:
####   Hover effect works on these clients:

Gmail: 
>\* [lang~="x-selector"]:hover { }

Outlook Web: 
>.class:hover

Yahoo! Web: 
>.class:hover

<em>-courtesy of Justin at FreshInbox</em>

##Outlook “View in Browser”:
#### 	Forces Outlook to provide a “view in browser link”

>\#outlook a {padding: 0;}

##Images in Outlook 2013:
#### 	Fix broken images in Outlook 2013

><td style=”line-height: 13px;”&gt;
	 <img src=”img.jpg”&gt;
></td&gt;

##Remove autolink styling in iOS:
#### 	Fix automatic styling of phone numbers, etc.

Use a span:
><span class=”appleLinksBlack”&gt;866-787-7030</span&gt;

<em>-courtesy of Justine Jordan</em>

##Stop some clients from stripping class:
#### 	Some clients strip any lines starting with “.”

Use a space before any class styling
> .selector { }

<em>-courtesy of Campaign Monitor http://kb.mailchimp.com/campaigns/ways-to-build/using-css-in-campaigns</em>

##Hide content in Office 365 (incl Webmail):
#### 	Office 365 strips display, mso-hide, mso conditional

Set font-size in containing cell to “0px”<br>
><td style=”font-size: 0px; display: none;&gt;

##Good formatting for bulleted list:
#### 	Stops bullet from sitting between two lines

><table&gt;  
>&nbsp;&nbsp;&nbsp;&nbsp;  <tr&gt;  
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;      <td valign=”top”&gt;&amp;bull;</td&gt;  
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;      <td&gt;Prolongs oil life</td&gt;  
>&nbsp;&nbsp;&nbsp;&nbsp;  </tr&gt;  
></table&gt;

<em>-courtesy of Michelle Klann</em>

##Ghost column to emulate "align" in Outlook
####	Outlook hates "align"; we love conditionals

><td&gt;  
>Table X  
><\!--[if mso]&gt;</td&gt;<td&gt;<![endif]--&gt;  
>Table Y  
></td&gt;  

<em>-courtesy of Jaina Mistry</em>

##Windows Phone media query and CSS3 support
####	Stripping out DOCTYPE defaults IE7 rendering on Windows Phone 8 and IE9 on Windows Phone 7. Let's use IE10!

><meta http-equiv="X-UA-Compatible" content="IE=edge" /&gt;

Note: Exchange ActiveSync based accounts do not benefit from forcing the document mode because the rendering engine is different (not IE), the doctype also gets preserved in this case.

<em> For more information see http://blog.jmwhite.co.uk/2014/08/19/email-campaigns-windows-phone-part-2-pop3-and-imap/</em>

<em>-courtesy of zerocents and James White</em>

##Fix mailto in Outlook.com
####	Outlook.com stops mailto from opening a new message

Add "target=_blank

><a href="#" target="_blank"&gt;Link</a&gt;

<em>-courtesy of Matthijs</em>

##Fix mailto in gmail
####	gmail strips subject and body from mailto links

Use lowercase for subject anbd body attribute

><a href="mailto:some_email@email.com?subject=A Subject&body=A Body"&gt;email@email.com</a&gt;

<em>-courtesy of SV</em>
