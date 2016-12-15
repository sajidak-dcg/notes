# Plugins:
1. Manually sort folders
2. Profile Buttons
3. SmartTemplate4
4. Stationery
5. Super Date Format `%d-%b-%y %H:%M`

# Thunderbird Templates:

Settings to emulate outlook, and use personal preferences

## Reply:
```html
<hr><b>From:</b> %from% &lt;%from(mail)%&gt;
<br><b>Sent:</b> %X:=sent% %A%, %d% %B%, %Y% %H%:%M% %date_tz% (%tz_name(1)%)
[[<br><b>To:</b> %to(name,bracketMail(angle))%]][[<br><b>Cc:</b> %cc(name,bracketMail(angle))%]]
<br><b>Subject:</b> %subject%
<br>
```


## Forward:
```html
<hr><b>From:</b> %from% &lt;%from(mail)%&gt;
<br><b>Sent:</b> %X:=sent% %A%, %d% %B%, %Y% %H%:%M% %date_tz% (%tz_name(1)%)
[[<br><b>To:</b> %to(name,bracketMail(angle))%]][[<br><b>Cc:</b> %cc(name,bracketMail(angle))%]]
<br><b>Subject:</b> %subject%
```


## Other Settings: Select/Check these
- Use instead of [Disable] default quote header
- use HTML (e.g. <b>bold</b>)
- Replace line breaks with <br> (Uncheck after a restart, if untouched is treated as checked)

## Global Settings: Select/Check these
- Process Signature
- Add `--` in HTML mail
- Support Stationery addon
- Force Paragraph Mode


## Signature Text
```html
<div>
<br>Regards,
<br>FNAME.
<span class="mail-sig">
<br><b>Full Name</b>
<br>Mobile Number
</span>
</div>
```

## Stationery Template contents:
```html
<!DOCTYPE html>
<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
	<style>
		* {
			font-family: Calibri, "Noto Sans UI", "Lucida Sans Unicode", sans-serif;
		}
		.mail-sig{
			margin-left: 5px;
			padding-left: 5px;
			border-left: 1px solid #f61515;
			display: block;
		}
		blockquote.cite[type=cite]{
			margin: 0px !Important;
			padding: 0px !Important;
			border-width: 0px !Important;
		}
	</style>
</head>
<body>
	<div>
		<p>Dear %cursor%,</p>
		<p></p>
	</div>
	%sig(html)%
	<br>
	%quoteHeader%
	<br />
	%quotePlaceholder%
</body>
</html>
<!-- SmartTemplate4 Quote Header templates for Reply and Forward
<hr><b>From:</b> % from% &lt;% from(mail)%&gt;
<br><b>Sent:</b> % X:=sent% %A%, %d% %B%, %Y% %H%:%M% %date_tz% (%tz_name(1)%)
[[<br><b>To:</b> % to(name,bracketMail(angle))%]][[<br><b>Cc:</b> % cc(name,bracketMail(angle))%]]
<br><b>Subject:</b> % subject%
-->
```
