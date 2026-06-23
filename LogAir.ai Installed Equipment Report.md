Using ONLY the information in the uploaded documents (maintenance logs
and TCDS), extract the following. If a piece of information is not
explicitly stated in the documents, write "NOT FOUND" — do not infer
or guess.

1. Airframe: make, model, serial number, year of manufacture.
   Use the exact text string as it appears in the TCDS header.

2. Engine: currently installed make, model, serial number.
   If the logs record an engine replacement, use the replacement engine.
   If an STC number is associated with the replacement, include it.

3. Propeller: make, model, serial number if recorded.

4. STCs: list every STC number mentioned anywhere in the logs or TCDS.
   Include the description exactly as written in the document.

5. AD compliance entries: every AD number mentioned in the logs with
   its compliance date. Copy the AD number exactly as written.

6. Any 337 major alteration entries: date and description.

7. Current aircraft total time (Hobbs or tach hours)

8. Any equipment known to have been REMOVED and not replaced
     (e.g. heaters, specific avionics, original components replaced by STC)

9. ELT make, model, and battery type if recorded

10. Magneto make and model (current, after any replacements)


Do not use any manufacturer names, model designations, or AD numbers
that do not appear verbatim in the uploaded documents.

Format your response as markdown using this structure:

# Aircraft Configuration — [N-Number if found, otherwise NOT FOUND]

## Airframe
- Make:
- Model:
- Serial Number:
- Year:

## Engine
- Make:
- Model:
- Serial Number:
- STC (if replacement):

## Propeller
- Make:
- Model:
- Serial Number:

## Installed STCs
- [STC number]: [description as written in document]

## AD Compliance on Record
- [AD number]: [compliance date]

## Major Alterations (337s)
- [date]: [description as written in document]

## Agent Notes
- [any configuration changes, component replacements, or ambiguities
  found in the documents that may affect AD applicability]


**Version:** 1.0  
**Date:** 6/23/26
**Copyright** LogAir.ai -- all rights reserved
