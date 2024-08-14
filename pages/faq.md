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
</div>
</details>
<details class="isomer-details">
<summary><strong>How to search the Global Discovery Catalogue to find datasets?</strong>
</summary>
<div data-type="detailsContent" class="isomer-details-content">
<p>The first step to using data published via WIS2 is to determine which
dataset or datasets contains the data that is needed. To do this, a data
consumer may browse discovery metadata provided by the Global Discovery
Catalogue. Discovery metadata follows a standard scheme (see Manual on
WIS, Volume II – Appendix F: WMO Core Metadata Profile). A data consumer
may discover a dataset using keywords, geographic area of interest, temporal
information, or free text. Matching search results from the Global Discovery
Catalogue provide high-level information (title, description, keywords,
spatiotemporal extents, data policy, licensing, contact information), from
which a data consumer can assess and evaluate their interest in accessing/downloading
data associated with the dataset record.</p>
<p>A key component of dataset records in the Global Discovery Catalogue is
that of "actionable" links. A dataset record provides one to many links
that clearly identify the nature and purpose of the link (informational,
direct download, API, subscription) so that the data consumer can interact
with the data accordingly. For example, a dataset record may include a
link to subscribe to notifications (see below: How to subscribe to notifications
about the availability of new data) about the data, or an API, or an offline
archive retrieval service.</p>
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
<details class="isomer-details">
<summary><strong>How to download data?</strong>
</summary>
<div data-type="detailsContent" class="isomer-details-content">
<p>Links to where data can be accessed are made available through dataset
discovery metadata (via the Global Discovery Catalogue) and/or data notification
messages (via Global Brokers). Links can be used to directly download the
data (according to the network protocol and content description provided
in the link) using a mechanism appropriate to the workflow of the data
consumer. This could include web and/or desktop applications, custom tooling,
or other approaches.</p>
<p>A discovery metadata record or notification message may provide more than
one download link. The preferred link will be identified as "canonical"
(link relation: "rel": "canonical").</p>
<p>Where data is provided through an interactive web service, a canonical
link that provides a URL where one can directly download a data object
may be complemented with an additional link providing the URL for the root
of the web service from where one can interact with or query the entire
dataset.</p>
<p>If a download link implements access control (for example, the data consumer
needs to take some additional action(s) to download the data object), the
download link will contain a security object that provides the pertinent
information (such as the access control mechanism used and where/how a
data consumer would need to register to request access).</p>
</div>
</details>
<details class="isomer-details">
<summary><strong>How to use the data?</strong>
</summary>
<div data-type="detailsContent" class="isomer-details-content">
<p>Data is shared on WIS2 in accordance with the Unified Data Policy (Resolution
1 (Cg-Ext (2021))). This data policy describes two categories of data:
core and recommended.</p>
<ul>
<li>
<p>Core data is considered essential for the provision of services for the
protection of life and property and the well-being of all nations. Core
data is provided on a free and unrestricted basis, without charge and with
no conditions on use.</p>
</li>
<li>
<p>Recommended data is exchanged on WIS2 in support of Earth system monitoring
and prediction efforts. Recommended data <em>may</em> be provided with conditions
on use and/or subject to a license.</p>
</li>
</ul>
<p>Furthermore, the Unified Data Policy (Resolution 1 (Cg-Ext (2021))) encourages
attribution of the source of the data in all cases. In this way, credit
is given to those who have expended effort and resources in collecting,
curating, generating, or processing the data. Attribution provides visibility
of who is using data which, for many organizations, provides necessary
evidence to justify continued provision of and updates to the data.</p>
<p>Details of the applicable WMO data policy and any rights or licenses associated
with data are provided in the discovery metadata that accompanies the data.
Discovery metadata records are available from the Global Discovery Catalogue.</p>
<p>The <em>Manual on WIS</em>, Volume II – Appendix F: WMO Core Metadata Profile,
section 1.18 Properties / WMO data policy provides details on how data
policy, rights and/or licenses are described in the discovery metadata.</p>
<p>When using data from WIS2, data consumers:</p>
<ul>
<li>
<p>Shall respect the conditions of use applicable to the data as expressed
in the WMO data policy, rights statements, or licenses.</p>
</li>
<li>
<p>Should attribute the source of the data.</p>
</li>
</ul>
</div>
</details>
<details class="isomer-details">
<summary><strong>Further reading for data consumers</strong>
</summary>
<div data-type="detailsContent" class="isomer-details-content">
<p></p>
</div>
</details>
<details class="isomer-details">
<summary></summary>
<div data-type="detailsContent" class="isomer-details-content">
<p></p>
</div>
</details>
</div>
<p></p>