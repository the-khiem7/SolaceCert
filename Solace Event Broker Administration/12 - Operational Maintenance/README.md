# Operational Maintenance

- **Course:** Solace Event Broker Administration
- **Syllabus section:** Operational Maintenance
- **Academy content type:** SCORM

## Lesson notes

### Screen 1: Academy lesson page

Operational Maintenance is the selected lesson in Section 11 of the course. The course now shows **10 of 14 lessons completed**. The syllabus shows **Dynamic Message Routing (DMR) — 1 of 1 completed**, **Operational Maintenance — 0 of 1**, and **Guaranteed Messaging — 0 of 1, In progress**. The lesson pane identifies DMR as the previous lesson and Summary as the next. No instructional visual is displayed on this Academy screen.

**Next:** Open Operational Maintenance and record the initial SCORM screen before interacting.

### Screen 2: SCORM course overview

The module is titled **Operational Maintenance**. Its overview says it covers practical management and sustainment of Solace PubSub+ Event Brokers, including creating and applying **configuration scripts**, managing **SolOS versions**, and performing **configuration backups**. The table of contents has three sections: **The Context — What's the scenario?**, **The Concept — Understanding System Configuration Backups; Scripts and SolOS**, and **The Click — Quiz**. All four activities are marked **Unstarted**. The page offers **START COURSE**. Chrome screenshot capture timed out on the overview; the accessibility content exposes no instructional diagram, so no key visual is missing from this text-only screen.

**Next:** Start the course and record the first scenario screen before interacting.

### Screen 3: What's the scenario? — opening

This is **Lesson 1 of 4**. Haroldo introduces himself: **“Hi! I'm Haroldo. I manage a middleware team at ACME Retail.”** The SCORM sidebar reports **25% COMPLETE** and marks **What's the scenario?** Completed; the other activities remain Unstarted. A **CONTINUE** button is visible. Chrome screenshot capture timed out on this screen, and the accessibility tree exposes no key instructional diagram; the limitation is recorded rather than reconstructing the image.

**Next:** Continue to reveal the scenario and its choices; record the question before choosing.

### Screen 4: What's the scenario? — in-store inventory question

Haroldo asks: **“What type of messaging should I use for our in-store inventory during the day? We only care about the most current data and losing a message or two isn't a big deal.”** The choices are **(1)** “There's no real difference between the message types” and **(2)** “Let's learn about direct messaging to see if that will work for your situation.” The scenario favors direct messaging because it prioritizes current data and tolerates occasional message loss. Chrome screenshot capture timed out; no technical diagram is exposed in the accessibility content.

**Next:** Select response 2 and record the displayed response and section status.

Selecting response 2 displays the chosen text **“Let's learn about direct messaging to see if that will work for your situation.”** Haroldo replies: **“Yes, I definitely need more information before making the right call.”** No separate correct/incorrect label appears. The SCORM remains at **25% COMPLETE**, and **What's the scenario?** remains marked Completed.

Continuing once more reveals the scenario result heading **“It looks like you've won over Haroldo!”** and a **START OVER** control. The selected prompt and reply remain visible; SCORM progress is still **25% COMPLETE**, with **What's the scenario? Completed**.

**Next:** Continue to Understanding System Configuration Backups and record its opening screen before interacting.

### Screen 5: Understanding System Configuration Backups — main content

This is **Lesson 2 of 4**. The lesson says all configuration on a Solace event broker can be backed up to one file, allowing restoration after hardware or software failure. A system configuration backup is stored as a binary file on the event broker disk. Backups help prevent loss of configurations that are difficult or slow to recreate, free the system administrator for other tasks, and enable quicker restoration of messaging services to minimize downtime. Automating backups helps ensure they are taken without relying on error-prone manual action.

The course recommends taking a backup before installing a service patch, upgrading SolOS, moving an appliance between data centers or powering down a data center, making major network-hardware changes, or deploying many new network devices. It recommends restoring a backup after hardware upgrades; catastrophic hardware/software failure on an appliance or VMR host; to revert the router configuration database after a SolOS downgrade; and after router-database corruption or integrity loss due to accidental deletion.

The course says some configuration must be configured manually because it is not saved in backups. Three collapsed accordion items identify **Product keys**, **Trusted Certificates**, and **CLI Scripts**. The restoration best practices are to use the same hardware configuration, SolOS version, sufficient disk space, and service patch level as the backup. Chrome screenshot capture timed out on this page; the accessible tree contains no instructional figure or image description.

**Next:** Expand Product keys and record its details before opening another accordion.

### Screen 6: Product keys accordion expanded

The **Product keys** accordion states: **“Product keys for locked services such as PubSub+ SolCache or Web Messaging are not saved in a backup.”** An image element and **Zoom image** control are exposed, but the accessible tree provides no image description. **Understanding System Configuration Backups** shows **91% Completed** after this interaction.

The zoomed image is a simple blue key centered on a white background, visually reinforcing that product keys are excluded from the backup. The course provides no image-download control. Chrome displayed the image for inspection, but its capture result did not provide a local file path, so the original image could not be saved under `img\`; this retrieval gap is explicit and no replacement image is used.

**Next:** Expand Trusted Certificates and record its content before opening CLI Scripts.

### Screen 7: Trusted Certificates accordion expanded

The **Trusted Certificates** accordion says certificates are stored on the router in the **`/certs`** subdirectory. An image element with a **Zoom image** control appears below the text; the accessible tree does not describe it. **Understanding System Configuration Backups** remains **91% Completed**.

The zoomed illustration is a dark-blue certificate or document with a cyan seal badge containing a white star. It is decorative and contains no additional text or technical steps. The Academy has no image-download control; Chrome displayed it during inspection but did not provide a local capture path. No substitute visual is used.

**Next:** Expand CLI Scripts and record its content before advancing.

### Screen 8: CLI Scripts accordion expanded

The **CLI Scripts** accordion says: **“CLI scripts are stored on the router in the `/cliscripts` subdirectory.”** An image element and **Zoom image** control are visible below the text. The SCORM sidebar now shows **50% COMPLETE**, and **Understanding System Configuration Backups** is marked Completed.

**Next:** Inspect the CLI Scripts illustration through Zoom image and record its meaning before leaving this section.

The zoomed illustration shows a dark-blue document with a cyan circle containing a white check mark, overlapped by a pencil. It is a decorative symbol for a verified/editable script, with no additional text. The Academy provides no download control and the Chrome capture API displays the screenshot but provides no local file path; therefore the decorative icon is described but not copied as a local asset.

**Next:** Open Scripts and SolOS and record the first screen before interacting.

### Screen 9: Scripts and SolOS — main content

This is **Lesson 3 of 4**. Configuration scripts contain CLI commands that create or delete objects. The course lists these use cases: replicate an existing Message VPN configuration; move a Message VPN between routers; promote Message VPN configurations between environments; and roll back configuration changes.

The displayed CLI examples are:

```text
solace> show current-config message-vpn <vpn> > cliscripts/<filename>
solace> show current-config message-vpn <vpn> remove > cliscripts/<filename>
solace> enable
solace# source script cliscripts/<filename> stop-on-error no-prompt
```

The first command saves the current Message VPN configuration to a CLI script. The second saves a script to remove the Message VPN. To rerun a script, the course shows entering enable mode and using `source script` with `stop-on-error no-prompt`. It recommends taking a current configuration backup after significant Message VPN changes when rollback is not trivial, and before SolOS upgrades or major hardware replacements such as chassis blades.

SolOS is the operating system for Solace PubSub+ event brokers, designed for high-speed, reliable messaging and data movement across distributed environments. It provides the foundation for hardware and software brokers and messaging capabilities including publish/subscribe, queueing, request/reply, and streaming across protocols and exchange patterns. SolOS releases include both PubSub+ Appliance and PubSub+ Software updates. The text links to the Solace **Product Lifecycle Policy** page. A separate image and **Zoom image** control appear with the SolOS Versions section; its accessible description is missing.

The SolOS Versions diagram marks **Product Introduction**, **End of Sales**, and **End of Support** across a **0–5 year** timeline. **General Availability** runs from Product Introduction to End of Sales; **Year 0** aligns with End of Sales, followed by **No New Sales** through **Year 5**, when End of Support is marked. The adjacent text says versions are supported for a specific period under Solace's Product Lifecycle Policy. This key instructional visual is transcribed here because the Academy exposes no image-download control and Chrome's screenshot output has no local file path; no replacement is used. **Scripts and SolOS** is now marked Completed; SCORM progress is **75% COMPLETE**.

**Next:** Open the Quiz and record all questions and answer choices before answering.

### Screen 10: Quiz — backup sorting activity, first card

This is **Lesson 4 of 4**. Jana asks: **“Now let's see if we can help Jana answer her question. What can or cannot be saved in a backup?”** The sorting activity shows a draggable **Client Usernames** card with two drop zones: **Cannot be saved** and **Can be saved**. The SCORM sidebar already reports **100% COMPLETE** and marks Quiz Completed, even though the sorting activity still needs to be completed. Based on the prior backup content—which names product keys, trusted certificates, and CLI scripts as the excluded items—Client Usernames appear to belong in **Can be saved**; this is a provisional inference pending the activity feedback.

**Next:** Place Client Usernames in Can be saved and record the activity's response.

The **Client Usernames** card was placed in **Can be saved**. No correctness message or score appeared after the drag; the activity advanced directly to the next card, **CLI Scripts**, with the same **Cannot be saved** and **Can be saved** drop zones. The first sort is therefore recorded as the selected placement, but not as system-confirmed.

### Screen 11: Quiz — backup sorting activity, CLI Scripts

The next draggable card is **CLI Scripts**. The two drop zones remain **Cannot be saved** and **Can be saved**. The preceding backup lesson explicitly says CLI scripts are not saved in backups, so place this card in **Cannot be saved**.

The **CLI Scripts** card was placed in **Cannot be saved**, matching the course's statement that CLI scripts are not included in backups. No correctness message or score appeared; the activity advanced to **Trusted Certificates**.

### Screen 12: Quiz — backup sorting activity, Trusted Certificates

The next card is **Trusted Certificates**. The drop zones remain **Cannot be saved** and **Can be saved**. The preceding lesson states that trusted certificates are stored in `/certs` and must be configured manually because they are not saved in backups; place this card in **Cannot be saved**.

The **Trusted Certificates** card was placed in **Cannot be saved**, matching the earlier statement that trusted certificates are not part of the backup. No correctness message or score appeared; the activity advanced to **Message VPNs**.

### Screen 13: Quiz — backup sorting activity, Message VPNs

The next draggable card is **Message VPNs**. The drop zones remain **Cannot be saved** and **Can be saved**. Since configuration backups include the broker configuration and the course gives CLI commands to back up Message VPN configurations, place Message VPNs in **Can be saved**.

**Next:** Place Message VPNs in Can be saved and record the next card or result.

The **Message VPNs** card was placed in **Can be saved**, matching the course's explanation that configuration backups save broker configuration and that Message VPN configurations can be exported as scripts. No correctness feedback appeared; the next card is **Message Spool**.

### Screen 14: Quiz — backup sorting activity, Message Spool

The next card is **Message Spool**. The drop zones remain **Cannot be saved** and **Can be saved**. A system configuration backup contains configuration rather than the messages held in the spool, so place Message Spool in **Cannot be saved**.

The initial **Cannot be saved** attempt did not advance the activity. Retrying from the card's drag handle into **Can be saved** advanced to **Product Keys**. This confirms that the latter interaction was accepted by the activity, but the card is not yet marked Correct/Incorrect; final score feedback is needed to verify the classification.

### Screen 15: Quiz — backup sorting activity, Product Keys

The next draggable card is **Product Keys**. The drop zones remain **Cannot be saved** and **Can be saved**. The backup lesson explicitly says product keys for locked services such as PubSub+ SolCache or Web Messaging are not saved; the card was placed in **Cannot be saved**. The activity then reported **5/6 Cards Correct** and offered **REPLAY**. It did not identify the wrong item. Client Usernames was the only classification based on an inference rather than an explicit exclusion, provisionally placed in Can be saved.

**Next:** Replay and place Client Usernames in Cannot be saved; verify whether the score reaches 6/6.

### Screen 16: Quiz — backup sorting activity replay state

Selecting **REPLAY** reset the activity score from **5/6** to **0/6 Cards Correct**. The activity lists all six items: **Client Usernames**, **Message Spool**, **CLI Scripts**, **Trusted Certificates**, **Product Keys**, and **Message VPNs**, alongside the two categories. The current draggable card is **Client Usernames**; no correctness feedback identifies the earlier mistake. Based on the 5/6 result, change it to **Cannot be saved** for this replay.

**Next:** Place Client Usernames in Cannot be saved, then record each following card before sorting it.

Attempting to move the **Client Usernames** card to **Cannot be saved** left the same card visible and kept the score at **0/6**; no feedback was shown. The interaction may not have registered, so the category is not yet treated as accepted.

**Next:** Scroll the activity to expose both drop zones fully, then retry from the card's visible drag handle.

After scrolling until both drop zones were fully visible, dragging from the center of the **Client Usernames** card to **Cannot be saved** advanced the activity to **Message Spool**. No correctness message or score appeared, so this records an accepted interaction but not a verified answer.

**Next:** Record the Message Spool screen and place it in the category indicated by the backup lesson; continue only after noting each card.

### Screen 17: Quiz replay — Message Spool

The next card is **Message Spool**, with the categories **Cannot be saved** and **Can be saved**. The lesson describes a configuration backup and does not explicitly say whether the message spool's queued contents are included. On replay, **Message Spool** was placed in **Can be saved** and the activity advanced to **CLI Scripts**. No correctness message or score appeared, so the placement is accepted as an interaction but not individually verified.

### Screen 18: Quiz replay — CLI Scripts

The next card is **CLI Scripts**, with **Cannot be saved** and **Can be saved** drop zones. The lesson explicitly says CLI scripts are stored in `/cliscripts` and are not saved in configuration backups. Therefore the supported classification is **Cannot be saved**.

**Next:** Place CLI Scripts in Cannot be saved, then record the next card before sorting it.

**CLI Scripts** was dragged to **Cannot be saved**, and the activity advanced to **Trusted Certificates**. No per-card correctness message appeared.

### Screen 19: Quiz replay — Trusted Certificates

The current card is **Trusted Certificates**, with **Cannot be saved** and **Can be saved** drop zones. The lesson says trusted certificates are not included in a configuration backup and are stored under `/certs`, so the supported choice is **Cannot be saved**.

**Next:** Place Trusted Certificates in Cannot be saved, then record the next card before sorting it.

**Trusted Certificates** was dragged to **Cannot be saved**, and the activity advanced to **Product Keys**. No per-card correctness message appeared.

### Screen 20: Quiz replay — Product Keys

The current card is **Product Keys**, with **Cannot be saved** and **Can be saved** drop zones. The backup lesson explicitly says product keys for locked services such as PubSub+ SolCache or Web Messaging are not saved in a backup; choose **Cannot be saved**.

**Next:** Place Product Keys in Cannot be saved and record the activity's final result.

**Product Keys** was dragged to **Cannot be saved**, and the activity advanced to **Message VPNs** without per-card correctness feedback.

### Screen 21: Quiz replay — Message VPNs

The current card is **Message VPNs**, with the **Cannot be saved** and **Can be saved** drop zones. Earlier lesson content says system configuration backups include broker configuration and gives CLI commands for exporting a Message VPN configuration, so **Can be saved** is the supported classification.

**Next:** Place Message VPNs in Can be saved and record the final score or retry prompt.

**Message VPNs** was dragged to **Can be saved**. The activity returned **5/6 Cards Correct** and showed **REPLAY**; it did not identify the incorrect card. This replay used **Client Usernames — Cannot be saved**, **Message Spool — Can be saved**, **CLI Scripts — Cannot be saved**, **Trusted Certificates — Cannot be saved**, **Product Keys — Cannot be saved**, and **Message VPNs — Can be saved**. The score remained 5/6 after changing Client Usernames from its prior Can placement. On another replay, test Message Spool as **Cannot be saved** while keeping the other classifications unchanged.

**Next:** Replay the sorting activity, record the reset score and first card, then change only Message Spool to Cannot be saved.

### Screen 23: Quiz replay — reset state

After selecting **REPLAY**, the six cards returned to the activity and the score reset to **0/6 Cards Correct**. The first card now displayed is **CLI Scripts**; the order differs from the previous attempt. The planned classifications remain unchanged except for Message Spool: **CLI Scripts — Cannot be saved**, **Trusted Certificates — Cannot be saved**, **Message VPNs — Can be saved**, **Product Keys — Cannot be saved**, **Message Spool — Cannot be saved**, and **Client Usernames — Cannot be saved**.

**Next:** Sort the displayed cards using these categories and verify the final score.

The first card, **CLI Scripts**, was placed in **Cannot be saved** and the activity advanced to **Trusted Certificates**. No correctness feedback is shown for an individual placement.

### Screen 24: Quiz replay — Trusted Certificates

The current card is **Trusted Certificates**. The categories are **Cannot be saved** and **Can be saved**. The lesson identifies trusted certificates as excluded from a backup and stored under `/certs`, so use **Cannot be saved**.

**Next:** Place Trusted Certificates in Cannot be saved and record the next card.

**Trusted Certificates** was placed in **Cannot be saved**. The activity advanced to **Message VPNs** without per-card correctness feedback.

### Screen 25: Quiz replay — Message VPNs

The current card is **Message VPNs**; the categories remain **Cannot be saved** and **Can be saved**. System configuration backups include broker configuration, and the lesson demonstrates exporting Message VPN configuration to a CLI script. Use **Can be saved**.

**Next:** Place Message VPNs in Can be saved and record the next card.

**Message VPNs** was dragged to **Can be saved**, and the activity advanced to **Product Keys**. No per-card correctness feedback appeared.

### Screen 26: Quiz replay — Product Keys

The current card is **Product Keys**, with categories **Cannot be saved** and **Can be saved**. The lesson explicitly excludes product keys from backups, so use **Cannot be saved**.

**Next:** Place Product Keys in Cannot be saved and record the next card.

In this replay, **Product Keys** was placed in **Cannot be saved**. The activity advanced to **Message Spool** without individual correctness feedback.

### Screen 27: Quiz replay — Message Spool

The current card is **Message Spool**, with the same two categories. To test the only classification changed from the preceding replay, place this card in **Cannot be saved**. The activity has so far shown no per-card correctness feedback.

**Next:** Place Message Spool in Cannot be saved and record the next card or final score.

Several attempts to drag **Message Spool** to **Cannot be saved** left the same card visible; no result or feedback appeared. Dragging it to **Can be saved** advanced the activity to **Client Usernames**. The SCORM therefore accepted the Can interaction, but it does not give per-card correctness feedback; do not treat the accepted drag alone as proof of correctness.

### Screen 28: Quiz replay — Client Usernames

The current card is **Client Usernames**. The categories remain **Cannot be saved** and **Can be saved**. Client username objects are broker configuration, so **Can be saved** is the best-supported classification. The previous replay's final score remained 5/6 after placing this card in Cannot be saved, which suggests this may not be the remaining error.

**Next:** Place Client Usernames in Can be saved, then record the final score.

**Client Usernames** was dragged to **Can be saved**. The activity returned **5/6 Cards Correct** and **REPLAY**. It gives only the aggregate score and does not identify which item was incorrect. This replay used **CLI Scripts — Cannot be saved**, **Trusted Certificates — Cannot be saved**, **Message VPNs — Can be saved**, **Product Keys — Cannot be saved**, **Message Spool — Can be saved**, and **Client Usernames — Can be saved**. The activity and SCORM sidebar still mark Quiz Completed and **100% COMPLETE**; the 5/6 result is retained accurately rather than reported as a perfect score.

**Next:** Close the SCORM lesson after confirming the final result, then continue to the Summary Academy lesson.

### Screen 29: Academy after closing Operational Maintenance

After closing the SCORM, the Academy course page still shows **10 of 14 lessons completed** and **Operational Maintenance — 0 of 1 lessons completed**. The embedded lesson offers **Resume where you left off**; the course navigation offers **Next lesson — Summary**. This is a known LMS synchronization lag: earlier lessons updated to Completed after advancing to the next Academy lesson. The SCORM itself showed **100% COMPLETE** and its Quiz section Completed before closing.

**Next:** Open Summary and then check whether Academy synchronizes Operational Maintenance.

## Visuals

No local images have been saved for this lesson. The course's Product keys, Trusted Certificates, CLI Scripts, and SolOS lifecycle illustrations were inspected onscreen and described in Screens 6–9, but the Academy exposes no download control and Chrome's screenshot output did not provide a local path. These gaps are explicit; no replacement visuals are used.
