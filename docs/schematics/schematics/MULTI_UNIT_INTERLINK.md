# AGHub Multi-Unit N+1 Interlink Topology

========================================================================================
SCALABLE MULTI-UNIT N+1 HIGH-POWER BUS INTERLINK SCHEMATIC

AGHUB UNIT #1                    AGHUB UNIT #2                    AGHUB UNIT #3
┌──────────────┐                 ┌──────────────┐                 ┌──────────────┐
│  48VDC LFP   │                 │  48VDC LFP   │                 │  48VDC LFP   │
│ Battery/BMS  │                 │ Battery/BMS  │                 │ Battery/BMS  │
└──────┬───────┘                 └──────┬───────┘                 └──────┬───────┘
│                                │                                │
▼                                ▼                                ▼
[ Direct DC Tie ]                [ Direct DC Tie ]                [ Direct DC Tie ]
(4/0 AWG Marine)                 (4/0 AWG Marine)                 (4/0 AWG Marine)
│                                │                                │
▼                                ▼                                ▼
[ Tamper Isolator ]              [ Tamper Isolator ]              [ Tamper Isolator ]
(Encased Lockout)                (Encased Lockout)                (Encased Lockout)
│                                │                                │
└────────────────────────┬───────┴────────────────────────┘
│
▼
====================================
COMMON HIGH-CAPACITY DC BUS BAR
====================================
│
├─────────────────────────────────┐
▼                                 ▼
[ Master Microgrid Hub ]          [ Regional Load / Pump ]
(Shared Battery Load Balancer)     (Extended Complex Infrastructure)

COMMUNICATION & CAN-BUS NETWORK (DAISY-CHAIN ISOLATED LOOP):

[ Edge Unit 1 ] ◄── CAN-Bus ──► [ Edge Unit 2 ] ◄── CAN-Bus ──► [ Edge Unit 3 ]
│                                                               │
└───────────────────────────────┬───────────────────────────────┘
▼
[ Master Gateway / Starlink ]
(Heartbeat Sync & Failover Control)


## Interconnect Hardware & Coupling Protocols

1. **Direct DC Power Tie:** Connected via high-current 4/0 AWG marine-grade flexible cables housed inside armored steel sleeves. Enables shared load balancing across adjacent units.
2. **Hydraulic Interlink Manifold:** Uses 2-inch quick-connect stainless steel camlock fittings linked to a common ultrafiltration loop.
3. **Control Communication Loop:** Optically isolated RS-485 / CAN-bus daisy chain running Modbus RTU pr
