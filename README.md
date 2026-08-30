<img width="1774" height="402" alt="MadhatCh1-banner2048x334" src="https://github.com/user-attachments/assets/e69a98ef-fbb6-4981-b32c-30847466dba9" />

# Operation Dead Deploy: Investigating a misconfigured Azure policy

## Scenario
<!---
2 to 3 sentences. What was the situation and what question did the investigation answer? Frame it like a work ticket, not homework.
--->
A temporary test environment was deployed for a junior intern with a temporary contributor access. His unfamiliarity with the company's governance caused some issues. This investigation focuses on identifying what was incorrectly configured/deployed, and if there's any policy that are configured incorrectly.

## Environment 
<!---
One list: platform, services, tools, access level. Honest framing: "live multi-user Azure training tenant, Reader access."
--->
Live multi-user Azure training tenant, Reader Access.

## Investigation
<!---
The core. Numbered steps IN YOUR OWN WORDS: what you looked at, what you found, what you concluded at each step. 6 to 12 screenshots of meaningful moments (portal views, query results, before/after).
--->
Step 1.</br>
This subscription follows Microsoft's naming convention. All but one is not following that standard, it was identified by:</br>
Searching Resource group or click Resource group icon > Resource Manager > Locate and identify that particular RG.

<img width="1686" height="327" alt="ss-rg" src="https://github.com/user-attachments/assets/3d1bbed4-48e4-4963-9e65-ac151f3e89c1" />
<img width="642" height="517" alt="ss-rg1" src="https://github.com/user-attachments/assets/206422f8-daf9-4ccf-a28b-b305e232c607" />

</br>Step 2.</br>
Digging deep in to the incident by referring to Tags. Go to:</br>
Resource groups > Select the Resource group in question > Tags > Look for the intern-flag and take note of its value(string).

<img width="1905" height="718" alt="ss-tags" src="https://github.com/user-attachments/assets/cbd5b345-16d1-4170-abd8-2b639877d6f0" />

</br>Step 3.</br>
Looking for the source of the resource. All resource deployment has names, timestamp, status and these are stored at Deployments, to locate: </br>
Resource groups > Select the RG > Deployments 

<img width="1319" height="640" alt="ss-deploy" src="https://github.com/user-attachments/assets/37d15308-4951-4d59-b1fe-25362146e55c" />




## What broke / what surprised me
<!---
The most credible section in the document. Dead ends, wrong guesses, the thing that took an hour. Employers know real work is messy. This section separates you from certificate collectors.
--->
## Findings and recommendations
<!---
What you determined, plus 2 or 3 recommendations as if you were reporting to the resource owner.
--->
## What I learned
<!---
3 to 5 bullets. At least one technical, one "what I'd do differently."
--->
