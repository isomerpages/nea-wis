---
title: Frequently Asked Questions
permalink: /faq/
variant: markdown
description: ""
---
<h2>FAQ</h2>
<p></p>
<div data-type="detailGroup" class="isomer-accordion isomer-accordion-white">
<details class="isomer-details">
<summary><strong>What is WIS2?</strong>
</summary>
<div data-type="detailsContent" class="isomer-details-content">
<p>Since the Global Telecommunication System (GTS) entered operational life
in 1971, it has been a reliable real-time exchange mechanism of essential
data for WMO Members.</p>
<p></p>
<p>In 2007, the WMO Information System (WIS) entered operations to complement
the GTS, providing a searchable catalogue and a Global Cache to enable
additional discovery, access, and retrieval. The success of WIS was limited
as the system only partially met the requirement of providing simple access
to WMO data. Today’s technology developed for the Internet of Things (IoT)
opens the possibility of creating a WIS2 able to stand to its expectations
of delivering an increasing number and volume of real-time data to WMO
centres in a reliable and cost-effective way.</p>
<p></p>
<p>WIS2 has been designed to meet the shortfalls of the current WIS and GTS,
support the WMO’s Unified Data Policy and the Global Basic Observing Network
(GBON), and meet the demand for high data volume, variety, velocity, and
veracity.</p>
<p></p>
<p>WIS2 technical framework is based around three foundational pillars: leveraging
open standards, simpler data exchange and cloud-ready solutions</p>
</div>
</details>
<details class="isomer-details">
<summary><strong>What are the components of WIS2?</strong>
</summary>
<div data-type="detailsContent" class="isomer-details-content">
<p></p>
<p><u>WIS2 Nodes</u>
</p>
<ul data-tight="true" class="tight">
<li>
<p>Data Collection or Production Centres (DCPCs) are centres that fulfil
within specific WMO Programmes an international responsibility for the
generation and provision for international distribution of data, forecast
products, processed or value-added information, and/or for providing archiving
services. ASMC is the DCPC for regional monitoring and alerting of transboundary
smoke haze.</p>
<p></p>
</li>
<li>
<p>National Centres (NCs) are responsible for collecting and providing observational
data and products intended for global or regional distribution to their
responsible GISC or DCPC, and distributing data on a national basis.</p>
</li>
</ul>
<p></p>
<p><u>Global Discovery Catalogue</u>: enables users to search all Datasets
provided by Data Publishers and discover where and how to interact with
those Datasets (e.g. subscribe to updates, access/download/visualize data,
or access more detailed information about the Dataset);</p>
<p></p>
<p><u>Global Broker</u>: provides highly available messaging services where
users may subscribe to notifications about all Datasets provided by Data
Publishers;</p>
<p></p>
<p><u>Global Cache</u>: provides highly available download service for cached
copies of Core data downloaded from Data Publishers’ Web-services;</p>
<p></p>
<p><u>Global Monitor</u>: gathers and displays system performance, data availability,
and other metrics from all WIS2 Nodes and Global Services</p>
</div>
</details>
<details class="isomer-details">
<summary><strong>What protocol does WIS2 use and how can I download the data?</strong>
</summary>
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
<p></p>
<p>In addition to the above, ASMC DCPC also provides an additional service
of supporting email subscription and download. You may browse our data
catalog and subscribe via the <a href="https://go.gov.sg/asmc-wis2-email-subscription-request-form" rel="noopener nofollow" target="_blank">email subscription link</a>.</p>
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