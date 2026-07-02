# PUBG Sensitivity Calculator

A multilingual PUBG sensitivity calculator for ADS sensitivity, DPI conversion, vertical multiplier, scope sensitivity, PUBG-style eDPI, and resolution/aspect ratio changes.

Created by **Lokx_x**

## Features

- ADS sensitivity conversion
- DPI conversion
- PUBG-style eDPI calculation
- Vertical sensitivity multiplier calculation
- Scope sensitivity calculation
- Resolution / aspect ratio conversion
- Offline HTML version
- Excel version
- Multilingual support:
  - Korean
  - English
  - Japanese
  - Simplified Chinese
  - Traditional Chinese
  - Russian

## About PUBG-style eDPI

PUBG’s in-game sensitivity scale is not a simple linear value.

Based on PUBG configuration values such as `LastConvertedSensitivity`, the internal converted sensitivity appears to follow this formula:

```text
ConvertedSensitivity ≈ 0.002 × 10^(Sensitivity / 50)
```

This means that increasing the PUBG sensitivity value by 15 almost doubles the converted sensitivity:

```text
10^(15 / 50) ≈ 1.995
```

Because of this, this calculator does not use the simple `DPI × sensitivity` method.

Instead, it converts PUBG sensitivity into a more intuitive **PUBG-style eDPI** value where:

- the same perceived PUBG sensitivity is shown as the same eDPI
- 2x perceived PUBG speed is shown as 2x eDPI

The goal is not to define the “best sensitivity,” but to make it easier to compare settings when changing DPI, ADS sensitivity, vertical multiplier, scope sensitivity, resolution, or aspect ratio.

## Important Note

This tool is mainly focused on **PUBG-internal sensitivity conversion**.

It is not intended to be a perfect cross-game sensitivity converter for games like Valorant, CS, or Overwatch.

Cross-game conversion requires reliable yaw / deg-per-count / cm/360 reference values, FOV behavior, and other game-specific factors. If a cross-game reference feature is added in the future, it will be labeled as an estimated starting point rather than a perfect 1:1 conversion.

## Web Version

The web version is a single HTML file and works offline.

No installation required.  
Just open `index.html` in your browser.

You can also use the GitHub Pages version directly:

https://lokx-x.github.io/pubg-sensitivity-calculator/

## Credits

Created by **Lokx_x**  
Localization & Web Version by **ChatGPT (OpenAI)**
