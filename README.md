# PUBG Sensitivity Calculator v2.2

A multilingual sensitivity calculator for PUBG: BATTLEGROUNDS.

Created by **Lokx_x**  
Localization & Web Version by **ChatGPT (OpenAI)**

## Overview

PUBG Sensitivity Calculator helps convert and compare PUBG sensitivity settings across DPI, ADS sensitivity, vertical multiplier, scope sensitivity, resolution/aspect ratio changes, and 360° distance.

Version 2.2 adds an estimated 360° distance calculator and cross-game sensitivity reference for CS2, Valorant, and Overwatch.

This project is focused on PUBG-internal sensitivity conversion first. Cross-game values are intended as estimated starting points, not perfect 1:1 replacements for personal testing.

## Files

- `index.html`  
  Offline web version. Open it directly in a browser.

- `PUBG_Sensitivity_Calculator_v2.2.xlsx`  
  Excel version with multilingual sheets.

- `screenshots/`  
  Preview images for the web / Excel calculator.

## Supported Languages

- English
- 한국어
- 日本語
- 简体中文
- 繁體中文
- Русский

## Main Features

- PUBG vertical multiplier calculator
- DPI converter
- PUBG-style eDPI calculator
- Scope sensitivity helper
- Resolution / aspect-ratio reference
- 360° distance calculator
- PUBG state selection:
  - TPP General
  - FPP General
  - ADS (AR)
- FPP FOV selection from 80 to 103
- Aspect-ratio correction reference:
  - 16:9
  - 16:10
  - 21:9
  - 4:3
- Cross-game sensitivity reference:
  - CS2
  - Valorant
  - Overwatch

## PUBG Sensitivity Formula

PUBG's in-game sensitivity scale is not linear.

Based on PUBG configuration values such as `LastConvertedSensitivity`, the internal converted sensitivity appears to follow this formula:

```text
LastConvertedSensitivity ≈ 0.002 × 10^(Sensitivity / 50)
```

This means that increasing PUBG sensitivity by 15 almost doubles the converted sensitivity:

```text
10^(15 / 50) ≈ 1.995×
```

Because of this, this calculator does not use the simple `DPI × sensitivity` method for PUBG-style eDPI or sensitivity ratio conversion.

## PUBG-style eDPI

PUBG-style eDPI is designed to show PUBG sensitivity in a more intuitive relative scale.

It is based on PUBG's logarithmic sensitivity behavior, so:

- the same perceived PUBG sensitivity is shown as the same eDPI
- 2× perceived PUBG speed is shown as 2× eDPI
- DPI changes and PUBG sensitivity changes can be compared more naturally

## 360° Distance Formula

The v2.2 360° distance calculator uses the following estimated PUBG yaw formula:

```text
PUBG yaw ≈ 0.005 × 10^(Sensitivity / 50)
```

Base 360° distance:

```text
cm/360 = 360 × 2.54 / (DPI × yaw)
```

Final PUBG 360° distance:

```text
cm/360 = Base cm/360 × State/FOV Factor × Aspect Factor
```

## State / FOV Factors

The v2.2 web and Excel versions use empirical correction values based on PUBG config values, manual measurement, and reverse calculation.

### FPP General

```text
State/FOV Factor = (tan(45°) / tan(FOV / 2))^0.8
```

### TPP General

TPP is displayed as FOV 80 and uses the same style of correction:

```text
State/FOV Factor = (tan(45°) / tan(80° / 2))^0.8
```

### ADS (AR)

ADS uses a distance factor based on an estimated yaw multiplier of 0.8:

```text
ADS Distance Factor = 1.25
```

This is equivalent to treating ADS horizontal yaw as approximately 0.8× of the base yaw.

## Aspect-Ratio Factors

The v2.2 calculator uses the following aspect-ratio distance factors:

```text
16:9  = 1.0000
16:10 = 1.0000
21:9  = 0.8500
4:3   = 1.1667
```

Notes:

- 16:10 is treated as equivalent to 16:9 for horizontal 360° distance.
- 21:9 uses the existing 0.85 correction.
- 4:3 uses a revised 1.1667 correction instead of the older 1.3333 value.
- These values are unofficial estimates based on manual measurement and reverse calculation.

## Resolution / Aspect-Ratio Conversion Notes

The resolution conversion section uses practical approximations for PUBG users.

For 4:3 conversion, PUBG does not allow decimal sensitivity values. Because of this, the calculator uses a practical integer sensitivity approximation:

```text
16:9 → 4:3
Sensitivity: +3
Vertical Multiplier: ×1.166

4:3 → 16:9
Sensitivity: -3
Vertical Multiplier: ÷1.166
```

The exact horizontal correction would be closer to:

```text
50 × log10(1.1667) ≈ +3.34 sensitivity
```

However, because PUBG only accepts integer sensitivity values, `+3` is used as a practical in-game setting.

## Cross-game Reference

The cross-game section converts the estimated PUBG 360° distance into a target-game sensitivity using each game's yaw reference.

Included target games:

```text
CS2       yaw 0.022,  FOV 90 (4:3 Base)
Valorant  yaw 0.07,   FOV 103
Overwatch yaw 0.0066, FOV 103
```

Cross-game sensitivity conversion is only a starting point. Different games may handle FOV, zoom, ADS, recoil, animation, camera behavior, and monitor-distance matching differently.

## Important Disclaimer

This is an unofficial community-made calculator.

The 360° distance values, yaw estimates, state/FOV factors, and aspect-ratio factors are based on:

- PUBG configuration values
- manual measurement
- reverse calculation
- practical in-game testing

They are **not official PUBG/KRAFTON reference values**.

Use the results as an estimated starting point and verify with your own in-game testing.

## Version 2.2 Changes

### Added

- 360° distance calculator
- PUBG state selector: TPP / FPP / ADS
- FPP FOV selector
- PUBG yaw display
- state/FOV correction display
- aspect-ratio correction display
- CS2 / Valorant / Overwatch sensitivity reference

### Changed

- Updated aspect-ratio correction values:
  - 16:10 now treated as 16:9 for horizontal distance
  - 4:3 changed from older 1.3333-style correction to 1.1667
  - 21:9 remains 0.85
- Updated FPP/TPP FOV correction to use `tan(FOV/2)^0.8` style empirical correction
- ADS calculation changed to a yaw ×0.8 / distance ×1.25 style estimate
- 4:3 resolution conversion updated to practical PUBG integer sensitivity logic:
  - sensitivity ±3
  - vertical multiplier ×/÷1.166

### Notes

Version 2.2 is a major calculation update. Older v2.1 values may differ, especially for 360° distance, FOV behavior, ADS behavior, and 4:3 conversion.

## License

MIT License

