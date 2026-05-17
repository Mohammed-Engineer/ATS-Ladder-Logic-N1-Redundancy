
# âš¡ Automatic Transfer Switch â€” N+1 Redundancy
# PLC Ladder Logic

![PLC](https://img.shields.io/badge/PLC-Ladder_Logic-orange?style=for-the-badge)
![IEC 61131](https://img.shields.io/badge/IEC_61131--3-Standard-blue?style=for-the-badge)
![Critical Power](https://img.shields.io/badge/Critical_Power-N%2B1-red?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)

> ATS control system in PLC ladder logic for N+1 redundancy â€” automatic changeover from main supply to generator on failure. Designed for data centers, hospitals and mission critical facilities.

---

## ðŸ”„ How It Works

```
NORMAL:     Main Transformer â†’ CB1 CLOSED â†’ Building powered âœ…
FAILURE:    Main supply fails â†’ CB1 OPENS automatically
            Generator starts â†’ 10 second stabilisation timer
            CB2 CLOSES â†’ Generator powers building âœ…
            Alarm sounds â†’ Engineer notified ðŸš¨
RESTORE:    Main supply returns â†’ Transfer back automatically
SAFETY:     CB1 and CB2 NEVER close simultaneously â€” interlock active
```

---

## ðŸ“‹ Ladder Logic Rungs

| Rung | Function |
|---|---|
| Rung 1 | Normal operation â€” CB1 control |
| Rung 2 | Generator start on main supply failure |
| Rung 3 | Generator stabilisation timer â€” 10 seconds |
| Rung 4 | CB2 close after timer complete |
| Rung 5 | Safety interlock â€” CB1 and CB2 cannot close together |
| Rung 6 | Alarm activation when generator running |
| Rung 7 | Return timer on main supply restoration |
| Rung 8 | Transfer back to main supply |

---

## ðŸ—ï¸ N+1 Redundancy Configuration

| Component | Role |
|---|---|
| N | Main transformer supply â€” normal operation |
| +1 | Backup diesel generator â€” standby |
| Result | Zero downtime for critical loads âœ… |

**Applications:** Data Centers Â· Hospitals Â· Banks Â· Emergency Services

---

**Platform:** PLC Fiddle Simulator | **Standard:** IEC 61131-3 Ladder Logic  
**Author:** Mohammed Azam Ali MIET | Final Testing Engineer â€” Schneider Electric Leeds UK  
**GitHub:** github.com/Mohammed-Engineer
