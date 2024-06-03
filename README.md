## **Folderizer**

Folderizer is a sieve filter designed to help automatically organise messages sent to catch all email addresses.

Emails are sorted into Inbox folders based on the receiving email address e.g hello@example.com will be moved to "Inbox/Hello":
- If the folder doesn't already exist it will be created.
- If the email contains any "." then this will create subfolders e.g sieve.test@example.com will be moved to "Inbox/Sieve/test"

### **Examples**

| X-Delivered-To | Folder |
| ----------- | ----------- |
| hello@exmaple.com | Inbox/Example |
| sieve.test@example.com | Inbox/Sieve/test |
| sieve.test.2024@example.com | Inbox/Sieve/test/2024 |
| sieve-filter@example.com | Inbox/Sieve-filter |

### **How to use it?**
1. Find youself an email host that lets you upload a sieve filter.
2. Create a catch all email address - eg. gotta_catch_em_all@example.com
3. Upload your sieve filter.
4. Bask in the glory of an automatically sorted Inbox.

### **FAQ**

#### Where did you get the idea from?
From my ISPs help page on Sieve Filters - https://support.aa.net.uk/Sieve-Example:Move_email_to_a_suffix_folder

#### Why aren't subfolders correctly capitalised?
As per the example above sieve.test is moved to Inbox/Sieve/test. This isn't intentional, I'm just not sure how to fix it. :-)

#### What happens when I reply to those emails? Won't I have the incorrect address in the From field?
Yes, you most likely will unless you want to manually configure your email client to have a From address corresponding to every inbound email. This kind of defeats the purpose of the catch all / makes for a bad overall experience.

Thankfully though, there is a solution (at least for Thunderbird users) in the form of the [ReplyAsOriginalRecipient Thunderbird Extension](
https://github.com/ThierryBZH/ReplyAsOriginalRecipient) by thierry@ephemeride.com

This extension looks for email header "x-original-to", if not found then use address from "to" field if there is only one address. It's a replacement ReplyAsOriginalRecipient extension made by Qiqitori.







