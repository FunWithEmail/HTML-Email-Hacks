 HTML-Email-Hacks
================

A series of HTML hacks for all those lovely Email clients out there.

This repo is a place to put all of the HTML Email hacks we all depend on so much to get our campaigns looking and feeling sweet and spiffy. 

---

## Links and Helpful Tools

* Responsive Email Resources: www.ResponsiveEmailResources.com  
* Bulletproof Buttons: www.buttons.cm  
* Bulletproof Backgrounds: www.backgrounds.cm  
* HTML Email Boilerplate: http://htmlemailboilerplate.com  
* Special characters for HTML Email: http://www.emailonacid.com/character_converter/  
* Send HTML Email with Google Docs: http://www.labnol.org/internet/send-html-email/19672/
* SpamAssassin Spam Scores: http://spamassassin.apache.org/tests_3_0_x.html
* W3C HTML for email Community Group: http://www.w3.org/community/htmail/participants
* The Ultimate Guide to CSS: https://www.campaignmonitor.com/css/

---

## Click To Tap:
####   Change button text responsively

```css	
@media screen and (max-width:600px) {
	span[class=click] { display: none !important; max-height: 0 !important; }
	span[class=tap]:after { content:"Tap"; }
}
```
```html
<a href="#"><span class="tap"><span class="click">Click</span></span> here</a>
```

<em>-courtesy of Nicole Merlin</em>
  
## Kill Gmail App Zooming:
####	  Stop Gmail app from zooming text
	  
```html
style="min-width:600px;"
```
<em>-courtesy of Chris Wise</em>
	 
## Target Webkit Clients:
####	  Webkit support is best support
	  
```css
@media screen and (-webkit-min-device-pixel-ratio:0) { }
```

<em>-courtesy of Kevin Mandeville</em>
  
## Margins and Float in Outlook:
####	  Use a capital “M” or “F”
	  
```html
style="Margin: 20px; Float: left"
```

<em>-courtesy of Nicole Merlin</em>

## Interactive Email in Gmail:
####	No Class or ID selector support

Use lang as selector with "x-" prefix
```css
* [lang~="x-selector"] { }
```

```html
<div lang="x-selector"></div>
```

<em>-courtesy of Justin at FreshInbox</em>

## Interactive Email con’t - Hover!:
####   Hover effect works on these clients:

Gmail: 
```css
* [lang~="x-selector"]:hover { }
```

Outlook Web:
```css
.class:hover
```

Yahoo! Web: 

```css
.class:hover
```
<em>-courtesy of Justin at FreshInbox</em>

## Outlook “View in Browser”:
#### 	Forces Outlook to provide a “view in browser link”

```css
#outlook a { padding: 0; }
```

## Images in Outlook 2013:
#### 	Fix broken images in Outlook 2013

```html
<td style="line-height: 13px;">
	<img src="img.jpg" />
</td>
```

## Remove autolink styling in iOS:
#### 	Fix automatic styling of phone numbers, etc.

Use a span:
```css
.appleLinksBlack a { text-decoration:none !important; }
.appleLinksBlack a { color:#000000 !important; }
```
```html
<span class="appleLinksBlack">866-787-7030</span>
```
Add additional classes such as `.appleLinksWhite a`, `.appleLinksPink a` when appropriate

<em>-courtesy of Justine Jordan</em>

## Stop some clients from stripping class:
#### 	Some clients strip any lines starting with “.”

Use a space before any class styling
```css
 .selector { }
```

<em>-courtesy of Campaign Monitor http://kb.mailchimp.com/campaigns/ways-to-build/using-css-in-campaigns</em>

## Hide content in Office 365 (incl Webmail):
#### 	Office 365 strips display, mso-hide, mso conditional

Set font-size in containing cell to “0px”

```html
<td style="font-size: 0px; display: none;"></td>
```

## Good formatting for bulleted list:
#### 	Stops bullet from sitting between two lines

```html
<table>
	<tr>
		<td valign="top">&bull;</td>
		<td>Prolongs oil life</td>
	</tr>
</table>
```

<em>-courtesy of Michelle Klann</em>

## Ghost column to emulate "align" in Outlook
####	Outlook hates "align"; we love conditionals

```html
<td>
	Table X
	<!--[if mso]></td><td><![endif]-->
	Table Y
</td>
```

<em>-courtesy of Mike Ragan http://labs.actionrocket.co/make_mobile_email_work_in_outlook</em>

## Windows Phone 8 CSS3 support (IE Mobile)
####	Windows Phone 8 renders with IE7 standards by default with POP3/IMAP accounts

```html
<meta http-equiv="X-UA-Compatible" content="IE=edge" />
```

Note: Exchange ActiveSync based accounts do not benefit from forcing the document mode because the rendering engine is not IE Mobile.

<em> For more information see http://blog.jmwhite.co.uk/2014/08/19/email-campaigns-windows-phone-part-2-pop3-and-imap/</em>

<em>-courtesy of zerocents and James White</em>

## Fix mailto in Outlook.com
####	Outlook.com stops mailto from opening a new message

Add `"target=_blank"`

```html
<a href="#" target="_blank">Link</a>
```

<em>-courtesy of Matthijs</em>

## Fix mailto in gmail
####	gmail strips subject and body from mailto links

Use lowercase for subject and body attribute

```html
<a href="mailto:some_email@email.com?subject=A Subject&body=A Body">email@email.com</a>
```

<em>-courtesy of SV</em>

## Image gaps in Office 365 (OWA)
####	Office 365 strips display:block causing images to have massive gaps

Wrapping an image in a `<div>` with a height equal to the image height will simulate
a block element for clients that won't accept `display:block`.

```html
<div style="height:125px;">  
    <img src="/path/to/image.jpg" alt="Image Description" style="display:block;" width="200" height="125" />  
</div>
```

In some cases the addition of `font-size:0;` may be required in order to remove further gaps created by certain CSS properties set on the parent element i.e. table cell such as line-height.

Warning: Small font sizes can effect your spam score.

<em> For more information visit: http://www.emailonacid.com/blog/details/C13/two_fixes_for_image_spacing_in_outlook_web_app_owa</em>

<em>-courtesy of James White at http://blog.jmwhite.co.uk</em>
