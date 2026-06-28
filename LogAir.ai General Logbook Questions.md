# LogAir.ai General Aircraft Logbook Analysis (tm)

To gain an idea of the general maintenance status of this aircraft, this engineered prompt contains optimized, structured prompts designed to extract comprehensive maintenance, damage, operational, and system-specific histories from aircraft logbooks using NotebookLM. 

---

## 1. Tracking Damage History & Major Repairs
Logbooks rarely use blunt words like "crashed." Instead, mechanics write about what they *replaced*, *straightened*, *rigged*, or *reconstructed*. These prompts target specific industry euphemisms and regulatory documents.

> **Prompt for Gear-Up Landings & Prop Strikes:**
> """
> Scan the text for any mentions of 'gear-up,' 'belly landing,' 'propeller strike,' 'prop strike,' 'sudden stoppage,' 'dial indicator,' 'crankshaft runout,' or 'reregulated.' Provide the dates and details of any occurrences.
> """

> **Prompt for Structural Repairs:**
> """
> Look for structural repair terminology such as 'replaced skin,' 'spliced,' 'bulkhead repair,' 'spar replacement,' 'doubler installed,' or 'frame alignment.' Summarize the context and dates of these repairs.
> """

> **Prompt for Major Alterations:**
> """
> Are there any entries referencing 'Form 337' or 'Major Repair and Alteration'? List all occurrences with dates, who performed the work, and a summary of what was fixed or modified.
> """

---

## 2. Analyzing Maintenance Habits & Inactivity
A healthy airplane is an airplane that flies regularly. These prompts help determine if the previous owner followed rigorous maintenance intervals or if the plane sat decaying in a hangar.

> **Prompt for Oil Change Frequency:**
> """
> Analyze the oil change history. What is the average number of flight hours between oil changes? List any instances where the interval exceeded 50 hours or 4 months, and note if oil analysis or filter inspection findings (such as 'metal flakes' or 'contamination') are mentioned.
> """

> **Prompt for Annual Inspections:**
> """
> Compile a chronological timeline of all 'Annual Inspections' or '100-hour Inspections.' Are there any missing years or significant chronological gaps in the annual inspection history?
> """

> **Prompt for Periods of Inactivity:**
> """
> Look at the dates and tach/Hobbs hours across the logbooks. Identify any periods longer than 6 months where the aircraft recorded zero or minimal flight hours. List the start and end dates of these inactive periods.
> """

> **Prompt for Inactivity Side-Effects:**
> """
> During or immediately following the identified periods of inactivity, are there any mentions of 'corrosion,' 'pitting,' 'camshaft replacement,' 'lifter replacement,' 'cylinder rust,' or 'pickling/preservation'?
> """

---

## 3. Detecting Harsh Operations
Certain commercial or utilitarian missions put immense aerodynamic, thermal, and structural stress on an airframe. Use this prompt to flag specialized operations:

> **Prompt for Fleet/Harsh Operations:**
> """
> Search the entire document for keywords indicating specialized, fleet, or harsh operational history. Look specifically for: 'pipeline,' 'patrol,' 'fire,' 'tanker,' 'skydiving,' 'jump,' 'parachute,' 'tow,' 'glider,' 'banner,' 'agricultural,' 'spray,' 'flight school,' 'instructional,' or 'livery.' Summarize any entries containing these terms. Furthermore, note if there are patterns of multiple short flights recorded on the same day by different pilot names.
> """

---

## 4. Component-Specific Deep Dives

### Engine(s) Specifics
Aircraft engines speak in numbers (compressions) and component names. This prompt forces NotebookLM to look past a simple "runs fine" and dig into the actual health of the powerplant.

> **Prompt for Engine Analysis:**
> """
> Analyze the engine logbooks and extract the following details for all engines installed:
> * **Time & Overhaul:** What is the current Time Since Major Overhaul (SMOH) or Time Since New (TSN)? Identify the date and the name of the facility that performed the last overhaul.
> * **Top Overhaul:** Are there any mentions of a 'Top Overhaul,' 'STOH,' or individual 'cylinder replacement' or 'cylinder repair'? List which cylinders were affected and at what engine hours.
> * **Compressions:** Summarize the historical trend of cylinder compression checks (e.g., 74/80). Note any compressions that dropped below 70/80 or any comments regarding 'exhaust valve leaking.'
> * **Accessories:** Scan for maintenance or replacement of major engine accessories, specifically: 'magnetos' (including 500-hour inspections), 'starter,' 'alternator,' 'fuel pump,' 'vacuum pump,' and 'turbocharger' or 'wastegate' (if applicable).
> * **Contamination:** Search for terms like 'metal in screen,' 'metal in filter,' 'oil analysis report,' or 'bearing material' and provide the exact dates and contexts.
> """

### Propeller(s) Specifics
Propellers are frequently overlooked, but a prop strike or an aging hub can introduce major hidden expenses. This prompt searches for signs of impact, stress, or leaks.

> **Prompt for Propeller Analysis:**
> """
> Analyze the propeller logbooks and extract the following specific details:
> * **Time & Overhaul:** What is the Time Since Propeller Overhaul (SPOH) or Time Since New (TSN)? Note the date and facility of the last overhaul.
> * **Physical Condition & Dressing:** Look for mentions of 'dressed blades,' 'filed nicks,' 'ground down,' or 're-pitched.' 
> * **Hub & Seals:** Search for keywords like 'resealed hub,' 'leaking oil,' 'grease spray,' 'hub dye penetrant inspection,' or 'eddy current inspection.'
> * **Governor:** Are there any records of the propeller governor being replaced, overhauled, or adjusted?
> * **Prop Strike Checks:** Specifically look for compliance with manufacturer prop-strike inspections or entries containing 'sudden stoppage inspection' or 'dialed crankshaft.'
> """

### Airframe Specifics
This prompt focuses on the bones of the aircraft—rigging, landing gear, control surfaces, and structural integrity.

> **Prompt for Airframe Analysis:**
> """
> Analyze the airframe logbooks and extract the following specific structural details:
> * **Rigging & Flight Controls:** Search for entries containing 'rigged flight controls,' 'cable tension check,' 'balanced control surfaces,' 'replaced pulleys,' or 're-skinned elevator/rudder.'
> * **Landing Gear System:** For retractable gear, find mentions of 'gear swing,' 'emergency extension test,' 'replaced actuators,' 'bushing replacement,' 'nose gear shimmy dampener,' or 'retraction test.' For fixed gear, look for 'cracked wheel pants' or 'gear leg alignment.'
> * **Windows & Windshield:** Identify when the 'windshield' or 'side windows' were last replaced, and note any mentions of 'crazing' or 'clouding.'
> * **Fuel Tanks:** Look for references to fuel system maintenance, specifically 'fuel bladder replacement,' 're-sealed tanks,' 'fuel leaks,' or 'fuel selector valve overhaul.'
> """

### Avionics & Electrical Specifics
Avionics logs mix statutory biennial checks with expensive upgrade histories. This prompt separates routine compliance from physical system tracking.

> **Prompt for Avionics Analysis:**
> """
> Analyze the avionics and electrical logbook entries and extract the following specific details:
> * **Certifications:** Identify the dates of the most recent IFR certifications, specifically '91.411' (altimeter/static system) and '91.413' (transponder) checks.
> * **Upgrades & Panel Modifications:** List all instances where equipment was 'removed' and 'installed' in the instrument panel. Identify major components like GPS units, audio panels, glass displays (EFIS), and engine monitors.
> * **Autopilot:** Search for references to the 'autopilot,' 'servos,' 'bridle cables,' or 'heading coupler' maintenance or troubleshooting.
> * **Wiring & Electrical Faults:** Look for troubleshooting terms like 'chafed wiring,' 'short circuit,' 'replaced circuit breaker,' 'ground wire repair,' or 'intermittent electrical bus dropouts.'
> """

---

## 5. Comprehensive Maintenance Picture & Extra Questions

| Focus Area | NotebookLM Prompt to Copy/Paste |
| :--- | :--- |
| **Airworthiness Directives** | "Provide a list of all Airworthiness Directives (ADs) and Service Bulletins (SBs) noted as 'complied with' (C/W). Are there any recurring ADs, and when was the last compliance recorded?" |
| **Corrosion & Environment** | "Search for any mentions of 'corrosion,' 'rust,' 'pitting,' 'treatment,' 'CorrosionX,' 'Zinc Chromate,' or 'Alodine.' Note the dates and locations on the airframe where corrosion was addressed." |
| **Major Component Life** | "Identify the most recent engine overhaul (SMOH) and propeller overhaul (SPOH). What were the exact dates, engine hours, and what maintenance facility performed the overhauls?" |
| **Recent Part Wear** | "Summarize component replacements in the last 5 years. Has the alternator, starter, magnetos, fuel pump, vacuum pump, or landing gear actuator been replaced or overhauled recently?" |
| **Logbook Continuity** | "Are there any entries mentioning 'lost logbooks,' 'duplicate logbook opened,' 'reconstructed records,' or missing pages?" |
| **Modifications (STCs)** | "List all Supplemental Type Certificates (STCs) or modifications installed on the aircraft. What aftermarket equipment (e.g., engine monitors, STOL kits) does this plane have?" |

---

## 6. Pro-Tips for NotebookLM Logbook Audits

1. **Targeting Multi-Engine/Twin Aircraft:** If evaluating a twin, add this modifier to your prompts: *"Please separate the data clearly into Left Engine/Propeller and Right Engine/Propeller systems."*
2. **Combating Poor OCR Quality:** Logbooks are frequently scanned PDFs with cursive handwriting or faded ink. If NotebookLM fails to find an event, guide it by asking for specific physical items (e.g., *"List all entries mentioning 'cylinder #3' or 'propeller'"*) instead of abstract concept terms like "damage history".
3. **Verify via Citations:** Always click NotebookLM's source citations to verify the context of its findings. A phrase like *"Checked for engine corrosion—none found"* might trigger a keyword hit for "corrosion" even though the result was positive.test

Ver: 1.0
Date: 6/28/2026
Copyright Locair.ai -- All rights reserved.
