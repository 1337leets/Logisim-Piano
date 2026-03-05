# Logisim Piano

A chromatic piano simulation built in Logisim Evolution using a Priority Encoder, MUX, and Buzzer.

## Versions

- **simple_piano:** 8-key diatonic (Do to Do2)
- **chromatic_piano:** 16-key chromatic starting from La3 (220 Hz) to Do5 (523 Hz)

## Design

Each key is mapped to a button. The Priority Encoder converts the active button to a 4-bit select signal, which drives a 14-bit MUX to output the corresponding frequency to the Buzzer. Volume is controlled via a slider.

### Signal Flow
```
Button → Priority Encoder → MUX → Buzzer (Frequency)
OR gate (any button active) → Buzzer Enable
Slider → Buzzer Volume
```

## Frequency Table

| Key | Note | Frequency (Hz) | Hex |
|-----|------|----------------|-----|
| 0 | La3 | 220 | 0x0DC |
| 1 | La3# | 233 | 0x0E9 |
| 2 | Si3 | 247 | 0x0F7 |
| 3 | Do4 | 262 | 0x106 |
| 4 | Do4# | 277 | 0x115 |
| 5 | Re4 | 294 | 0x126 |
| 6 | Re4# | 311 | 0x137 |
| 7 | Mi4 | 330 | 0x14A |
| 8 | Fa4 | 349 | 0x15D |
| 9 | Fa4# | 370 | 0x172 |
| 10 | Sol4 | 392 | 0x188 |
| 11 | Sol4# | 415 | 0x19F |
| 12 | La4 | 440 | 0x1B8 |
| 13 | La4# | 466 | 0x1D2 |
| 14 | Si4 | 494 | 0x1EE |
| 15 | Do5 | 523 | 0x20B |

## Tools
Logisim Evolution v4.1.0
