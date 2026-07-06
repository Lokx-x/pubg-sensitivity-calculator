# PUBG Sensitivity Calculator User Manual

Based on: PUBG Sensitivity Calculator v2.2  
Created by: Lokx_x  
Documentation support: ChatGPT (OpenAI)

---

## 0. About this document

This is the English user manual for PUBG Sensitivity Calculator.

This calculator was created to help with DPI conversion, vertical sensitivity adjustment, resolution/aspect-ratio conversion, scope sensitivity recommendations, 360° Distance calculation, and cross-game reference conversion while taking PUBG’s non-linear sensitivity behavior into account.

The calculated values are not “perfect answers.” They should be treated as practical starting points.  
PUBG sensitivity feel can vary depending on DPI, polling rate, in-game sensitivity, FOV, aspect ratio, mousepad, mouse feet, LOD, wrist/arm aiming style, and recoil-control habits.

After applying any calculated value, it is recommended to test it in Training Mode, Arcade, or real matches and fine-tune it manually.

---

# 1. Quick Start

## 1-1. Which feature should I use?

### When you want to slightly change ADS or scope sensitivity while keeping your vertical recoil control feel

Use **Vertical Sensitivity Calculator**.

Use this when you want to raise or lower ADS/scope sensitivity slightly while preserving your existing vertical recoil control feel as much as possible.

---

### When you want to change DPI while keeping a similar PUBG sensitivity feel

Use **DPI Converter**.

For example, when switching from 400 DPI to 800 DPI or 1600 DPI, this feature calculates a PUBG in-game sensitivity close to your previous feel.

---

### When you want to check your sensitivity range using PUBG-style eDPI

Check **PUBG-style eDPI**.

Because PUBG sensitivity cannot be accurately compared using simple `DPI × in-game sensitivity`, this calculator uses PUBG-style eDPI based on PUBG’s logarithmic sensitivity behavior.

---

### When changing aspect ratio such as 16:9, 16:10, 21:9, or 4:3

Use **Resolution / Aspect Ratio Converter**.

This provides sensitivity and vertical sensitivity correction values when changing aspect ratio.

---

### When you want recommended 2x/3x full-auto AR sensitivity

Use **Scope Sensitivity Calculator**.

It estimates recommended 2x and 3x full-auto AR sensitivity based on your Scope Mode Sensitivity, Vertical Sensitivity, and DPI.

---

### When you want to know your PUBG cm/360

Use **360° Distance Calculator**.

It shows how many centimeters you need to move your mouse for a full 360° turn with your current PUBG settings.

---

### When you want to convert PUBG sensitivity to CS2, Valorant, or Overwatch as a reference

Use **Cross-game Sensitivity Converter**.

It converts your PUBG setting into a reference sensitivity for other FPS games based on cm/360.

---

## 1-2. The most important thing to know

PUBG sensitivity is not a simple linear sensitivity system.

In many FPS games, sensitivity is often compared using:

```text
eDPI = DPI × in-game sensitivity
```

However, PUBG’s in-game sensitivity value does not increase linearly. PUBG sensitivity behaves closer to a logarithmic scale, and +15 sensitivity is almost equal to a 2x change.

Therefore, PUBG needs a calculator that reflects PUBG’s own sensitivity scaling rather than relying only on simple eDPI.

---

## 1-3. Should I use the calculated value as-is?

Use the calculated value as a starting point.

PUBG sensitivity feel is affected by many factors:

```text
- DPI
- Polling rate
- In-game sensitivity
- FOV
- Aspect ratio
- Scope state
- Scope zoom state
- Wrist/arm aiming style
- Mousepad and mouse feet
- LOD
- Recoil-control habits
```

The calculator helps you find a theoretically close starting point. The final setting should be tested and adjusted in-game.

---

# 2. Vertical Sensitivity Calculator

## 2-1. When should I use this?

Vertical Sensitivity Calculator calculates a recommended Vertical Sensitivity value when you change ADS or scope sensitivity while trying to preserve your previous vertical recoil-control feel.

Use it especially when:

```text
You like your current vertical recoil control,
but horizontal shake feels too strong and you want to lower ADS/scope sensitivity slightly.

or

Tracking moving targets or leading shots feels too slow,
so you want to raise ADS/scope sensitivity slightly.
```

The core idea is:

```text
Change ADS/scope sensitivity,
while keeping vertical recoil-control feel as close as possible.
```

---

## 2-2. Recommended adjustment range

This calculator is mainly recommended for changing ADS or scope sensitivity by about **1–3 sensitivity points**.

If you change sensitivity by 5 or more, the calculated vertical recoil control may still be close mathematically, but the following can change significantly:

```text
- Horizontal aiming feel
- First-shot aiming feel
- Lead-shot feel
- Vehicle spray
- Spray rhythm
- Hand pressure
```

Large sensitivity changes are closer to adapting to a new setting than fine-tuning an existing one.

---

## 2-3. Inputs

```text
Current Sensitivity
→ Your current ADS or scope sensitivity

Current Vertical Sensitivity
→ Your current vertical sensitivity

Target Sensitivity
→ The ADS or scope sensitivity you want to change to
```

The result is a recommended Vertical Sensitivity value that keeps your vertical recoil-control amount close to your original setting after changing to Target Sensitivity.

---

## 2-4. Example: lowering ADS sensitivity

Assume your current setting is:

```text
ADS Sensitivity: 35
Vertical Sensitivity: 0.78
```

You like your vertical recoil control, but horizontal shake feels slightly too strong, so you want to lower ADS sensitivity from 35 to 33.

If you only lower ADS from 35 to 33, vertical input becomes slower too. Your previous mouse pull-down movement may no longer control recoil enough.

In this case, increasing Vertical Sensitivity can bring the vertical recoil-control amount closer to the original feel.

```text
Current Sensitivity = 35
Current Vertical Sensitivity = 0.78
Target Sensitivity = 33
```

Apply the calculated Vertical Sensitivity and test AR sprays in-game.

---

## 2-5. Example: raising ADS sensitivity

You may want to raise ADS sensitivity from 35 to 38 because leading shots or tracking fast targets feels too slow.

When ADS sensitivity is raised, vertical input also becomes stronger. With the same mouse pull-down movement, the muzzle may be pulled down too much.

In this case, lowering Vertical Sensitivity can make the vertical recoil-control feel closer to the previous setting.

```text
Current Sensitivity = 35
Current Vertical Sensitivity = 0.78
Target Sensitivity = 38
```

Apply the calculated Vertical Sensitivity and test both AR spray and vehicle spray.

---

## 2-6. Practical tip: when +1 sensitivity is too fast, but the current value feels slightly slow

PUBG only allows integer sensitivity values, so your ideal value may feel like it sits between 35 and 36.

Example:

```text
Current setting:
ADS Sensitivity 35
Vertical Sensitivity 1.00

Problem:
During sprays, horizontal correction feels slightly slow.

Try ADS 36:
Now overall ADS sensitivity feels too fast.
```

In this situation, you can keep ADS Sensitivity at 35 and lower Vertical Sensitivity slightly.

Lowering Vertical Sensitivity increases the amount of downward mouse movement needed for recoil control. During that motion, horizontal correction input may feel relatively more active.

If ADS 36 is too fast and ADS 35 is slightly slow, try:

```text
Keep ADS Sensitivity 35
Lower only Vertical Sensitivity slightly
```

This can be useful when the general horizontal speed is acceptable, but micro-corrections during spraying feel slightly slow.

---

## 2-7. Practical tip: when -1 sensitivity is too slow, but the current value feels slightly fast

Conversely, your current sensitivity may feel slightly fast, but lowering it by 1 point may feel too slow.

Example:

```text
Current setting:
ADS Sensitivity 35
Vertical Sensitivity 1.00

Problem:
During sprays, horizontal movement feels slightly too fast.

Try ADS 34:
Now overall ADS sensitivity feels too slow.
```

In this case, you can keep ADS Sensitivity at 35 and raise Vertical Sensitivity slightly.

Raising Vertical Sensitivity reduces the amount of downward mouse movement needed for recoil control. This can reduce unwanted horizontal mixing during sprays and make the horizontal shake feel more stable.

If ADS 34 is too slow and ADS 35 is slightly fast, try:

```text
Keep ADS Sensitivity 35
Raise only Vertical Sensitivity slightly
```

This can be useful when you want to keep your current responsiveness but reduce excessive horizontal micro-shake during sprays.

---

## 2-8. Vertical Sensitivity feel by eDPI range

This is not an absolute rule, but a common feel pattern in AR sprays and scope usage.

High eDPI users:

```text
- Horizontal sensitivity is already fast
- If Vertical Sensitivity is too low, more downward hand movement is needed
- This can make horizontal micro-correction unstable during recoil control
- A somewhat higher Vertical Sensitivity can reduce required downward movement
- This may create more room for horizontal micro-correction
```

Low eDPI users:

```text
- Horizontal sensitivity is slow
- If Vertical Sensitivity is too high, downward input can interfere strongly
- Horizontal movement may feel restricted or stiff
- Not raising Vertical Sensitivity too much can allow freer horizontal movement
- Recoil control can feel more natural through hand movement
```

The final feel depends on mouse movement style, mousepad, mouse feet, LOD, and weapon handling style.

---

# 3. DPI Converter

## 3-1. When should I use this?

Use DPI Converter when you want to change DPI while keeping a similar PUBG sensitivity feel.

Examples:

```text
Changing from 400 DPI to 800 DPI
Changing from 400 DPI to 1600 DPI
Lowering from 1600 DPI to 800 DPI
```

---

## 3-2. Inputs

```text
Current DPI
→ Your current DPI

Current Sensitivity
→ Your current PUBG sensitivity

Target DPI
→ The DPI you want to change to
```

The result is the PUBG in-game sensitivity that should feel close to the original setting at the Target DPI.

---

## 3-3. Example

In PUBG, +15 sensitivity is almost equal to 2x. Therefore, if DPI is doubled, sensitivity should be lowered by about 15 to keep a similar feel.

```text
400 DPI / Sensitivity 35
≈ 800 DPI / Sensitivity 20
≈ 1600 DPI / Sensitivity 5
```

The reverse applies when lowering DPI.

```text
1600 DPI / Sensitivity 5
≈ 800 DPI / Sensitivity 20
≈ 400 DPI / Sensitivity 35
```

---

## 3-4. Notes on high DPI / low in-game sensitivity

High DPI + low in-game sensitivity can have benefits:

```text
- Denser input counts
- Micro-input may feel smoother
- Early AR ADS correction may feel more natural
- Vehicle spray tracking may feel easier
```

But PUBG has strong weapon recoil, so there are potential downsides:

```text
- If the sensor feels too sensitive, steady recoil control may become harder
- Tremor or unnecessary micro-input can be reflected more easily than low DPI
- PUBG’s integer sensitivity limit may become more noticeable at very low in-game sensitivity
- At 6x/8x full zoom, long-range micro-aiming can feel stepped
```

After changing DPI, do not only check 360° distance. Test AR spray, vehicle spray, and DMR single-shot correction too.

---

# 4. PUBG-style eDPI

## 4-1. What is it?

PUBG-style eDPI is a sensitivity comparison value that reflects PUBG’s logarithmic sensitivity behavior.

Normal eDPI is:

```text
Normal eDPI = DPI × in-game sensitivity
```

But since PUBG sensitivity is not linear, normal eDPI is not enough for accurate comparison.

This calculator uses:

```text
PUBG-style eDPI = DPI × 10^((Sensitivity - 11) / 50)
```

---

## 4-2. When is it useful?

PUBG-style eDPI is useful for:

```text
- Comparing different DPI/sensitivity combinations
- Comparing old and new sensitivity ranges
- Comparing your settings with other players
- Finding a similar sensitivity after changing DPI
```

---

## 4-3. Does the same eDPI mean the exact same feel?

No.

The overall rotation amount may be similar, but actual feel can differ depending on:

```text
- DPI
- In-game sensitivity
- Polling rate
- FOV
- Aspect ratio
- Scope zoom state
- LOD
- Mousepad/mouse feet
- Mouse movement habit
```

For example, 400 DPI with high in-game sensitivity and 1600 DPI with low in-game sensitivity can have similar eDPI, but the input texture can feel different.

---

# 5. Resolution / Aspect Ratio Converter

## 5-1. When should I use this?

Use this feature when changing PUBG aspect ratio and you want reference sensitivity and vertical sensitivity correction values.

Examples:

```text
16:9 to 16:10
16:9 to 21:9
16:9 to 4:3
4:3 back to 16:9
```

Changing resolution alone and changing aspect ratio are different.

```text
1920×1080 → 2560×1440
→ Resolution change within the same 16:9 aspect ratio

16:9 → 4:3
→ Aspect ratio change
```

Aspect ratio changes can affect field of view composition, target size on screen, recoil perception, and horizontal movement feel.

---

## 5-2. v2.2 correction values

The Excel v2.2 Resolution / Aspect Ratio Converter uses:

```text
16:9 → 16:10
No sensitivity change
Vertical Sensitivity ×1.11

16:10 → 16:9
No sensitivity change
Vertical Sensitivity ÷1.11

16:9 → 21:9
No sensitivity change
Vertical Sensitivity ×0.85

21:9 → 16:9
No sensitivity change
Vertical Sensitivity ÷0.85

16:9 → 4:3
Sensitivity +3
Vertical Sensitivity ×1.166

4:3 → 16:9
Sensitivity -3
Vertical Sensitivity ÷1.166
```

---

## 5-3. 16:9 ↔ 16:10

16:9 and 16:10 are treated the same for horizontal 360° distance.

However, the resolution converter applies Vertical Sensitivity correction to account for vertical view/recoil feel differences.

```text
16:9 → 16:10
No sensitivity change
Vertical Sensitivity ×1.11

16:10 → 16:9
No sensitivity change
Vertical Sensitivity ÷1.11
```

Horizontal rotation sensitivity is kept the same, while vertical recoil-control feel is corrected.

---

## 5-4. 16:9 ↔ 4:3

For 16:9 and 4:3 conversion, both sensitivity and vertical sensitivity are adjusted.

```text
16:9 → 4:3
Sensitivity +3
Vertical Sensitivity ×1.166

4:3 → 16:9
Sensitivity -3
Vertical Sensitivity ÷1.166
```

For 4:3, changing only Vertical Sensitivity did not match practical feel as well as adjusting both sensitivity and Vertical Sensitivity.

---

## 5-5. What to test after applying

After changing aspect ratio, test:

```text
- 180°/360° turn distance
- AR spray
- DMR single-shot correction
- Vehicle spray
- Close-range tracking
- Target size and recoil feel on screen
```

Aspect ratio changes affect not only cm/360 but also visual perception, so in-game testing is necessary.

---

# 6. Scope Sensitivity Calculator

## 6-1. When should I use this?

Scope Sensitivity Calculator estimates recommended 2x/3x full-auto AR sensitivity based on your Scope Mode Sensitivity, Vertical Sensitivity, and DPI.

Use it when:

```text
You do not know where to start for 2x full-auto AR sensitivity
You do not know where to start for 3x full-auto AR sensitivity
You want a 2x/3x starting point suitable for your sensitivity range
You want to reference real pro-player sensitivity tendencies
```

---

## 6-2. Inputs

```text
Scope Mode Sensitivity
→ The baseline scope mode sensitivity

Vertical Sensitivity
→ Your current Vertical Sensitivity

DPI
→ Your current mouse DPI
```

The calculator returns:

```text
PUBG-style eDPI including Vertical Sensitivity
Recommended 2x Sensitivity
Recommended 3x Sensitivity
```

---

## 6-3. What data are the recommendations based on?

The 2x/3x recommended sensitivities are not official PUBG conversion values.

They are practical estimates based on full-auto AR 2x/3x sensitivity settings used by current PUBG professional players.

Data process:

```text
1. Collect current PUBG pro players' DPI, Scope Mode Sensitivity, Vertical Sensitivity, and 2x/3x settings
2. Organize each player’s setting into PUBG-style eDPI ranges including Vertical Sensitivity
3. Compare how much higher 2x/3x sensitivity is set compared to Scope Mode Sensitivity in each range
4. Create a recommended 2x/3x sensitivity curve based on that tendency
```

Therefore, this feature should be treated as a starting point based on real pro-player setting tendencies, not an official formula.

Pro settings can change with patches, meta, equipment, and role, so the result should be used as a reference, not an absolute value.

---

## 6-4. How to interpret results

```text
2x Recommended Sensitivity
→ Starting point for 2x full-auto AR sensitivity in your sensitivity range

3x Recommended Sensitivity
→ Starting point for 3x full-auto AR sensitivity in your sensitivity range
```

These values do not make 2x/3x feel perfectly identical in every situation.

You may need to adjust depending on:

```text
- Whether you use 2x/3x mainly for AR spray
- Whether you also use them for DMR single shots
- How often you spray vehicles
- Wrist aiming or arm aiming
- High or low Vertical Sensitivity
- High or low eDPI
```

---

## 6-5. What to test after applying

After applying recommended sensitivity, test:

```text
- 2x mid-range AR spray
- 3x mid-range AR spray
- Vehicle spray
- Moving target lead shots
- DMR single-shot correction
```

The 2x/3x recommendations are primarily starting points for AR full-auto use. DMR-focused players may need to adjust manually.

---

## 6-6. 6x/8x full-zoom micro-aiming warning

At 6x and 8x full zoom, micro-aiming can feel stepped in very low scope sensitivity ranges.

For example, when aiming at a small head target beyond 200m, tiny mouse movement may not move the screen immediately, then suddenly jump by one or more pixels.

This issue is mainly felt in:

```text
- 6x full zoom
- 8x full zoom
- Very low scope sensitivity around 13 or below
- Small long-range targets
- Very tiny micro-adjustments
```

This should not be generalized to ADS, red dot, holo, 2x, 3x, or 4x in the same way.

Reducing zoom on 6x/8x may make the issue less noticeable than full zoom.

---

# 7. 360° Distance Calculator

## 7-1. When should I use this?

360° Distance Calculator shows how many centimeters you need to move your mouse for a full 360° turn with your current PUBG settings.

```text
Lower cm/360
→ Faster sensitivity

Higher cm/360
→ Slower sensitivity
```

This is useful for comparing physical rotation distance across different DPI/sensitivity combinations or different FPS games.

---

## 7-2. Inputs

```text
DPI
→ Your mouse DPI

Sensitivity
→ PUBG in-game sensitivity

PUBG State
→ TPP Hipfire / FPP Hipfire / ADS (AR)

FPP FOV
→ FOV used when FPP Hipfire is selected

Aspect Ratio
→ 16:9 / 16:10 / 21:9 / 4:3
```

**Hipfire** means the normal view state where you are holding a weapon but not aiming down sights. In other words, it is not ADS.

```text
TPP Hipfire
→ Third-person normal view without aiming down sights

FPP Hipfire
→ First-person normal view without aiming down sights

ADS (AR)
→ Right-click aim-down-sights state with an AR
```

ADS (AR) uses a separate correction because FOV and sensitivity feel differ from normal view.

---

## 7-3. Interpreting results

```text
PUBG yaw
→ Estimated horizontal rotation coefficient at current sensitivity

cm/360
→ Mouse movement distance needed for a 360° turn

State/FOV/Aspect correction
→ Correction based on TPP/FPP/ADS state and aspect ratio
```

cm/360 is useful for sensitivity comparison, but it does not fully describe aiming feel.

Even with the same cm/360, the feel may differ due to FOV, aspect ratio, scope zoom, recoil pattern, LOD, and mouse movement style.

---

# 8. Cross-game Sensitivity Converter

## 8-1. When should I use this?

Cross-game Sensitivity Converter calculates reference sensitivities for CS2, Valorant, and Overwatch based on your PUBG 360° Distance.

---

## 8-2. How to use

```text
1. Enter PUBG DPI and sensitivity.
2. Select PUBG State, FOV, and Aspect Ratio.
3. Select the target game.
4. Enter the DPI you will use in the target game.
5. Check the converted sensitivity.
```

---

## 8-3. Notes

Cross-game values are not perfect 1:1 conversions.

Games differ in:

```text
- FOV
- Zoom behavior
- ADS behavior
- Movement speed
- Recoil pattern
- Character model size
- Engagement distance
- Mouse input handling
```

Use the converted value as a starting point for another game.

---

# 9. Recommended Testing Routine

## 9-1. Common testing routine after changing sensitivity

After using any calculator feature, test in this order:

```text
1. 180°/360° turn distance
2. AR ADS spray
3. 2x/3x mid-range spray
4. DMR single-shot correction
5. Vehicle spray
6. Moving target lead shots
7. 6x/8x full-zoom long-range micro-aiming
```

---

## 9-2. Do not change too many variables at once

If you change sensitivity, DPI, Vertical Sensitivity, resolution, and aspect ratio all at once, it becomes difficult to tell which change caused the difference in feel.

Change one variable at a time when possible.

```text
Good examples:
Change only DPI
Change only ADS sensitivity
Change only Vertical Sensitivity
Change only aspect ratio

Bad example:
Change DPI + ADS sensitivity + Vertical Sensitivity + aspect ratio all at once
```

---

# 10. FAQ

## Q1. Why use PUBG-style eDPI instead of normal eDPI?

Because PUBG sensitivity is closer to logarithmic than linear.

Normal eDPI uses `DPI × in-game sensitivity`, but PUBG’s in-game sensitivity number does not map linearly to actual sensitivity.

---

## Q2. Is +15 sensitivity really almost 2x?

Yes, almost.

```text
10^(15 / 50) ≈ 1.995
```

---

## Q3. How much should I lower sensitivity when changing from 400 to 800 DPI?

Lower it by about 15.

```text
400 DPI / Sensitivity 35
≈ 800 DPI / Sensitivity 20
```

---

## Q4. How much should I lower sensitivity when changing from 400 to 1600 DPI?

Since DPI becomes 4x, lower sensitivity by about 30.

```text
400 DPI / Sensitivity 35
≈ 1600 DPI / Sensitivity 5
```

---

## Q5. Does the same PUBG-style eDPI mean exactly the same sensitivity?

No.

Overall rotation amount may be similar, but feel can differ due to DPI, in-game sensitivity, polling rate, FOV, aspect ratio, scope zoom, LOD, and more.

---

## Q6. Is 1600 DPI low sensitivity always better than 400 DPI high sensitivity?

No.

1600 DPI + low in-game sensitivity can feel smoother for micro-input, but PUBG has strong recoil. If the sensor feels too sensitive, steady recoil control can become harder.

At low sensitivity values, 6x/8x full-zoom long-range micro-aiming may also feel stepped.

---

## Q7. Do I need correction when changing from 16:9 to 16:10?

In the resolution converter:

```text
16:9 → 16:10
No sensitivity change
Vertical Sensitivity ×1.11

16:10 → 16:9
No sensitivity change
Vertical Sensitivity ÷1.11
```

However, in the 360° Distance horizontal distance calculation, 16:10 is treated the same as 16:9.

---

## Q8. Are the scope sensitivity recommendations official?

No.

The 2x/3x recommended sensitivities are practical estimates based on current PUBG pro players’ full-auto AR 2x/3x sensitivity settings.

Use them as starting points, not official conversions.

---

## Q9. Are cross-game conversion values accurate?

They are cm/360-based reference values.

Since every game differs in FOV, zoom, recoil, movement speed, character model size, and engagement distance, they are not perfect 1:1 conversions.

---

## Q10. Is this calculator official?

No.

This is an unofficial tool based on PUBG config values, manual testing, reverse-calculated reference values, and pro-player setting data. It is not an official PUBG/KRAFTON calculator.

---

# 11. Technical Notes

This section is for users who want to understand the background logic. It is not required for using the calculator.

---

## 11-1. PUBG sensitivity is close to logarithmic

Comparing PUBG config LastConvertedSensitivity values suggests:

```text
LastConvertedSensitivity ≈ 0.002 × 10^(Sensitivity / 50)
```

This means the ratio between two sensitivity values is:

```text
Sensitivity ratio = 10^(Sensitivity difference / 50)
```

Examples:

```text
+1 sensitivity  ≈ 1.047x
+3 sensitivity  ≈ 1.149x
+15 sensitivity ≈ 1.995x
```

---

## 11-2. Are LastConvertedSensitivity and PUBG yaw the same?

Probably not.

The commonly seen `PUBG yaw = 0.002` appears to be a base coefficient from PUBG config or engine input structure, but it should not be treated directly as a deg/count value for cm/360 calculation.

This calculator keeps the non-linear PUBG config curve, but reverse-calculates the yaw value from a Sensitivity 50, 16:9, FPP FOV90 cm/360 reference.

```text
PUBG yaw ≈ 0.05 deg/count at Sensitivity 50
```

Therefore, the 360° Distance calculation uses:

```text
PUBG yaw ≈ 0.005 × 10^(Sensitivity / 50)
```

Summary:

```text
0.002
→ config conversion coefficient

0.005
→ yaw coefficient for cm/360 reverse calculation

0.05
→ PUBG yaw deg/count at Sensitivity 50
```

---

## 11-3. PUBG-style eDPI formula

```text
PUBG-style eDPI = DPI × 10^((Sensitivity - 11) / 50)
```

The `-11` is a normalization value for display scale.

This is not an absolute physical unit. It is a comparison value for PUBG sensitivity ranges.

---

## 11-4. 360° Distance formula

Base cm/360 is calculated as:

```text
cm/360 = 360 × 2.54 / (DPI × PUBG yaw)
```

Then TPP/FPP/ADS state, FOV, and aspect ratio corrections are applied.

---

## 11-5. FOV correction

FPP FOV correction uses:

```text
FPP correction = (tan(45°) / tan(FOV / 2)) ^ 0.8
```

The 0.8 power matched manual measurements around FOV 80–100 better than a pure tangent correction.

---

## 11-6. Aspect correction

360° Distance uses:

```text
16:9  = 1.00
16:10 = 1.00
21:9  = 0.85
4:3   = 1.16
```

These values are for horizontal 360° distance correction and serve a different purpose from the Vertical Sensitivity corrections in the Resolution / Aspect Ratio Converter.

---

## 11-7. Background of Scope Sensitivity recommendations

2x/3x recommended sensitivities are not official PUBG formulas.

They are practical estimates based on actual full-auto AR 2x/3x sensitivity settings used by current PUBG professional players.

Analysis process:

```text
1. Collect pro players' DPI, Scope Mode Sensitivity, Vertical Sensitivity, and 2x/3x settings
2. Organize them by PUBG-style eDPI including Vertical Sensitivity
3. Compare how much higher 2x/3x sensitivity is set than Scope Mode Sensitivity in each eDPI range
4. Estimate recommended 2x/3x sensitivity from that tendency
```

Therefore, these values are starting points based on real pro-player tendencies, not official values.

---

## 11-8. Why Vertical Sensitivity feels different at high and low eDPI

High eDPI users already have fast horizontal sensitivity. If Vertical Sensitivity is too low, they need more downward hand movement to control recoil. This can make horizontal micro-corrections unstable.

A somewhat higher Vertical Sensitivity can reduce the downward movement needed for recoil control and may create more room for horizontal micro-correction.

Low eDPI users have slower horizontal sensitivity. If Vertical Sensitivity is too high, downward input can interfere strongly with horizontal movement and feel restrictive or stiff.

At low eDPI, avoiding excessively high Vertical Sensitivity can make horizontal movement feel freer and allow more natural recoil control through hand movement.

This is not an absolute rule, but a common tendency by sensitivity range.

---

# End of Manual EN v1.0
