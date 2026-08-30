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
<img width="642" height="517" alt="ss-rg1" src="https://github.com/user-attachments/assets/417f157b-29b7-4982-8e73-8410378ebdbe" />

</br>Step 2.</br>
Dig deep in to the incident by referring to Tags. Tags can help identify what resources were made/deployed or configured incorrectly. Go to:</br>
Resource groups > Select the Resource group in question > Tags > Look for the intern-flag and take note of its value(string).


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
