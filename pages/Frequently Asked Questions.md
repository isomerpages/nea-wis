---
title: Frequently Asked Questions
permalink: /faq/
variant: tiptap
description: ""
---
<h2>FAQ</h2>
<p></p>
<div data-type="detailGroup" class="isomer-accordion isomer-accordion-white">
<details class="isomer-details">
<summary><strong>How can I subscribe to and download the data through email?</strong>
</summary>
<div data-type="detailsContent" class="isomer-details-content">
<ol data-tight="true" class="tight">
<li>
<p>Complete the subscription form here: <a href="https://go.gov.sg/asmc-wis2-email-subscription-request-form" rel="noopener noreferrer nofollow" target="_blank">https://go.gov.sg/asmc-wis2-email-subscription-request-form</a>
</p>
</li>
</ol>
<p></p>
<ol start="2" data-tight="true" class="tight">
<li>
<p>Enter your details, ensuring your email address is correct.</p>
</li>
</ol>
<p></p>
<div class="isomer-image-wrapper">
<img style="width: 100%" height="auto" width="100%" alt="" src="/images/FAQ/FAQ_email_1.png">
</div>
<p></p>
<ol start="3" data-tight="true" class="tight">
<li>
<p>Select your desired topics for subscription and submit the form.</p>
</li>
</ol>
<p></p>
<div class="isomer-image-wrapper">
<img style="width: 100%" height="auto" width="100%" alt="" src="/images/FAQ/FAQ_email_2.png">
</div>
<p></p>
<ol start="4" data-tight="true" class="tight">
<li>
<p>Check your inbox for an email from Amazon Web Services. Click "Confirm
Subscription" in the email to finalise your subscription.</p>
</li>
</ol>
<p></p>
<div class="isomer-image-wrapper">
<img style="width: 100%" height="auto" width="100%" alt="" src="/images/FAQ/FAQ_email_3.png">
</div>
<p></p>
<ol start="5" data-tight="true" class="tight">
<li>
<p>You'll now receive email notifications when new data is available for
your chosen topics.</p>
</li>
</ol>
<p></p>
<p></p>
<div class="isomer-image-wrapper">
<img style="width: 100%" height="auto" width="100%" alt="" src="/images/FAQ/FAQ_email_4.png">
</div>
</div>
</details>
<details class="isomer-details">
<summary><strong>How can I subscribe to and download the data through an MQTT Client?</strong>
</summary>
<div data-type="detailsContent" class="isomer-details-content">
<ol data-tight="true" class="tight">
<li>
<p>In order to download WIS 2.0 data, you will require an MQTT client. MQTT
explorer is one example of a free and readily available MQTT client which
can be downloaded from the <a href="https://mqtt-explorer.com/" rel="noopener noreferrer nofollow" target="_blank">MQTT Explorer website</a>.</p>
<p></p>
</li>
<li>
<p>Open MQTT Explorer and add a new connection to one of the Global Brokers.
As an example, we will connect to the Global Broker hosted by MeteoFrance
using the following details:</p>
<ul data-tight="true" class="tight">
<li>
<p>host: globalbroker.meteo.fr</p>
</li>
<li>
<p>port: 8883</p>
</li>
<li>
<p>username: everyone</p>
</li>
<li>
<p>password: everyone</p>
</li>
<li>
<p>Turn off Validate Certificate</p>
</li>
<li>
<p>Turn on Encryption</p>
<div class="isomer-image-wrapper">
<img style="width: 100%" height="auto" width="100%" alt="" src="/images/FAQ/FAQ_email_6.png">
</div>
</li>
</ul>
</li>
<li>
<p>Click on the '<strong>ADVANCED</strong>' button, remove the pre-configured
topics and add the following topics to subscribe to:</p>
</li>
</ol>
<blockquote>
<p><strong>origin/a/wis2/sg-mss-asmc/#</strong>
</p>
<p><strong>origin/#</strong>
</p>
</blockquote>
<p></p>
<div class="isomer-image-wrapper">
<img style="width: 100%" height="auto" width="100%" alt="" src="/images/FAQ/FAQ_email_7.png">
</div>
<ol start="4" data-tight="true" class="tight">
<li>
<p>Click '<strong>BACK</strong>', then '<strong>SAVE</strong>' to save your
connection and subscription details. Then click '<strong>CONNECT</strong>'.
Messages will start appearing in your MQTT Explorer as soon as new notification
messages are available.</p>
</li>
</ol>
</div>
</details>
<details class="isomer-details">
<summary><strong>What are some useful links?</strong>
</summary>
<div data-type="detailsContent" class="isomer-details-content">
<p>You may browse the technical documents and guides at the <a href="https://library.wmo.int/records?search=&amp;refine[Languages_EN][]=English&amp;refine[WMO_Programmes_EN][]=WMO+Information+System+%28WIS%29&amp;sort=_score&amp;perpage=10&amp;page=1&amp;&amp;page=1" rel="noopener nofollow" target="_blank">WMO Library</a> or
at the WIS2 <a href="https://github.com/wmo-im" rel="noopener nofollow" target="_blank">Github</a>
</p>
<p></p>
</div>
</details>
</div>
<p></p>