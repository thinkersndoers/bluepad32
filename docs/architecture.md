# Bluepad32 Architecture

WIP

```
  ┌──────────────┐ ┌──────────┐ ┌──────────┐ ┌─────────────┐ ┌──────────┐
  │              │ │  NINA /  │ │          │ │             │ │          │
  │ Unijoysticle │ │  AirLift │ │ Arduino  │ │ MightyMiggy │ │ Custom   │      Platforms
  │              │ │          │ │          │ │             │ │          │
  └────────┬─────┘ └────┬─────┘ └────┬─────┘ └─────┬───────┘ └───┬──────┘
           │            │            │             │             │
           │            │            │             │             │
      ┌────▼────────────▼────────────▼─────────────▼─────────────▼─┐
      │                                                            │
      │                                                            │
      │                                                            │           Firmware
      │                          Bluepad32                         │
  ┌───┤                                                            │
  │   │                                                            │
  │   │                                                            │
  │   └─────┬──────────────────┬──────────────┬─────────────────┬──┘
  │         │                  │              │                 │
  │         │                  │              │                 │
  │         │   ┌──────────────▼────────────┐ │                 │
  │         │   │                           │ │                 │
  │         │   │           BTstack         ├─┼──────────────┐  │              Bluetooth Stack
  │         │   │                           │ │              │  │
  │         │   └────┬──────┬─────────┬─────┘ │              │  │
  │         │        │      │         │       │              │  │
  │         │        │      │         │       │              │  │
  │      ┌──▼────────▼───┐  │         │       │              │  │
  │      │               │  │         │       │              │  │
  │      │   FreeRTOS    │  │         │       │              │  │
  │      │               │  │         │       │              │  │
  │      └──────┬────────┘  │         │       │              │  │
  │             │           │         │       │              │  │
┌─▼─────────────▼───────────▼─┐ ┌─────▼───────▼──┐ ┌─────────▼──▼──────────┐
│                             │ │                │ │                       │
│            ESP-IDF          │ │    Pico SDK    │ │    Posix / libusb     │    Operating System
│                             │ │                │ │                       │
└────────────────┬────────────┘ └────────┬───────┘ └───────────┬───────────┘
                 │                       │                     │
                 │                       │                     │
┌────────────────▼────────────┐ ┌────────▼───────┐ ┌───────────▼───────────┐
│                             │ │                │ │                       │
│                             │ │                │ │                       │
│         ESP32 family        │ │  Raspberry Pi  │ │         Posix         │
│                             │ │                │ │                       │     Hardware
│     ESP32, ESP32-S3, etc    │ │  Pico W family │ │      Linux, macOS     │
│                             │ │                │ │                       │
│                             │ │                │ │                       │
└─────────────────────────────┘ └────────────────┘ └───────────────────────┘
```

Made with: <https://asciiflow.com/>
