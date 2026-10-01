# AGHub Anti-Sabotage & Physical Security Specification

## 1. Fluid System Protection

Operating in unmonitored environments requires zero-trust fluid containment to prevent water theft, siphon attempts, or contamination.

* **Internal Sump Reservoir:** Sump tanks are structurally integrated beneath the lower Corten container floor structure. Access requires heavy equipment unbolting from inside the unit.
* **Armored Conduit Sheathing:** All external water supply lines (from deep wells or between linked units) run inside Schedule-80 structural steel pipe sheathing fastened with anti-tamper security bolts.
* **Automated Hydraulic Lockout Valve System:** Normally Closed (NC) motorized brass solenoid valves are installed at all bulkhead connections.

*                           [ Differential Flow Detection ]
                                           │
                                           ▼
         ┌──────────────────────────────────────────────────────────────────┐
         │ Supply Flowmeter (F1) vs. Return Flowmeter (F2) Variance > 2%    │
         └────────────────────────────────┬─────────────────────────────────┘
                                          │
                                          ▼
                         [ AUTOMATED VALVE TRIP SIGNAL ]
                                          │
                                          ▼
                        [ Motorized Solenoids Lock (500ms) ]
                                          │
                                          ▼
                       [ Starlink GPS Intrusion Alert Sent ]

---

## 2. Electrical & Enclosure Hardening

* **Microswitch Tamper Loops:** High-voltage distribution boards, access doors, and inverter bays feature NC microswitches wired into the ARM edge computer's digital inputs. Opening a panel without a signed maintenance key trips an alert.
* **Hard-Brick Charge Lockout:** Unauthorized intrusion triggers an immediate software shutdown of solar charge controllers and battery BMS discharge gates, disabling the system until reset via remote Starlink command.
* **Glass-Glass Solar Array Armor:** Solar canopies utilize double-tough tempered TOPCon modules mo
