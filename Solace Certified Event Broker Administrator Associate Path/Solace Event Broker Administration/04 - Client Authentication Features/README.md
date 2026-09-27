---
title: "Client Authentication Features"
document_type: lesson
learning_path: "Solace Certified Event Broker Administrator Associate Path"
course: "Solace Event Broker Administration"
lesson_order: 4
source: Solace Academy
---

# Client Authentication Features

- **Course:** Solace Event Broker Administration
- **Syllabus section:** Client Authentication
- **Academy content type:** SCORM

## Screen 1: Course overview

The overview describes a comprehensive introduction to PubSub+ client authentication, focusing on **internal**, **RADIUS**, and **LDAP** authentication. It promises theory plus a hands-on activity implementing client authentication in PubSub+ Manager.

The SCORM table of contents groups the lesson into **The Context** (What's the Scenario?), **The Concept** (Understanding Client Authentication), and **The Click** (Hands-on Activity). All three sections initially showed Unstarted. The START COURSE link opens What's the Scenario?.

The cover uses an original background asset named `ogw3GKnfxHOrA_2c.jpg`, exposed by the page's CSS. It has no descriptive alternative text. No local image was saved: the Chrome screenshot API has timed out on this course page, and direct retrieval from the course CDN failed with a workstation DNS error. The cover visual is recorded as a capture gap; no substitute has been created.

## Screen 2: What's the Scenario? - Jana

Jana introduces herself as a member of the administration team. She says the team needs to ensure that its order management system is secure. The screen offers a CONTINUE button to reveal the next part of the scenario.

The scenario uses the original background asset `stock-image.jpg`, with no descriptive alt text. Its visual was not copied into `img/`: Chrome screenshot capture is unavailable in this session, and the workstation previously failed to resolve the course CDN host. No substitute image was created.

## Screen 3: Scenario risk and response choices

Jana explains that ACME Retail's order management system must not be accessed by someone pretending to be a consumer. Such access could put order processing and customer data at risk.

The two responses are:

1. “Let's learn about the different authentication methods and features to help you choose.”
2. “With cloud authentication, that's just a risk you have to take.”

The first response is the appropriate path because it investigates authentication controls rather than accepting impersonation risk. The scenario remains at 33% SCORM completion and marks What's the Scenario? Completed.

## Screen 4: Scenario response

I selected response 1. The scenario displays Jana's selected response, “Let's learn about the different authentication methods and features to help you choose,” and removes the two choice buttons. No further feedback text appears on this screen; the internal navigation link leads to Understanding Client Authentication. What's the Scenario? is marked Completed.

## Understanding Client Authentication

### Client authentication methods

Client authentication establishes that messaging-system clients are who they claim to be. Basic authentication presents a valid client username and password. Using the broker's internal username/password database can suit small deployments or testing, but has limitations. The broker can validate credentials against LDAP (including Active Directory) or RADIUS, moving password management to an external service; the client application or user must still store or remember the password. Kerberos single sign-on, client certificates, and OAuth/OpenID Connect token authentication are presented as ways to avoid retaining a username/password on the client.

### Internal authentication

Basic internal authentication is the default. It authenticates the client's username and password against the broker's internal database, and the username must match a client username account provisioned on the event broker. Internal credentials are stored on the broker; the other schemas described here store credentials outside it.

### RADIUS authentication

The course lists these requirements:

- Up to three RADIUS servers on external host machines.
- The client's username and password are sent to an external RADIUS server for authentication.
- Configure RADIUS domains and RADIUS profiles on the Solace PubSub+ Event Broker.

A **RADIUS domain** is the authentication-domain string appended to CLI usernames in outgoing RADIUS access requests. A **RADIUS profile** contains authentication-request retransmit and timeout values and per-server RADIUS authentication configuration.

### LDAP authentication

The course lists up to three LDAP servers on external hosts. Client usernames and passwords are sent to an external LDAP server. Up to ten LDAP profiles can be configured on the Solace PubSub+ Event Broker.

An LDAP profile must be configured and enabled for LDAP authentication to work; creating the profile does not enable it automatically. It stores authentication/authorization retry and timeout values and configuration for its LDAP servers. A system administrator must configure at least one reachable LDAP server and a search base DN.

### Client certificate authentication

A client proves its identity using a valid X.509 v3 certificate issued by a recognized Certificate Authority (CA). The lesson lists four requirements:

- Clients specify a client certificate and private key.
- Client-certificate authentication is enabled and configured on every Message VPN the client will use.
- The TLS/SSL service is configured and enabled, including the TLS/SSL server-certificate file used by the event broker.
- CA certificates are loaded onto the event broker so it can construct a full certificate chain and validate incoming certificates for SSL connections.

A client connecting to a Message VPN must still provide a valid client username. By default, the common name (CN) in the certificate subject becomes that username.

### Key visuals and capture gap

The lesson exposes four images: `security-concepts-overview.jpg` (608 x 611 pixels, loaded in the page), `AdobeStock_135042763.jpg`, `AdobeStock_442053298.jpg`, and `LDAP process.jpg`. All have empty alt text. The image filenames are recorded, but none is in `img/`: Chrome screenshot capture has timed out on the Academy page and direct image retrieval fails because the workstation cannot resolve the CDN host. No substitute visuals were created. The section shows **8% Completed** at the last observation; the scenario prompt “Tell me what you've got!” and its CONTINUE control remain at the bottom.

## Image interaction: Goals for a secure system

Selecting the first Zoom image control opens an enlarged-image container and replaces the control with Unzoom image. The enlarged image has no additional accessible description. This confirms the image can be expanded, but its visual remains unavailable for local capture.

## Image interaction: Client Basic Internal Authentication

Selecting Zoom image for the Client Basic Internal Authentication illustration opens the same enlarged-image container with an Unzoom image control and no additional accessible description. The illustration remains a capture gap.

## Image interaction: Client Basic RADIUS Authentication

The RADIUS illustration also opens in an enlarged-image container with an Unzoom image control and no added accessible description. Its visual remains unavailable for local capture.

## Certificate checklist interaction

I checked all four items shown under the client-certificate implementation requirements: client certificate/private key, certificate-authentication configuration for each target Message VPN, TLS/SSL service, and CA certificates on the broker. All four checkboxes now show selected, and the SCORM table of contents marks Understanding Client Authentication Completed. The module shows 67% overall (two of three sections complete).

The LDAP image opened after a retry using its refreshed accessibility control. Its enlarged-image container adds no descriptive text, and the image itself has no alt text; the visual remains uncaptured.

## Image interaction: LDAP process

The LDAP process illustration opens in the enlarged-image container after re-targeting the control from the refreshed accessibility tree. It offers Unzoom image and adds no descriptive text. Its source is `LDAP process.jpg`; the visual remains a local-capture gap.

## Hands-on Activity: introduction

The activity says its goal is to explore implementing client authentication in PubSub+ Manager. It offers two steps:

1. **Walkthrough video:** “Let's do a walkthrough of client authentication on PubSub+ Manager.”
2. **Explore your environment:** “Now go ahead and follow along in your own environment to get a better understanding of the options and how to configure your authentication.”

The second step explicitly refers to using the learner's own environment, so I will inspect the course demonstration and instructions first and will not change a live broker without a target/action authorized by the user. The original screen asset is `Hands-on Activity - Client Authentication Configuration.jpg` (1920 x 1080, no alt text); it was not captured locally because course screenshots and CDN retrieval are unavailable.

At the time this screen opened, the SCORM table of contents already marked Hands-on Activity Completed and showed **100% COMPLETE**, before I had opened its START control. I will still review the visible steps and any course video before leaving.

## Step 1: Walkthrough video

The first activity card is titled **Walkthrough video** and says, “Let's do a walkthrough of client authentication on PubSub+ Manager.” Its player exposes the original media `Hands-on Activity - Client Authentication Configuration.mp4` and poster of the same base name. Before playback, the player had no loaded duration and exposed no caption/text tracks. The control sequence includes Step 1, Step 2, and Last step.

The poster has no descriptive alt text and is not saved locally because the Academy screenshot/CDN capture limitations noted above also apply here. No live configuration has been performed.

## Resume checkpoint

The course video was played through to its end while muted at 2x speed. Its duration is **2:25** (145.512 seconds), and the player exposes no caption or text tracks. The player returned to the beginning after reaching the end. No external PubSub+ Manager changes were made. This completes the walkthrough review; the SCORM remained marked 100% complete.

## Step 2: Explore your environment

The activity instructs the learner to follow along in **their own environment** to understand the available client-authentication options and how to configure them. It provides no embedded broker simulator or course-controlled sandbox on this screen. This is an instruction for a real external environment, so I did not connect to or modify a broker. The screen is recorded as reviewed with the environment exercise intentionally not performed. The SCORM had already marked the full Hands-on Activity complete before either step was reviewed.

## Hands-on Activity: final screen

The activity's final step contains only **START AGAIN** and the step-progress controls; it presents no additional lesson text. The player shows the walkthrough at 100% loaded, and the lesson outline marks all three sections Completed with **100% COMPLETE**. The SCORM review is finished.

## Resume checkpoint

Lesson 04 has been reviewed through the final screen of the Hands-on Activity. Its SCORM shows 100% COMPLETE and all three sections are marked Completed. Next, close the SCORM and refresh the Academy course page to verify the lesson completion status before opening Lesson 05, Client Authorization.
