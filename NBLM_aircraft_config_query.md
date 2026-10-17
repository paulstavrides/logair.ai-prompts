Using ONLY the information in the uploaded documents (maintenance logs
and TCDS), extract the following. If a piece of information is not
explicitly stated in the documents, write "NOT FOUND" — do not infer
or guess. Ignore any source whose title begins with "CANDIDATE AD LIST".
Do not use any manufacturer names, model designations, or AD numbers
that do not appear verbatim in the documents.

1. Airframe: make, model, serial number, year of manufacture, exactly as
   in the TCDS header.
2. Engine: currently installed make, model, serial number. If the logs
   record an engine replacement, use the replacement engine and give any
   STC number associated with it.
3. Propeller: make, model, serial number if recorded.
4. Magnetos: make and model of each. If left and right differ, list both,
   left first, each marked with its position, e.g.
   "10-357230-1 (Left) / 10-357230-2 (Right)".
5. ELT: make, model, battery type if recorded.
6. STCs: every STC number in the logs or TCDS, with its description
   exactly as written.
7. AD compliance: every AD number in the logs, copied exactly, with its
   compliance date, or "<number> (Hobbs)" if tracked by Hobbs/tach time.
8. 337 major alterations: date and description.
9. Current time as of the latest entry: TTAF, Hobbs, flight Hobbs, and
   heater Hobbs if there is a separate heater meter.
10. Equipment REMOVED and not replaced.

Reply in this markdown:

# Aircraft Configuration — [N-Number or NOT FOUND]
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
- [STC number]: [description]
## AD Compliance on Record
- [AD number]: [date, or "<value> (Hobbs)"]
## Major Alterations (337s)
- [date]: [description]
## Total Time / Current Aircraft
- TTAF: [value] Hours
- Hobbs: [value] Hours
- Flight Hobbs: [value] Hours [omit if only one Hobbs meter]
- Heater Hobbs: [value] Hours [omit if not applicable]
## Removed Equipment
- [equipment as written]
## Agent Notes
- [configuration changes, component replacements, or ambiguities that
  may affect AD applicability]

<!-- NEXT QUESTION -->

Using ONLY the information in the uploaded documents (maintenance logs
and TCDS), list every appliance or accessory currently installed on the
aircraft, as recorded in the logs. If a piece of information is not
explicitly stated, write "NOT FOUND" — do not infer or guess. Ignore any
source whose title begins with "CANDIDATE AD LIST". Do not use any
manufacturer names or model designations that do not appear verbatim in
the documents.

Leave out equipment the logs record as removed and not replaced, and
leave out the airframe, engines, propellers, magnetos and ELT. Cover at
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

Type is what the unit is, in a few plain words (e.g. Transponder, Vacuum
pump, Shoulder harness). Position is the engine or side a unit is fitted
to, or "-" if that does not apply.

Reply with ONLY this markdown, no other text:

## Installed Equipment
- [Category] | [Type] | [Make] | [Model] | [Part Number] | [Serial Number] | [Position]

**Version:** 2.0  
**Date:** 10/17/26
**Copyright** LogAir.ai -- all rights reserved
