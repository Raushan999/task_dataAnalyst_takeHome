1. Problem statement:-
A dataset generated via our tele-calling operations is available below. 
We have a small team of tele-callers who make calls to users who have applied for jobs on our job assistant 
(you can try it by sending a “hi” on WhatsApp to +91-8050-205-205). The goal is to gauge their interest in 
the job and then push them to go for the interview and get hired. 
In some cases, we might make calls to a list of leads received from a 3rd party. 
For instance, to a list of drivers received from a driving school to place them in a job at a cab company. 
Our tele-callers generally make follow-up calls to leads who don't answer the phone (RNR status) or 
who demonstrate interest (to get them to go for the interview/on-boarding).

2. Descriptions of the various tables in the dataset are below: 
**leads**
○ id (uniqueidentifier)
○ userId (foreign key reference to our internal users table) 
○ name (lead’s name) 
○ phoneNumber (lead’s phone number) 
○ city (lead’s city) 
○ state (lead’s state) 
○ source (source of the lead) 
○ isExternal (false if the lead was acquired via our job assistant; true if the lead was acquired via a 3rd party source) 
○ createdAt (date/time of creation of the table entry) 
○ receivedAt (date/time when the lead was received by us) 
**lead_calls**
○ Id (unique identifier) 
○ telecallerId (foreign key reference to telecallers table) 
○ leadId (foreign key reference to leads table) 
○ client (name of the client/company/employer who the call was made for) 
○ status (status of the call) 
○ comments (comments entered by the telecaller) 
○ calledAt (date/time of the call) 
○ createdAt (date/time of creation of the table entry) 
**telecallers**
○ Id (unique identifier) 
○ name (telecaller’s name) 
○ phoneNumber (telecaller’s phone number) 
○ createdAt (date/time of creation of the table entry) 
