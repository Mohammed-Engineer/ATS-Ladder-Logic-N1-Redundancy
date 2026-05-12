# ATS Automatic Transfer Switch
# N+1 Redundancy Ladder Logic

## About
Automatic Transfer Switch control system
designed in ladder logic for mission
critical facilities including data centers
hospitals and banks.

## Scenario
One main supply from transformer
One backup generator
Automatic changeover on main supply failure

## What It Does
- Main supply fails → CB1 opens automatically
- Generator starts automatically
- 10 second stabilisation timer
- CB2 closes → Generator powers building
- Alarm sounds → Engineer notified
- Main supply returns → Transfer back automatically
- Safety interlock prevents both supplies
  connecting simultaneously

## Rungs
- Rung 1: Normal operation CB1 control
- Rung 2: Generator start on main failure
- Rung 3: Generator stabilisation timer 10s
- Rung 4: CB2 close after timer
- Rung 5: Safety interlock CB1 and CB2
- Rung 6: Alarm when generator running
- Rung 7: Return timer on main restoration
- Rung 8: Transfer back to main supply

## Redundancy
N+1 Configuration
N = Main transformer supply
+1 = Backup generator
Zero downtime for critical loads!

## Platform
PLC Fiddle Simulator
Ladder Logic — IEC 61131-3 Standard
