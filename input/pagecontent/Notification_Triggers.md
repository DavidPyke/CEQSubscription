<!-- Notification_Triggers.md {% comment %}
*****************************************************************************************
*                            WARNING: DO NOT EDIT THIS FILE                             *
*                                                                                       *
* This file is generated by SUSHI. Any edits you make to this file will be overwritten. *
*                                                                                       *
* To change the contents of this file, edit the original source file at:                *
* ig-data/input/pagecontent/6_Notification_Triggers.md                                  *
*****************************************************************************************
{% endcomment %} -->
### Triggering Events for Each Notification Type

Asserting that you support a Notification Type means that agree to abide by that Notification Type’s specific policies and requirements.

#### Admission
When a patient has been checked into the EHR system.  Codes vary by venue type.

|Venue | Definition | Code |
|--------------|---------------|---|
|General | Patient has been checked in to the EHR, <br> includes all subsidiary admit events | admit |
|ED | Patient is triaged| edadmit |
|Acute | An admission order has been issued and bed is assigned | acadmit|
|Ambulatory | Admitted to an ambulatory encounter |ambadmit|
|Skilled Nursing/<br> Rehab | Bed is assigned and patient has arrived| snradmit|

#### Discharge
Push Notification Implementers should use the same criteria for the Discharge trigger that they use for meaningful use reporting.  (i.e., patient's status is changed to "discharged"). Notes, such as Against Medical Advice, are included in or attached to the resulting Encounter Resource.

#### Referrals
Only applies to Secondary Referrals (i.e., referrals not made by the Notification Recipient).  Internal consults are not included.

#### Transfer
The issuance of a transfer order that will not create an admit notification from the same system and is not originating from the Notification Recipient.

#### Gaps in Care
A trigger based on the [eCQM as defined by CMS](https://www.cms.gov/Regulations-and-Guidance/Legislation/EHRIncentivePrograms/ClinicalQualityMeasures "Electronic Clinical Quality Measures Basics") or other request for follow-up based on Notification Generator policy or process.