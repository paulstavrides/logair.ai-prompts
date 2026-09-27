Using ONLY the information in the uploaded documents (maintenance logs
and TCDS), extract the following. If a piece of information is not
explicitly stated in the documents, write "NOT FOUND" — do not infer
or guess.

Ignore any source whose title begins with "CANDIDATE AD LIST". Those are
reference documents, not records of this aircraft.

1. Airframe: make, model, serial number, year of manufacture.
   Use the exact text string as it appears in the TCDS header.

2. Engine: currently installed make, model, serial number.
   If the logs record an engine replacement, use the replacement engine.
   If an STC number is associated with the replacement, include it.

3. Propeller: make, model, serial number if recorded.

4. Magnetos: make and model for each magneto. If left and right magnetos
   differ, list both, in that order, and mark each with its position in
   parentheses, e.g. "10-357230-1 (Left) / 10-357230-2 (Right)".

5. ELT (emergency locator transmitter): make, model, battery type if
   recorded.

6. STCs: list every STC number mentioned anywhere in the logs or TCDS.
   Include the description exactly as written in the document.

7. AD compliance entries: every AD number mentioned in the logs with
   its compliance date. Copy the AD number exactly as written. If
   compliance is tracked by Hobbs/tach time instead of a calendar date,
   write the value as "<number> (Hobbs)" instead of a date.

8. Any 337 major alteration entries: date and description.

9. Current aircraft time: total airframe time (TTAF), flight Hobbs, and
   Hobbs meter reading, each as of the most recent logbook entry, plus
   heater Hobbs time if the aircraft has a separate heater hour meter.

10. Any equipment known to have been REMOVED and not replaced
    (e.g. heaters, specific avionics, original components replaced by STC).

11. Installed equipment: every appliance or accessory currently installed,
    as recorded in the logs, with make, model, part number, and serial
    number. Leave out anything listed under Removed Equipment. Cover at
    least these categories, one line per unit:
    - Avionics: nav/com, GPS, transponder, audio panel, autopilot and its
      servos, displays, AHRS, traffic/terrain systems, ADS-B equipment
    - Instruments: altimeter, airspeed, attitude, directional gyro, turn
      coordinator, vertical speed, engine and fuel gauges and senders
    - Restraints: seat belts and shoulder harnesses
    - Fuel system: fuel pumps, fuel injection servos and nozzles, fuel
      selector valves, fuel quantity senders
    - Vacuum/pneumatic: vacuum pumps, vacuum regulators
    - Electrical: alternators, starters, voltage regulators, batteries,
      ignition switches, circuit breakers
    - Engine accessories: oil filters and adapters, induction air filters,
      propeller governors, oil coolers
    - Lighting: beacons, strobes, landing and taxi lights
    - Cabin: combustion heaters, fire extinguishers, oxygen equipment
    - Landing gear: wheels, brakes, tires
    If a unit is fitted to one engine or one side only, give its position.
    Magnetos and the ELT have their own sections above; do not repeat
    them here.

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

## Magnetos
- Make:
- Model:

## ELT
- Make:
- Model:
- Battery Type:

## Installed STCs
- [STC number]: [description as written in document]

## AD Compliance on Record
- [AD number]: [compliance date, or "<value> (Hobbs)" if Hobbs-based]

## Major Alterations (337s)
- [date]: [description as written in document]

## Total Time / Current Aircraft
- TTAF: [value] Hours
- Hobbs: [value] Hours
- Flight Hobbs: [value] Hours (FLT Hobbs) [omit if the aircraft has only one Hobbs meter]
- Heater Hobbs: [value] Hours [omit if not applicable]

## Removed Equipment
- [equipment as written in document]

## Installed Equipment
- [Category] | [Make] | [Model] | [Part Number] | [Serial Number] | [Position]
  (one line per unit; write NOT FOUND for any unknown field, and "-" for
  Position when it does not apply)

## Agent Notes
- [any configuration changes, component replacements, or ambiguities
  found in the documents that may affect AD applicability]

**Version:** 1.4  
**Date:** 9/26/26
**Copyright** LogAir.ai -- all rights reserved
