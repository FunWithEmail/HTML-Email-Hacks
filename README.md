<h1> HTML-Email-Hacks </h1>
================

<p>A series of HTML hacks for all those lovely Email clients out there

This repo is a place to put all of the HTML Email hacks we all depend on so much to get our campaigns looking and feeling sweet and spiffy. </p>

<h2>Click To Tap:</h2>
<h3>   Change button text responsivly</h3>
	
<blockquote@media screen and (max-width:600px) {<br>
span[class=click] {display: none !important; max-height: 0 !important;}<br>
span[class=tap]:after {content:”Tap”;}<br>
<br>
<a href=”#”><span class=”tap”><span class=”click”>Click</span></span> here</a></blockquote>
  
<h2>Kill Gmail App Zooming:</h2>
<h3>	  Stop Gmail app from zooming text</h3>
	  
<blockquote>style=”min-width:600px;”</blockquote>
	 
<h2>Target Webkit Clients:</h2>
<h3>	  Webkit support is best support</h3>
	  
<blockquote>@media screen and (-webkit-min-device-pixel-ratio:0) { }</blockquote>
  
<h2>Margins and Float in Outlook:</h2>
<h3>	  Use a capital “M” or “F”</h3>
	  
<blockquote>style=”Margin: 20px; Float: left”</blockquote>

<h2>Interactive Email in Gmail:</h2>
<h3> 	No Class or ID selector support</h3>

<blockquote>* [lang~=”x-selector”] { }
<div lang=”x-selector”>
Use lang as selector with “x-” prefix</blockquote>

<h2>Interactive Email con’t - Hover!:</h2>
<h3>   Hover effect works on these clients:</h3>

<blockquote>Gmail - * [lang~=”x-selector”]:hover { }
Outlook Web - .class:hover
Yahoo! Web - .class:hover</blockquote>

<h2>Outlook “View in Browser”:</h2>
<h3> 	Forces Outlook to provide a “view in browser link”</h3>

<blockquote>#outlook a {padding: 0;}</blockquote>

<h2>Images in Outlook 2013:</h2>
<h3> 	Fix broken images in Outlook 2013</h3>

<blockquote><td style=”line-height: 13px;”>
	 <img src=”img.jpg”>
</td></blockquote>

<h2>Remove autolink styling in iOS:</h2>
<h3> 	Fix automatic styling of phone numbers, etc.</h3>

<h5>Use a span:
<blockquote><span class=”appleLinksBlack”>866-787-7030</span></blockquote>

<h2>Stop some clients from stripping class:</h2>
<h3> 	Some clients strip any lines starting with “.”</h3>

<h5>Use a space before any class styleing
<blockquote> .selector { }</blockquote>

<h2>Hide content in Office 365 (incl GM Webmail):</h2>
<h3> 	Office 365 strips display, mso-hide, mso conditional</h3>

<h5>Set font-size in containing cell to “0px”
<blockquote><td style=”font-size: 0px; display: none;></blockquote>

<h2>Good formatting for bulleted list:</h2>
<h3> 	Stops bullet from sitting between two lines</h3>

<blockquote><table>
	<tr>
		<td valign=”top”>&bull;</td>
		<td>Prolongs oil life</td>
	</tr>
</table></blockquote>
