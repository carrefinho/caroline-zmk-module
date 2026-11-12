# Caroline

ZMK shield for Caroline, a 36-key electrostatic-capacitive keyboard with no
analog front end. It takes a Seeed XIAO Plus module and scans with
[zmk-ec-direct](https://github.com/carrefinho/zmk-ec-direct).

One shield, `caroline`, covers three controllers. The pins and tuning for each
are in `boards/shields/caroline/boards/`.

| Controller | Board | JP1-JP4 | Power |
|---|---|---|---|
| XIAO nRF52840 Plus | `xiao_ble//zmk` | A-C | Battery or USB, BLE |
| XIAO SAMD21 Plus | `seeeduino_xiao` | C-B | USB only |
| XIAO RP2040 Plus | `xiao_rp2040//zmk` | A-C | USB only |

The jumpers choose whether each row is one sense line of ten keys (A-C) or two
of five (C-B). They have to match the controller.

Every key must be up when the board powers on. That is when it takes its
released baselines.
