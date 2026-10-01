```markdown
# AGHub Single Unit Electrical Harness Schematic

========================================================================================
AGHUB CORE ELECTRICAL HARNESS SCHEMATIC (SINGLE UNIT)

[ SOLAR ARRAY: 20kW TOPCon ]
│
├─► [ String 1: 500VDC / 20A ] ──┐
├─► [ String 2: 500VDC / 20A ] ──┼──► [ 100A DC Main Fused Isolator ]
└─► [ String 3: 500VDC / 20A ] ──┘                 │
▼
[ MPPT Charge Controller ]
(150V–600V DC Input)
│
▼
[ Common 48VDC Power Bus ] ◄───┐
│                  │
┌──────────────────────────────────────────┴──────┐           │
▼                                                 ▼           │
[ 20kWh LFP Battery Module ]                    [ 15kW Pure Sine Inverter ] │
(Integrated Master BMS & Shunt)                 (48VDC to 230VAC 1-Phase)  │
│                                                 │           │
▼                                                 ▼           │
[ RS-485 Modbus Telemetry ]                      [ AC Sub-Panel / Breakers ]│
│                                                 │           │
│         ┌───────────────────────────────────────┼───────────┘
│         │                                       │
│         ▼                                       ▼
│   [ LED Grow Drivers ]                   [ Inverter HVAC ]
│   (4 x 2.5kW Dimming)                    (4kW Inverter AC)
│         │                                       │
│         ▼                                       ▼
│   [ LED Array Racks ]                    [ Climate / Exhaust ]
│                                                 │
│                                                 ▼
│                                          [ Main Water Pump ]
│                                          (Variable-Freq VFD)
│                                                 │
└─────────────────────────┬───────────────────────┘
▼
[ Edge System Controller (ARM64) ]
(Optically Isolated I/O & Sensors)
│
▼
[ Starlink Satellite Terminal ]


## System Component Electrical Ratings

| Sub-System | Voltage Input / Output | Current Draw / Capacity | Wire Gauge / Protection |
| :--- | :--- | :--- | :--- |
| **PV Arrays** | 500 VDC Input | 20A per String (3 Strings) | 10 AWG Solar Cable (PV-1F) |
| **Main DC Bus** | 48 VDC Nominal | 300A Max Continuous | 4/0 AWG Marine Flexible Cable |
| **LFP Battery Bank** | 48 VDC (16S Configuration) | 200A Max Discharge | 2/0 AWG with 250A Class T Fuse |
| **Main AC Output** | 230 VAC 1-Phase (50/60Hz) | 65A Max Continuous Load | 6 AWG THHN Conduit Enclosed |
| **LED Array Circuit**| 48 VDC Constant Current | 200W per Bar (50 Bars Total)| 14 AWG Multi-Conductor Tray
