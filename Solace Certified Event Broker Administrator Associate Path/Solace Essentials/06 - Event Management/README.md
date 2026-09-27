---
title: "Event Management"
document_type: lesson
learning_path: "Solace Certified Event Broker Administrator Associate Path"
course: "Solace Essentials"
lesson_order: 6
source: Solace Academy
---

# Event Management

- **Course:** Solace Essentials
- **Syllabus order:** 06
## LMS update on opening Event Management


### Event Management SCORM launch screen

The lesson opens with its title and a Start link. The instructions say to navigate between steps with the up and down arrow keys or the step controls on subsequent screens.

### Event Management screen 1 of 5 - Lesson Objectives

The objectives are to understand the basics of Message VPNs; understand authentication and authorizations for client applications; introduce the available management tools; and get started with each tool by configuring various options.

### Event Management screen 2 of 5 - Message VPNs and Messaging Applications

The lesson compares Message VPNs to virtual machines: multiple virtual machines share one server, while Message VPNs decouple messaging functionality from the equipment delivering it. They allow a single PubSub+ Event Broker to be shared while keeping messaging data separate and partitioning resources.

The “Messaging Applications” example contrasts dedicated infrastructure for each application-which requires separate network access, storage, security, APIs, and administration-with a shared broker design. A Trading Platform and an Online Store each need development environments. The Middleware Team manages administrator accounts, equipment utilization, and environment setup, with global admin and read/write access to both applications. The Application Support Team handles configuration changes and monitoring, with global read-only monitoring/troubleshooting and read/write access to both Message VPNs. Application Developers monitor development environments but do not change configuration. The lesson's proposed design reuses one Event Broker with two isolated development Message VPNs, one per application.

The visible illustration depicts a shared appliance split into four secured VPN areas; the text identifies the key benefits as data separation and resource partitioning. Scroll page down is available for the rest of the screen.

### Event Management screen 2 of 5 - lower Messaging Applications content

The lower screen says that without virtualization, each messaging application runs on dedicated servers and needs its own network access, storage, and security. Developers may work with different APIs, and administrators must monitor and manage each individual environment, increasing operational complexity and administrative burden. The accompanying illustration shows a Solace broker with multiple VPNs and separate infrastructure icons beneath them. A Zoom image control is present.

### Event Management screen 2 of 5 - zoomed Message VPN diagram

The zoomed infographic shows four separate, lock-marked VPN spaces inside one Solace broker, reinforcing the shared-broker illustration. The image modal has an Unzoom image control.

### Event Management screen 2 of 5 - diagram restored

The zoom modal is closed, returning to the lower Messaging Applications view with the dedicated-infrastructure explanation and its diagram visible again. The Scroll page down control remains available.

### Event Management screen 2 of 5 - full dedicated-resource illustration

The lower portion of the illustration is visible: four secured VPNs each connect to a different resource icon, including a server with a gear, a layered/storage-like symbol, a computer/network service, and a database. This reinforces the separation of application infrastructure under dedicated deployment. The Scroll page down control remains available.

### Event Management screen 2 of 5 - Middleware Team example

The scrolled scenario introduces a Trading Platform and an Online Store, each needing a development environment. The Middleware Team controls administrator accounts, equipment utilization, and environment setup, with global administrator and read/write access to both applications. An illustrative image accompanies this role description; the Application Support Team section begins below it.

### Event Management screen 2 of 5 - support and developer roles

The Application Support Team manages configuration changes and monitoring. It has global read-only access for monitoring and troubleshooting, plus read/write access to both Message VPNs. Application Developers monitor development environments but do not make configuration changes. The lower edge of the screen begins the proposed shared-broker arrangement.

### Event Management screen 2 of 5 - isolated development VPN design

The final screen recommends reusing one Event Broker and configuring two separate development Message VPNs, one for the Trading Platform and one for the Online Store, to provide isolated environments for both. The illustration places the two applications in separate locked VPN areas inside one Solace broker. The page is at its bottom: Scroll page down is disabled and Go to next step is available.

### Event Management screen 3 of 5 - Client Authentication and Authorization

Message VPNs are isolated environments, so each has its own client-authentication configuration. Authentication verifies that clients are who they claim to be. The lesson lists Basic authentication, Client Certificate, and Kerberos. Under “Basic Authentication,” four collapsed accordions are shown: None, Internal, RADIUS, and LDAP.

The “Client Object Model” says that client messaging connections require a Message VPN, a client username for authentication, a client profile for access to configurable resources and capabilities, and an ACL profile for authorization.

A client username is Message VPN-specific and used by client applications to authenticate. A username can support multiple client connections for horizontal scaling. Disabling it disconnects all clients connected through it. Each username is associated with a client profile and ACL profile.

Every Message VPN has a built-in “default” username that cannot be deleted and has assigned client and ACL profiles. If a client uses a username that does not exist on the broker, the default username is used; this can support external authentication such as LDAP or RADIUS without creating a broker username for every person. It is enabled automatically on software brokers, but should remain shut down in production unless explicitly needed; it can be useful in development and testing when authentication is disabled.

Client profiles are Message VPN-specific, can be shared across multiple usernames, and govern behavior such as maximum connections per username, TCP connection tuning, guaranteed-messaging capabilities, and event thresholds. A default client profile is pre-created on each Message VPN.

ACL profiles can likewise be shared across usernames to manage entitlements. Their Access Control Lists allow or restrict client actions, including client connections by IP address and topics that a client can publish or subscribe to. Each ACL definition has a default allow/disallow action plus exceptions, allowing whitelist- or blacklist-style rules.

Two CLI examples are shown. Client-connect example: `show acl-profile AP-1 message-vpn VPN-1 detail` has default action `disallow` and allows exceptions `192.168.1.0/24` and `192.168.2.200/32`. Publish-topic example: the same command shows default action `allow` with exception `system/host1/>`, which is therefore not allowed.

The visible Basic Authentication accordion headings are recorded above; their contents are still collapsed. Scroll page down is available.

### Event Management screen 3 of 5 - Basic Authentication: None

The “None” accordion says this method still requires a username at login but no password. It is the least secure option and should only be used for training and development. The accordion is expanded; Internal, RADIUS, and LDAP remain to inspect.

### Event Management screen 3 of 5 - Basic Authentication: Internal

The “Internal” accordion says the client must provide a username and password, and the credentials are stored on the PubSub+ Event Broker itself. The None and Internal accordions have been inspected; RADIUS and LDAP remain.

### Event Management screen 3 of 5 - Basic Authentication: RADIUS

The “RADIUS” accordion says users are authenticated through provisioned RADIUS servers using the configured RADIUS profile name. The panel also exposes a zoomable illustration. LDAP remains to inspect.

### Event Management screen 3 of 5 - Basic Authentication: LDAP

The “LDAP” accordion says clients can be authenticated using provisioned LDAP servers. All four Basic Authentication options are now recorded: None, Internal, RADIUS, and LDAP.

### Event Management screen 3 of 5 - Client Object Model diagram

The scrolled screen displays the end of the LDAP panel and the Client Object Model section. Its diagram shows a client username linked to both a client profile and an ACL profile inside a secured Message VPN. The adjacent text says that messaging clients require four managed objects: a Message VPN, client username, client profile, and ACL profile. A zoom control is available for the diagram.

### Event Management screen 3 of 5 - zoomed Client Object Model diagram

The zoomed diagram shows a client username at the bottom with arrows to both a client profile and an ACL profile, all within one secured VPN. It confirms that the username is the connection point associated with both profiles.

### Event Management screen 3 of 5 - Client Username details

The Client Username section lists five properties: usernames belong to a specific Message VPN; client applications use them to authenticate; one username can serve multiple connections for horizontal scaling; disabling a username disconnects its active clients; and each username is associated with a client profile and an ACL profile for authorization. The Scroll page down control remains available.

### Event Management screen 3 of 5 - Client Username: default

Every Message VPN contains an undeletable “default” username with its own client and ACL profiles. The illustration compares VPN-1, which contains a provisioned username “CU-1” plus “default,” with VPN-2, which shows “default.” If a client supplies a username that is not provisioned, the broker uses “default,” enabling external LDAP or RADIUS authentication without creating broker usernames for every user. The lesson warns that this built-in username is enabled automatically on software brokers and should be shut down in production when not explicitly used; it may be useful in development/testing where authentication is disabled. The page continues below the viewport.

### Event Management screen 3 of 5 - Client Profile

Client profiles belong to one Message VPN and can be assigned to zero or more usernames. Sharing a profile helps administrators manage groups without changing each username individually. Profiles control behaviors and capabilities such as resource allocation (including maximum connections for one username), TCP connection tuning, guaranteed-messaging capabilities, and event thresholds. A default client profile is pre-created on every Message VPN. The diagram shows three usernames sharing one client profile. A Zoom image control is available.

### Event Management screen 3 of 5 - zoomed default-username diagram

The zoomed diagram shows a client presenting username “CU-1” to VPN-1, where “CU-1” and “default” both exist, and another client presenting “CU-1” to VPN-2, where only “default” is shown. It visually reinforces use of the default username when the supplied username is not provisioned in that VPN.

### Event Management screen 3 of 5 - lower Client Profile details

The continued Client Profile view shows the shared profile “CP-1” linked to multiple usernames within VPN-1. The text reiterates that profiles group client behavior and resource limits; visible examples include per-username connection limits and TCP tuning, with guaranteed-messaging capabilities listed below. Continue down for the default-profile note and ACL material.

### Event Management screen 3 of 5 - Client Profile default and ACL Profile

A default client profile is pre-created on every Message VPN. ACL profiles are also Message VPN-specific and can be applied to zero or more usernames, allowing administrators to manage entitlements for groups. Their ACLs allow or restrict client behavior, including connections by IP address and publish/subscribe access to topics. Each ACL has a default allow/disallow action and exceptions, supporting whitelist- or blacklist-style rules. The diagram shows usernames CU-1, CU-2, and CU-3 sharing ACL profile AP-1. A Zoom image control is available.

### Event Management screen 3 of 5 - zoomed ACL Profile diagram

The enlarged diagram shows client usernames CU-1, CU-2, and CU-3 in VPN-1 all pointing to one ACL profile, AP-1. It illustrates shared authorization rules within the Message VPN.

### Event Management screen 3 of 5 - ACL Profile Client Connect example

The example gives AP-1 in VPN-1 a default client-connect action of `disallow`, with exceptions for `192.168.1.0/24` and `192.168.2.200/32`; matching connections are allowed. The accompanying CLI output is from `show acl-profile AP-1 message-vpn VPN-1 detail`. The Publish Topic example begins below.

### Event Management screen 3 of 5 - ACL Profile Publish Topic example and end of step

The Publish Topic example gives AP-1 in VPN-1 a default action of `allow` for published topics, except `system/host1/>`, which is not allowed. The `show acl-profile AP-1 message-vpn VPN-1 detail` output shows this one exception. Scroll page down is disabled at the bottom and Go to next step is available.

### Event Management screen 4 of 5 - Management Tools

The screen says PubSub+ Cloud Console offers an evolving single view of the Solace ecosystem and can deploy/manage brokers anywhere. For configuring objects inside an already deployed broker, the available tools are PubSub+ Broker Manager, SEMP, and CLI.


The “How to Access PubSub+ Broker Manager” tabs are PUBSUB+ CLOUD, PUBSUB+ SOFTWARE AND APPLIANCE, and OAUTH. The selected Cloud tab says to open Cluster Manager in the Cloud Console, select a broker service, then choose “Open PubSub+ Broker Manager” at the service’s top right.

SEMP v2 is described as a RESTful, programmable API for configuring brokers, complementing CLI and Broker Manager and supporting provisioning, operations, and maintenance anywhere. In “SEMP API URLs and Access,” the selected PUBSUB+ CLOUD tab says to open the cloud messaging service, choose Manage, and use the SEMP – REST API section for access details and tutorials. Another tab covers Software and Appliance brokers.

The CLI is a text-based interface for broker configuration, monitoring, administration, provisioning, and network troubleshooting. It starts when the broker powers up, is accessed over SSH, and is mainly used with Software or Appliance brokers. Both Cloud tabs are selected by default; alternate access tabs remain to inspect. Scroll page down is available.

### Event Management screen 4 of 5 - Broker Manager for Software and Appliance

The selected tab says to open a browser and enter the broker address. HTTP uses `http://<your-Solace PubSub+ software event broker's-address>:8080` (port 80 for an Appliance); HTTPS uses `https://<your-Solace PubSub+ software event broker's-address>:1943` (port 443 for an Appliance). These are generic course examples, not actual targets.

### Event Management screen 4 of 5 - Broker Manager OAuth

The OAuth tab says OAuth can be configured to let Broker Manager users sign in through an OAuth provider. Once enabled, the login screen shows an additional button for each configured provider. Selecting a button redirects to that provider and returns the user to Broker Manager; an existing provider session leads to an immediate return. A Broker Manager login-screen illustration appears below the explanation.

### Event Management screen 4 of 5 - zoomed Broker Manager OAuth screen

The zoomed illustration is a Broker Manager login form with username/password login and a separate “Login with OAuth” button highlighted below an “OR” divider. It visually matches the described provider sign-in option.

### Event Management screen 4 of 5 - SEMP API for Software and Appliance

The selected SEMP access tab says to use the same IP address used for PubSub+ Broker Manager and add `/SEMP/v2/config`. Its examples are `http://<your-broker-ip>:8080/SEMP/v2/config` (port 80 for an Appliance) and `https://<your-broker-ip>:943/SEMP/v2/config` (port 443 for an Appliance). These are generic instructional URLs, not a target broker.

### Event Management screen 4 of 5 - CLI and end of Management Tools

The final section describes CLI as a text-based interface for configuring and monitoring brokers, administration, provisioning, and network troubleshooting. It starts when an event broker powers up, is accessed through SSH, and is mainly used with Software and Appliance brokers. A terminal illustration shows broker-management output, including Message VPN status. The page is at its bottom: Scroll page down is disabled and Go to next step is available.

### Event Management screen 4 of 5 - zoomed CLI terminal illustration

The enlarged terminal sample shows `show message-vpn *`, listing the `bridgedemo` and `default` Message VPNs as Up, with subscription and local-connection counts. A subsequent `show` command displays a list of available CLI object/configuration areas such as `acl-profile`, `client-username`, `client-profile`, and `cluster`.

### Event Management screen 4 of 5 - confirmed bottom and next-step state

After the OAuth and CLI illustrations were restored, one more Scroll page down action reached the true end of the content. Scroll page down is disabled and Go to next step is enabled.

### Event Management screen 5 of 5 - Activity Guide exercises

The final screen directs the learner to try four exercises in the Solace Essentials Activity Guide: Exercise 3, creating a Message VPN using PubSub+ Manager; Exercise 4, creating a Queue using PubSub+ Manager; Exercise 5, mapping topics to a Queue; and Exercise 6, managing a Queue using SEMP. There are no other visible controls on this screen; Go to next step is disabled because it is the final step. No broker or queue configuration was performed.

## LMS check after visiting Event Management

## Key visual asset recovery
