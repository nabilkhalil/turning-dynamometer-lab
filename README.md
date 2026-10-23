# Turning Force Dynamometer Lab

Browser-based educational simulator of three-component cutting-force measurement in longitudinal turning. The tool holder is clamped on a Kistler 9257B-type piezoelectric plate dynamometer mounted on the lathe cross slide. Companion to the milling simulator (Cutting Force Dynamometer Lab).

All force data produced by the simulator are **simulated**, not experimental measurements.

## Deploy on GitHub Pages

1. Put `index.html` (and this README) in a repository, e.g. in a folder `turning/` next to the milling `index.html`.
2. *Settings → Pages → Deploy from a branch → main / root*.
3. The page is served at `https://<user>.github.io/<repo>/turning/`.

No build step, no backend. Three.js r128 loads from jsDelivr.

## What is different from the milling simulator

| Aspect | Milling | Turning |
|---|---|---|
| What sits on the dynamometer | Workpiece | Tool holder (force on the tool) |
| Force character | Periodic pulses at f_TP = N·z/60 | Quasi-static; dynamics only from runout (N/60) or interrupted cuts |
| Force model | Altintas mechanistic model, helical discs | Kienzle: kc = kc1.1·h^−mc, Fc = kc·b·h; thrust split by κr |
| Channels | Fx, Fy, Fz | x = Ff (feed), y = Fp (passive), z = Fc (cutting) |
| Key chain lesson | Bandwidth, aliasing, resonance | Charge-amplifier time constant (DC mode), drift, impact ringing |
| Sensor loads | Moments from contact position | Overhang moment: near pair compressed, far pair unloaded |

## Equations

```
N  = 1000·Vc/(π·D)      Vf = f·N      Q = Vc·ap·f      Pc = Fc·Vc/60000
h  = f·sin κ            b = ap/sin κ  κ = κr·2ap/(2ap + rε)   (C)
kc = kc1.1·h^(−mc)·(1 − (γ − 6°)/100)          Fc = kc·b·h
FT = rT·Fc              Ff = FT·sin κ    Fp = FT·cos κ               (C)
wear: Fc·(1 + 0.6·VB), FT·(1 + 2.0·VB)                               (C)
runout: ap(θ) = ap + e·cos θ;  interrupted cut: ap = 0 over the keyway angle
Ra ≈ f²/(32·rε)
```

Measurement chain: 2nd-order structure (fn, ζ) → crosstalk → Q = S·F + offset → high-pass with τ (unless DC) → drift + noise → V = Q/(S·range), ±10 V → Butterworth low-pass fc → sampling fs, 16-bit.

## Information categories

- **A, verified (Kistler 9257B product page):** 170 × 100 mm cover plate; Fx, Fy ±5 kN, Fz −5…+10 kN; −7.5/−7.5/−3.7 pC/N nominal; fn ≈ 3.5 kHz (free); Cx, Cy 1 kN/µm; Fischer 9-pin connector; preloaded.
- **B, established:** kinematics, cutting power, Kienzle law (Kienzle 1952), theoretical Ra, quartz d11 ≈ 2.3 pC/N, charge-amplifier relations, sampling theorem.
- **C, assumptions:** all material constants (kc1.1, mc, rT), rake correction, κeff with nose radius, wear factors, process noise, overhang and geometry, Cz, ζ, crosstalk, offset, drift, noise, τ options, workpiece size, ×10 visual feed compression.

Kistler also offers dedicated turning dynamometers; they are not modelled.

## Suggested lab exercise

Steel, ap = 1.5 mm, κr = 75°: record trials at f = 0.1 … 0.4 mm/rev. Plot log kc against log h, fit the line, and compare the slope (−mc) and intercept (kc1.1) with the model constants.

## Sources

- Kistler, *Multicomponent dynamometer, 5 kN, cover plate 100x170 mm / 9257B*. https://www.kistler.com/CH/en/p/multicomponent-dynamometers-9257b/000000000018007542
- O. Kienzle, VDI-Z 94 (1952) 299–305.
- S. Kalpakjian, S. R. Schmid, *Manufacturing Engineering and Technology*.
- IEEE Std 176-1987, *IEEE Standard on Piezoelectricity*.
