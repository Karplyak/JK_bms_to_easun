# JK_bms_to_easun
Try connect jk bms to inverter Easun 

# Schematics
```
                  RS485                      UART                        UART                     RS485/UART
┌────────────┐              ┌──────────┐                ┌─────────┐                ┌───────────┐              ┌───────────┐
│            │              │          │<----- RX ----->│         │<----- RX ----->│ RS485 to  │<-----B- ---->│ Inverter  │
│     JK     │<-----B- ---->│  RS485   │<----- TX ----->│ ESP32/  │<----- TX ----->│ TTl module│<---- A+ ---->│   EASUN   │
│     BMS    │<---- A+ ---->│  to TTL  │<----- GND ---->│ ESP8266 │<- 3.3V / GND ->└───────────┘              │  ISOLAR   │
│            │<--- GND ---->│  module  │<----- 3.3V --->│         │<-- --------------------------- VCC / GND -│ smh-ii-4.2│
│            │              │          │                │         │<- 3.3V / GND ->┌───────────┐              │           │
└────────────┘              └──────────┘                │         │<----- RX ----->│ RS232 to  │<---- RX ---->│           │
                                                        │         │<----- TX ----->│ TTl module│<---- TX ---->│           │
                                                        └─────────┘                └───────────┘              └───────────┘
```

# References
* https://github.com/syssi/esphome-seplos-bms
