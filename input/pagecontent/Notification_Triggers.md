### Triggering Events for Each Notification Type

Asserting that you support a Notification Type means that agree to abide by that Notification Type’s specific policies and requirements.

#### Admission
When a patient has been checked into the EHR system.  The URLs vary by venue type.

<table border="1">
<thead>
<tr>
<th>Venue</th>
<th>Definition</th>
<th>Canonical URL</th>
</tr>
</thead>
<tbody>
<tr>
<td>General</td>
<td>Patient has been checked in to the EHR, includes all subsidiary admit events</td>
<td>http://www.carequality.net/CEQTopic/admit</td>
</tr>
<tr>
<td>ED</td>
<td>Patient is triaged</td>
<td>http://www.carequality.net/CEQTopic/edadmit</td>
</tr>
<tr>
<td>Acute</td>
<td>An admission order has been issued and bed is assigned</td>
<td>http://www.carequality.net/CEQTopic/acadmit</td>
</tr>
<tr>
<td>Ambulatory</td>
<td>Admitted to an ambulatory encounter</td>
<td>http://www.carequality.net/CEQTopic/ambadmit</td>
</tr>
<tr>
<td>Skilled Nursing/<br> Rehab</td>
<td>Bed is assigned and patient has arrived</td>
<td>http://www.carequality.net/CEQTopic/snradmit</td>
</tr>
</tbody>
</table>

#### Discharge
Push Notification Implementers should use the same criteria for the Discharge trigger that they use for meaningful use reporting.  (i.e., patient's status is changed to "discharged"). Notes, such as Against Medical Advice, are included in or attached to the resulting Encounter Resource.

The canonical URL for this event is http://www.carequality.net/CEQTopic/discharge

#### Referrals
Only applies to Secondary Referrals (i.e., referrals not made by the Notification Recipient, e.g. Notification Recipient (PCP) orders a referral to specialist A, specialist A refers the patient to specialist B – A to B referral is a secondary referral ). Internal (e.g. within an IDN)  consults are not included.

The canonical URL for this event is http://www.carequality.net/CEQTopic/referred

#### Transfer
Transfer Type 1: When a transfer is ordered to any external (any location that would not trigger an internal Admit notification) location. For example
* Any transfer that crosses between EHRs (even when internal to one organization) shall generate a notification; and/or
* Any transfer within a EHR that crosses between settings (ED, Skilled Nursing, etc.) shall generate a notification.

Transfer Type 2: Any time a transfer order is generated.

The canonical URLs for these events are http://www.carequality.net/CEQTopic/transfer-ext (Type 1) and  http://www.carequality.net/CEQTopic/transfer-all (Type 2)

#### Gaps in Care
A trigger based on the [eCQM as defined by CMS](https://www.cms.gov/Regulations-and-Guidance/Legislation/EHRIncentivePrograms/ClinicalQualityMeasures "Electronic Clinical Quality Measures Basics") or other request for follow-up based on Notification Generator policy or process.

The canonical URL for this event is http://www.carequality.net/CEQTopic/caregap

#### Termination of Subscriptions

To terminate subscriptions for all events for a patient, the subscription update event should be marked as "delete".  

The canonical URL for this event is http://www.carequality.net/CEQTopic/delete
