<h1 align="center">
</h1>
<p align="center"> 
  <a href=""><img src="https://img.shields.io/static/v1?label=php&message=%3E=8.1&color=green&style=flat&logo=php"></a>
  <a href=""><img src="https://img.shields.io/static/v1?label=Platform&message=Linux/Windows&color=orange&style=flat"></a>
  <a href=""><img src="https://img.shields.io/static/v1?label=License&message=MIT&color=blue&style=flat"></a>
   <a href=""><img src="https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg?style=flat"></a>
</p>

# Thrly8-Finalersion
[Thrly8-Finalersion](https://Thrly8-Finalersion.com/) (SP in short) is a phishing toolkit for pentester or security professionals to enhance user awareness by simulating real-world phishing attacks. Thrly8-Finalersion helps to combine both phishing emails and phishing websites you created to centrally track user actions. The tool is designed in a view of performing professional phishing exercise and would be reminded to take prior permission from the targeted organization to avoid legal implications.

## Basic Requirements
* Operating System: Windows or Linux. The macOS support is not verified.
* Web Server: Any web server supporting PHP v8.1 or higher (for SP<=2.0, minimum requirement is PHP v7.4).
* Database: MySQL

## Installation
1. Clone this repo or download the latest release
2. Put the contents in your web root folder
3. Open installation page http://localhost/install in your browser and follow the steps
4. After installation, Thrly8-Finalersion will redirect to login page http://localhost/spear
>Default login - *Username: `admin`   Password: `sniperphish`*

## Main Features
* Web tracker code generation - track your website visits and form submissions independently
* Tracks data from phishing website containing any number of pages
* Create and schedule Phishing mail campaigns
* Combine your phishing site with email campaign for centrally tracking
* An independent "Quick Tracker" module for quick tracking an email or web page visit
* Advance report generation - generate reports based on the tracking data you needed
* Mail campaigns with QR/Bar code support (both locally and remotely embedding in mails)
* Track phishing message replies
* Signed and encrypted mail support
* Advanced mail campaign customization – read receipt, TO/CC/BCC emails etc.
* Anti-flood control for emails
* Non-ASCII (Punycode transcription) support for email and domain
* Auto-renaming attachments on-the-fly

## Creating Web-Email Campaign - Quick Guide
In short, we create web tracker -> Add the web tracker to the phishing website -> create mail campaign with a link pointing to the phishing website -> start mail campaign.
#### Creating a web tracker:
1. Design your website in your favorite programming language. Make sure you provided unique "id" and "name" value for HTML fields such as text field, checkbox etc.
2. Generate a web-tracker code `Web Tracker -> New Tracker` for your phishing site. The "Web Pages" tab lists the pages you want to track.
    * To track form submission data, provide the "id" or "name" values of HTML fields present in your phishing site form.
    * Repeat above for each page in your phishing site which is required to track.
3. From the final output, copy the generated JS link and place it in between &lt;Head&gt; and &lt;/Head&gt; section of each website page. This JS script contains the tracking code.
4. Finally, save the tracker created. Now the tracker is activated and listening in the background. Opening your phishing site pages or form submissions are tracked.

#### Creating an Email campaign:
1. Go to `Email Campaign -> User Group` and add target users 
2. Go to `Email Campaign -> Sender List` and configure Mail server details
3. Go to `Email Campaign -> Email Template` and create mail template. Here, you can to link your phishing website based on the web tracker you created. For that, click on `Insert` menu from email template editor and chose `Link to Web Tracker`. Select your web tracker from the pop-up window and insert it.
4. Now go to `Email Campaign -> Campaign List -> New Mail Campaign` and select/fill the fields to create the campaign.
5. Start Mail campaign

_Note: Thrly8-Finalersion tracks your phishing website only if the page is called by appending `rid` parameter (ie. `?rid={{RID}}`) at the end. For example opening `http://yourphishingsite.com/login?rid=abcd` will be tracked, but not `http://yourphishingsite.com/login`. Above 3rd step does this by default._

#### Viewing combined Web-Email Result
Go to `Web-MailCamp Dashboard -> Select Campaign`. Then select the web tracker and email campaign you created.<br/>

## More
* Thrly8-Finalersion website: https://Thrly8-Finalersion.com/
* Thrly8-Finalersion demo: https://demo.Thrly8-Finalersion.com/spear/
* Thrly8-Finalersion documentation: https://docs.Thrly8-Finalersion.com/
