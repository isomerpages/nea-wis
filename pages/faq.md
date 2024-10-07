---
title: FAQ
permalink: /faq/
variant: tiptap
---
<h2>FAQ</h2>
<p></p>
<div data-type="detailGroup" class="isomer-accordion isomer-accordion-white">
<details class="isomer-details">
<summary><strong>What is WIS 2.0?</strong>
</summary>
<div data-type="detailsContent" class="isomer-details-content">
<p>WIS2 has been designed to meet the shortfalls of the current WIS and GTS,
support Resolution 1 (Cg-Ext(2021)) – WMO Unified Policy for the International
Exchange of Earth System Data (<em><a href="https://library.wmo.int/idurl/4/57850" rel="noopener noreferrer nofollow" target="_blank"><u>World Meteorological Congress: Abridged Final Report of the Extraordinary Session</u></a></em> (WMO-No.
1281)), support the Global Basic Observing Network (GBON) and meet the
demand for high data volume, variety, velocity and veracity.</p>
<p>WIS2 technical framework is based around three foundational pillars: leveraging
open standards, simpler data exchange and cloud-ready solutions.</p>
<p></p>
<p>For further information please visit the <a href="https://github.com/wmo-im" rel="noopener noreferrer nofollow" target="_blank">github.com/wmo-im</a>
</p>
</div>
</details>
<details class="isomer-details">
<summary><strong>What is MQTT and how to download data?</strong>
</summary>
<div data-type="detailsContent" class="isomer-details-content">
<p>MQTT (Message Queuing Telemetry Transport) is a lightweight messaging
protocol designed for efficient communication in IoT and M2M applications.
MQTT uses a publish/subscribe model where clients publish messages to topics
and subscribe to topics to receive messages.</p>
<p></p>
<p>In order to download the data, you will require an MQTT client or use
a programming library for your preferred language (e.g., Paho for Python
or Java). Some readily available MQTT clients are MQTT explorer and MQTT.fx.</p>
<p></p>
<p>You will be required to enter the global broker's address and port and
provide credentials if required.</p>
</div>
</details>
<details class="isomer-details">
<summary><strong>How to search the Global Discovery Catalogue to find datasets?</strong>
</summary>
<div data-type="detailsContent" class="isomer-details-content">
<p>The first step is to determine which dataset or datasets contains the
data that you need.</p>
<p></p>
<p>To do this, you may browse and search for discovery metadata, using keywords,
geographic area of interest, temporal information, or free text, provided
by the Global Discovery Catalogue. Discovery metadata follows a standard
scheme (see Manual on WIS, Volume II – Appendix F: WMO Core Metadata Profile).</p>
<p></p>
<p>A key component of dataset records in the Global Discovery Catalogue is
that of "actionable" links. A dataset record provides one to many links
that clearly identify the nature and purpose of the link (informational,
direct download, API, subscription) so that the data consumer can interact
with the data accordingly. For example, a dataset record may include a
link to subscribe to notifications (see below: How to subscribe to notifications
about the availability of new data) about the data, or an API, or an offline
archive retrieval service.</p>
<p></p>
<p>The Global Discovery Catalogue is accessible via an API and provides a
low barrier mechanism. Internet search engines are able to index the discovery
metadata in the Global Discovery Catalogue, thereby providing data consumers
with an alternative means to search for WIS2 data.</p>
</div>
</details>
<details class="isomer-details">
<summary><strong>How to subscribe to notifications about the availability of new data?</strong>
</summary>
<div data-type="detailsContent" class="isomer-details-content">
<p>WIS2 provides notifications about updates to datasets; for example, when
a new observation record from an automatic weather station is added to
a dataset of surface observations. Notifications are published on message
brokers. Where data consumers need to use data rapidly once it has been
published (such as input to a weather prediction model), they should subscribe
to one or more Global Broker to get notifications messages using Message
Queuing Telemetry Transport (MQTT) protocol.</p>
<p>In WIS2, notifications are republished by Global Brokers to ensure resilient
distribution. Consequently, there will be multiple places where one can
subscribe. Data consumers requiring real-time notifications must subscribe
to Global Brokers. A data consumer should subscribe to more than one Global
Broker, thereby ensuring that notifications continue to be received if
a Global Broker instance fails.</p>
<p>A dataset in WIS2 is associated with a unique <em>topic</em>. Notifications
about updates to a dataset are published to the associated topic. Topics
are organized according to a standard scheme (see the <em>Manual on WIS</em>,
Volume II - Appendix D: WIS2 Topic Hierarchy).</p>
<p>A data consumer can find the appropriate topic to subscribe to either
by searching the Global Discovery Catalogue, using an Internet search engine,
or by browsing the topic hierarchy on a Message Broker.</p>
<p>WIS2 uses Global Caches to distribute core data, as defined in the Unified
Data Policy (Resolution 1 (Cg-Ext (2021))). Each Global Cache republishes
core data on its own highly available data server and publishes a new notification
message advertising the availability of that data from the Global Cache
location.</p>
<p>Notifications from WIS2 Nodes and Global Caches are published on different
topics: The root topic used by WIS2 Nodes is <code>origin</code>, while
the root topic used by Global Caches is <code>cache</code>. Other than the
root, the topic hierarchy is identical. For example, for synoptic weather
observations published by Environment Canada:</p>
<ul>
<li>
<p>Environment and Climate Change Canada, Meteorological Service of Canada’s
WIS2 Node publishes to: <code>origin/a/wis2/ca-eccc-msc/data/core/weather/surface-based-observations/synop</code>
</p>
</li>
<li>
<p>Global Caches publish to: <code>cache/a/wis2/ca-eccc-msc/data/core/weather/surface-based-observations/synop</code>
</p>
</li>
</ul>
<p>As per clause 3.2.13 of the <em>Manual on WIS</em>, Volume II, data consumers
should access core data from the Global Caches. Consequently, they need
to subscribe to the <code>cache</code> topic hierarchy to receive the notifications
from Global Caches, each of which provides a link (that is, URL) to download
from the respective Global Cache’s data server.</p>
</div>
</details>
<details class="isomer-details">
<summary><strong>How to use a notification message to decide whether to download data?</strong>
</summary>
<div data-type="detailsContent" class="isomer-details-content">
<p>On receipt of a notification message, a data consumer needs to decide
whether to download the newly available data. The content of the notification
message provides the information needed to make this decision. For details
of the specification, see the <em>Manual on WIS</em>, Volume II - Appendix
E: WIS2 Notification Message.</p>
<p>In many cases, data consumers will use a software application to determine
whether or not to download the data. This section provides insight about
what happens.</p>
<p>When subscribing to multiple Global Brokers the data consumer will receive
multiple copies of a notification message. Each notification message has
a unique identifier, defined using the <code>id</code> property. Duplicate
messages should be discarded.</p>
<p>The core data will be available from both a WIS2 Node and Global Caches,
each of which publishes a different notification message advertising an
alternative location from where the data can be downloaded. Because these
are different messages, they will have different identifiers. However,
each of these messages refers to the same data object, which is uniquely
identified in the notification message using the data_id property. Notification
messages from different sources can easily be compared to determine if
they refer to the same data. By subscribing to the cache root topic, data
consumers will only receive notifications about data available from the
Global Caches. The origin root topic should be used when subscribing to
notifications about recommended data. Data consumers should not subscribe
to the origin root topic for notifications about core data because notification
messages provided on these topics will refer to data published directly
on the WIS2 Nodes (referred to as, the "origin").</p>
<p>Data consumers need to consider their strategy for managing these duplicate
messages. From a data perspective, it does not matter which Global Cache
instance is used – they will all provide an identical copy of the data
object published by the originating WIS2 Node. The simplest strategy is
to accept the first notification message and download it from the Global
Cache instance that the message refers to by using a URL for the data object
at that Global Cache instance. Alternatively, a data consumer may have
a preferred Global Cache instance, for example, that is located in their
region. Whichever Global Cache instance is chosen, data consumers will
need to implement logic to discard duplicate notification messages based
on <code>id</code> and duplicate data objects based on <code>data_id</code>.</p>
<p>A notification message also provides a small amount of metadata about
the data object it references such as location and time. Data consumers
can use this metadata to decide if the data object referenced in the message
should be downloaded. This is known as client-side filtering.</p>
<p>The notification message should also include the metadata identifier for
the dataset to which the data object belongs. A data consumer can use the
metadata identifier to search the Global Discovery Catalogue and discover
more about the data - in particular, whether there are any conditions on
the use of this data.</p>
</div>
</details>
</div>
<p></p>