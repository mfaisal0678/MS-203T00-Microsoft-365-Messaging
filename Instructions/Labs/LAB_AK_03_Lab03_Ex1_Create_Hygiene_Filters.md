# Module 3 – Lab 3 - Exercise 1 - Create Hygiene Filters

In this lab, you will continue in your role as Holly Dickson, Adatum’s Messaging
Administrator. Adatum has experienced a recent rash of malware infections. The
company's CTO has asked Holly to investigate the various options that are
available in Exchange Online to fortify Adatum’s messaging environment. Holly
will begin by creating a series of hygiene filters that are designed to protect
Adatum’s messaging environment. You will create a malware filter, a connection
filter, and a spam filter.

**Note**: In this lab exercise, you will use the **Office 365 Security and
Compliance center** to create hygiene filters. Protection services no longer
reside in the EAC for Exchange Online, and instead have been moved to the
Security and Compliance center.

## Task 1 - Create a Malware Filter

In this task, you will create a malware filter that checks for attachments that
have a specific file type that indicate a possible malware attachment. If an
attachment is found matching one of those file types and the recipient’s domain
matches Adatum’s Microsoft 365 domain, then a notification message will be
applied to the email.

1.  You should still be logged into LON-CL1 as the **Administrator** with a
    password of **Pa55w.rd**; however, if the log-in page appears, then log in
    now.

2.  In your **Edge** browser, enter **protection.office.com** as URL

3.  In the left-hand navigation pane, select **Security**.
    
4.  In the **Office 365 Security & Compliance center**, select **Permissions**.
    
5.  In the **Home \> permissions** page in the **search** field, type **Org** then select the search glass.

6.  On the **Home \> permissions** page list, select the **Organization Management** role.

7.  On the **Organization Management**page under the **Members**section, select the **Edit** icon.

8. On the **Editing choose members** page. Select **Choose members**.

9. On the **Choose members** page, Select the **Add** icon.

10. On the **Choose members** list. Select the **Mod Administrator** account.Then select the **Add** icon.

11. On the **Choose members** page. Select the **Done** icon.

12. On the **Editing choose members** page, select the **Save** icon.

     **Note**: the organization management role may take a minute or two to update the microsoft tenant. If the policy doesn't update within a few minutes proceed to the connection filter task. 
     
13. In the **Office 365 Security & Compliance center**, select **Threat Management** in the left-hand
    navigation pane, and then in the expanded group select **Policy**.     
     
14.  In the **Home \> Policy** page, select the **Anti-Malware** tile under the
    **Policies** section.

15. In the **Home \> Policy \> Anti-malware** page, on the menu bar at the top
    of the window, select **+Create** to add a new malware filter. This
    initiates the **Create an anti-malware policy** wizard.

16. In the **Name your policy** page, enter **Malware Policy** in the **Name**
    field.
    
17. In the **Description** field, enter **This policy has been created to
    protect the messaging environment** and then select **Next**.   

18. In the **users and domains** section under domains, enter **onmicrosoft.com** and then select **Next**.

19. On the **protection settings** page, select the checkboxes for **enable the common attachements filter** and **enable zero-hour auto purge for malware (recommended)**.

20. On the **Notifications** section, since this filter will not generate any
    notifications, do not select any of the notification options, and instead
    select **Next**.

21. On the **reivew** section, confirm that all the information is correct, then select the **Submit** icon.

22. Congratulations, the New Anti-Malware policy has been created. Select the **Done** icon.

    **Note**: A **Security & Compliance** window will appear with a message that indicates your organization settings need to be updated. Select **Yes** to continue.
    
23.  It may take a minute or so for your organization settings to be updated.
    Once the update is complete and you are back on the **Home \> Policy \>
    Anti-malware** page, you can proceed to the next task. Do not close any of
    the browser tabs.

## Task 2 - Create a Connection Filter

In this task, you will modify the default connection filter to include an
allowed IP address and a blocked IP address. Any messages originating from the
allowed IP address will always be accepted, and any messages originating from
the blocked IP address will always be blocked.

1.  You should still be logged into LON-CL1 as the **Administrator** with a
    password of **Pa55w.rd**; however, if the log-in page appears, then log in
    now.

2.  In your **Edge** browser, you should still be in the **Office 365 Security &
    Compliance center** (SCC). If so, then proceed to the next step; otherwise,
    perform the steps from the prior task to navigate to the SCC now.

3.  In the **Office 365 Security & Compliance admin center**, select **Threat Management** in the left-hand
    navigation pane, and then in the expanded group select **Policy**.

4.  In the **Home \> Policy** page, select the **Anti-spam** tile under the
    **Policies** section.

5.  In the **Anti-spam settings** window, in the list of policies, select the
    drop-down arrow to the left of **Connect filter policy (always ON)** and
    then select the **Edit policy** button that appears.

6.  On the **Connection filter policy** pane, you can identify the IP Addresses
    that can send messages to your environment and the IP addresses will be
    blocked from sending messages.

    **Note:** At this time, you will NOT be adding IP addresses to the allow or
    block lists. You can do this if you have a known IP address you would like
    to test against. However, it typically takes up to 1 hour to propagate the
    change within the system. For this lab, simply review the fact that you can
    create allowed and blocked lists of IP addresses in this **Connection filter
    policy** pane.

    On the **Connection filter policy** pane, select the **Turn on safe list**
    check box at the bottom of the page.

    **Important:** Selecting the **Turn on safe list** check box is a best
    practice that enables for your Microsoft 365 tenant the most common
    third-party sources of trusted senders to which Microsoft subscribes.
    Selecting this check box skips spam filtering on messages sent from these
    senders, ensuring that they are never mistakenly marked as spam.

7.  Select **Save**.

8.  Leave the Office 365 Security & Compliance center open in your browser and
    proceed to the next task.

## Task 3 - Create a Spam Filter

For Microsoft 365 customers whose mailboxes are hosted in Microsoft Exchange
Online, their email messages are automatically protected against spam and
malware. Microsoft 365 has built-in malware and spam filtering capabilities that
help protect inbound and outbound messages from malicious software and help
protect users from receiving spam messages.

For Microsoft 365 customers whose mailboxes are hosted in Microsoft Exchange
Online, their email messages are automatically protected against spam and
malware. Microsoft 365 has built-in malware and spam filtering capabilities that
help protect inbound and outbound messages from malicious software and help
protect users from receiving spam messages.

As Adatum’s Messaging Administrator, Holly doesn't need to set up or maintain
the filtering technologies, which are enabled by default. However, she can make
company-specific filtering customizations in the Exchange admin center. She has
decided to test this out by configuring a spam policy to grant or deny an email
by focusing on the language of the email and the location of the email's origin.

1.  You should still be logged into LON-CL1 as the **Administrator** with a
    password of **Pa55w.rd**; however, if the log-in page appears, then log in
    now.

2.  In your **Edge** browser, you should still be in the **Office 365 Security &
    Compliance center** (SCC). If so, then proceed to the next step; otherwise,
    perform the steps from the prior task to navigate to the SCC now.

3.  In the **Office 365 Security & Compliance center**, you should still be on
    the **Anti-spam settings** page after completing the prior task. If so, then
    proceed to the next step; otherwise, in the left-hand navigation pane,
    select **Threat Management**, select **Policy,** and then select the
    **Anti-spam** tile under the **Policies** section.

4.  In the **Anti-spam policies** windows in the list of policies, select the
    **Anti-spam inbound policy(defualt)**.

5.  In the **Anti-spam inbound policy (default)** pane, you will be
    presented a variety of options on how you would like spam to be handled and
    what rating will be triggered depending on the severity of the spam. The
    following steps will guide you through these settings so that you can update
    them per Adatum's requirements.

6.  Select the **edit spam threshhold and properties** link, under the **bulk email threashold & spam properties** section. Update the
    following settings:

    -   set the threshold: **5** 
   
    -   **mark as spam** 
    -   empty messages: **Off**
    -   Embedded tags in HTML: **On**
    -   JavaScript or VBScript in HTML :**On**
    -   SPF record hard fail: **On**
    -   Sender ID filtering hard fail: **On**
    -   from these counties:

           -   Type the letters **"ab"** in the **from theses countries** field to display
                the list of countries starting with the letters “ab” or that
                include an “ab”. You can enter any letter or letters that you
                wish.

           -   Select any country/region you want to restrict.

           -   If you want to restrict an additional country, repeat the
                prior two steps.
                
                
7.  Once you have selected all the countries/regions that you want to restrict. Select **save**.             

8.  Select the **edit actions** icon under the **actions** section to update the following
    settings:

    **Note:** This section determines what happens to emails that have been tagged as spam.

    -   Select the **spam** drop-down arrow and select the **Move message to junk email folder**.

    -   Select the **phishing** drop-down arrow and select **quarrantine message**.

     -  change **retain spam in quarantine for this many days** to **10** days.

9.  Select **Save**.

10.  In the list of spam filters, select the drop-down arrow to the left of the
    **Default spam filter policy (always ON)** filter that you just edited. In
    the middle column of settings for this filter, note how **End-user spam
    notifications** are disabled (it status is **Off**). <br/><br/>
    Below this option, select **Configure end-user spam notifications**.

11.  In the **Default** window that appears, select the **Enable end-user spam
    notifications** check box, and then change the **Send end-user spam
    notifications every (days)** value to **5**.

12.  Select **Save**.

13.  In your Edge browser, leave the **Office 365 Home** tab open as well as the **Microsoft 365 admin center** tab. Close all other tabs and proceed to the next lab.

# End of Lab 3
