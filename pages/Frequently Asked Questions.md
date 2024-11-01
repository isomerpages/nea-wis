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
<p>In order to download WIS 2.0 data, you will require an MQTT client. MQTT
explorer is one example of a free and readily available MQTT client which
can be downloaded from the <a href="https://mqtt-explorer.com/" rel="noopener noreferrer nofollow" target="_blank">MQTT Explorer website</a>.</p>
<p></p>
<p>Open MQTT Explorer and add a new connection to one of the Global Brokers.
As an example, we will connect to the Global Broker hosted by MeteoFrance
using the following details:</p>
<p></p>
<ul data-tight="true" class="tight">
<li>
<p>host: <a href="http://globalbroker.meteo.fr" rel="noopener noreferrer nofollow" target="_blank">globalbroker.meteo.fr</a>
</p>
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
</ul>
<p></p>
<p>Click on the 'ADVANCED' button, remove the pre-configured topics and add
the following topics to subscribe to:</p>
<p><strong>origin/a/wis2/sg-mss-asmc/data/recommended/#</strong>
</p>
<p></p>
<p>Click 'BACK', then 'SAVE' to save your connection and subscription details.
Then click 'CONNECT'. Messages will start appearing in your MQTT Explorer
as soon as new notification messages are available.</p>
</div>
</details>
<details class="isomer-details">
<summary></summary>
<div data-type="detailsContent" class="isomer-details-content">
<p>The MQTT protocol is used for all WIS2 publish-subscribe workflows (publication
and subscription). MQTT (Message Queuing Telemetry Transport) is a lightweight
messaging protocol designed for efficient communication in IoT and M2M
applications. MQTT uses a publish/subscribe model where clients publish
messages to topics and subscribe to topics to receive messages.</p>
<p></p>
<p>In order to download WIS 2.0 data, you will require an MQTT client. Some
readily available and free to use MQTT clients are MQTT explorer and MQTT.fx.
You will be required to enter the global broker's address and port, provide
credentials, and subscribe to the topics of interest.</p>
<p></p>
<p>For a tutorial on how to connect using MQTT explorer, please refer to
the following link: <a href="https://training.wis2box.wis.wmo.int/practical-sessions/connecting-to-wis2-over-mqtt/" rel="noopener noreferrer nofollow" target="_blank">Connecting to WIS2 over MQTT - WIS2 in a box training (wmo.int)</a>
</p>
</div>
</details>
<details class="isomer-details">
<summary><strong>What are some useful links?</strong>
</summary>
<div data-type="detailsContent" class="isomer-details-content">
<p>You may browse the technical documents and guides at the <a href="https://library.wmo.int/records?search=&amp;refine[Languages_EN][]=English&amp;refine[WMO_Programmes_EN][]=WMO+Information+System+%28WIS%29&amp;sort=_score&amp;perpage=10&amp;page=1&amp;&amp;page=1" rel="noopener nofollow" target="_blank">WMO Library</a> or
at the WIS2 <a href="https://github.com/wmo-im" rel="noopener nofollow" target="_blank">Github.</a>
</p>
<p></p>
<p>In addition the follow are the current WIS2 Global Services:</p>
<table style="minWidth: 100px">
<colgroup>
<col>
<col>
<col>
<col>
</colgroup>
<tbody>
<tr>
<td rowspan="1" colspan="1">
<p>Global Services</p>
</td>
<td rowspan="1" colspan="2">
<p>Country/Member</p>
</td>
<td rowspan="1" colspan="1">
<p>Website</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Global Broker</p>
</td>
<td rowspan="1" colspan="1">
<p>Australia</p>
</td>
<td rowspan="1" colspan="1">
<p>Melbourne</p>
</td>
<td rowspan="1" colspan="1">
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Global Broker</p>
</td>
<td rowspan="1" colspan="1">
<p>China</p>
</td>
<td rowspan="1" colspan="1">
<p>Beijing</p>
</td>
<td rowspan="1" colspan="1">
<p><a rel="noopener noreferrer nofollow" target="_blank">gb.wis.cma.cn</a>
</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Global Broker</p>
</td>
<td rowspan="1" colspan="1">
<p>France</p>
</td>
<td rowspan="1" colspan="1">
<p>Toulouse</p>
</td>
<td rowspan="1" colspan="1">
<p><a rel="noopener noreferrer nofollow" target="_blank">globalbroker.meteo.fr</a>
</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Global Broker</p>
</td>
<td rowspan="1" colspan="1">
<p>Germany</p>
</td>
<td rowspan="1" colspan="1">
<p>Offenbach</p>
</td>
<td rowspan="1" colspan="1">
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Global Broker</p>
</td>
<td rowspan="1" colspan="1">
<p>United States of America</p>
</td>
<td rowspan="1" colspan="1">
<p>Washington</p>
</td>
<td rowspan="1" colspan="1">
<p><a rel="noopener noreferrer nofollow" target="_blank">wis2globalbroker.nws.noaa.gov</a>
</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Global Cache</p>
</td>
<td rowspan="1" colspan="1">
<p>Australia</p>
</td>
<td rowspan="1" colspan="1">
<p>Melbourne</p>
</td>
<td rowspan="1" colspan="1">
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Global Cache</p>
</td>
<td rowspan="1" colspan="1">
<p>Germany</p>
</td>
<td rowspan="1" colspan="1">
<p>Offenbach</p>
</td>
<td rowspan="1" colspan="1">
<p><a rel="noopener noreferrer nofollow" target="_blank">https://opendata.dwd.de/test/wis2/cache/</a>
</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Global Cache</p>
</td>
<td rowspan="1" colspan="1">
<p>Japan</p>
</td>
<td rowspan="1" colspan="1">
<p>Tokyo</p>
</td>
<td rowspan="1" colspan="1">
<p><a rel="noopener noreferrer nofollow" target="_blank">https://wisdev.kishou.go.jp/data/wis2/</a>
</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Global Cache</p>
</td>
<td rowspan="1" colspan="1">
<p>Republic of Korea</p>
</td>
<td rowspan="1" colspan="1">
<p>Seoul</p>
</td>
<td rowspan="1" colspan="1">
<p><a rel="noopener noreferrer nofollow" target="_blank">https://wis2data.kma.go.kr/cache/a/wis2/</a>
</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Global Cache</p>
</td>
<td rowspan="1" colspan="1">
<p>United States of America</p>
</td>
<td rowspan="1" colspan="1">
<p>Washington</p>
</td>
<td rowspan="1" colspan="1">
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Global Discovery Catalogue</p>
</td>
<td rowspan="1" colspan="1">
<p>China</p>
</td>
<td rowspan="1" colspan="1">
<p>Beijing</p>
</td>
<td rowspan="1" colspan="1">
<p><a rel="noopener noreferrer nofollow" target="_blank">https://gdc.wis.cma.cn/dataService</a>
</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Global Discovery Catalogue</p>
</td>
<td rowspan="1" colspan="1">
<p>Canada</p>
</td>
<td rowspan="1" colspan="1">
<p>Ottawa</p>
</td>
<td rowspan="1" colspan="1">
<p><a rel="noopener noreferrer nofollow" target="_blank">https://api.weather.gc.ca/collections/wis2-discovery-metadata</a>
</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Global Discovery Catalogue</p>
</td>
<td rowspan="1" colspan="1">
<p>Republic of Korea</p>
</td>
<td rowspan="1" colspan="1">
<p>Seoul</p>
</td>
<td rowspan="1" colspan="1">
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Global Monitoring</p>
</td>
<td rowspan="1" colspan="1">
<p>Morocco</p>
</td>
<td rowspan="1" colspan="1">
<p>Casablanca</p>
</td>
<td rowspan="1" colspan="1">
<p>&nbsp;</p>
</td>
</tr>
</tbody>
</table>
<p></p>
</div>
</details>
</div>
<p></p>