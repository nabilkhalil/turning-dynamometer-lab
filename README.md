# Turning Force Dynamometer Lab

**An interactive virtual lab for learning how cutting forces are measured in turning.**

You set up a virtual lathe, clamp the tool on a force sensor (a *dynamometer*), cut metal, and watch the forces appear live on screen. Then you change the cutting conditions and see how the forces respond.

## ▶ [Click here to open the lab](https://nabilkhalil.github.io/turning-dynamometer-lab/)

The lab opens straight in your browser. Nothing to download, install or sign up for. Use Chrome, Edge or Firefox on a laptop or desktop.

Link to share: `https://nabilkhalil.github.io/turning-dynamometer-lab/`

> **Note:** Every force value in this lab comes from a computer model. It behaves like a real instrument, but it is **not real measured data**. Don't cite these numbers as experimental results.

**Jump to:** [Quick start](#quick-start-5-minutes) · [The four modes](#the-four-modes) · [The screen](#a-tour-of-the-screen) · [Settings](#settings-you-can-change) · [Experiments](#experiments-to-try) · [Key terms](#key-terms) · [Help](#tips-and-troubleshooting) · [Instructors](#for-instructors)

---

## What you will learn

By the end of a session you should be able to:

- Explain how a force sensor turns a force into an electrical signal you can record.
- Set up a force measurement in the right order: mount, clamp, connect, set up, zero, cut.
- Name the three forces on a turning tool, **Fc**, **Ff** and **Fp**, and say which is largest.
- Predict how feed, depth of cut, tool angle, tool wear and material change the forces.
- Choose sensible measurement settings and spot what goes wrong when you don't.

[↑ Back to top](#turning-force-dynamometer-lab)

---

## Quick start (5 minutes)

1. **[Click here to open the lab](https://nabilkhalil.github.io/turning-dynamometer-lab/).** A 3D lathe appears, with force plots on the right.
2. **Stay in Guided learning.** It is already selected at the top of the page.
3. **Click step 1** in the list on the left. Watch the animation and read the note under the list.
4. **Click the next step each time.** Only the current step can be clicked, so you can't get lost. There are **13 steps**.
5. **At step 9 the cut starts.** Watch the plots: three almost flat lines. The highest one is **Fc**, the main cutting force.
6. **Click any part of the 3D model** (sensor, cable, amplifier, tool…) to read what it does.

That's it. Once you've done the guided run, try the other modes.

[↑ Back to top](#turning-force-dynamometer-lab)

---

## The four modes

Pick a mode with the buttons at the top of the page.

| Mode | Use it to… |
| --- | --- |
| **Guided learning** | Walk through the full measurement step by step. **Start here.** |
| **Free exploration** | Skip the setup: the lathe is ready to cut. Change any setting, even while cutting, and see what happens. |
| **Virtual experiment** | Run a series of cuts, save each one as a *trial*, compare them on a chart, and export the results. |
| **Assessment** | Answer 15 quiz questions and do 4 hands-on tasks, then click **Generate report** to get a file for your instructor. |

[↑ Back to top](#turning-force-dynamometer-lab)

---

## A tour of the screen

### 3D bench (top left)

- **Drag** to rotate, **scroll** to zoom. The camera buttons (**Iso, Front, Top, Tool, Dyno, Chain**) jump to useful viewpoints.
- The view buttons let you look inside the sensor: **External, Transparent, Section, Exploded, Sensor,** and **Force path** (shows how force travels from the tool into the sensor).
- **Deflection ×** makes the sensor's bending visible. The real bending is tiny: a few micrometres.
- **Force vectors** draws arrows for the forces on the tool.

### Control buttons

- **Start turning**: start or stop the cut.
- **New pass**: cut again from the start.
- **Reset / zero amplifier**: clear leftover charge. **Always click this before a measurement.**

### Force plots (right)

- One plot each for **Fc, Ff, Fp**, plus the total force **F**. In turning the force stays almost constant while the tool cuts.
- Tick **Overlay true model force** to see the "perfect" force as a dashed line. The gap between the two lines is the error added by the measuring equipment.

### Tabs at the bottom

| Tab | What's there |
| --- | --- |
| Cutting & chain parameters | All the settings: material, tool, speeds, feeds, and the measuring equipment. |
| Analysis | Average and peak forces, cutting power, the frequency spectrum, and an automatic explanation of your signal. |
| Experiment log | Save trials, compare them, run a parameter sweep, export CSV files. |
| Assessment | Questions, tasks and the report generator. |
| Constants & sources | Every number the model uses, and where it comes from. |
| Theory | Short explanations of the physics and equations. |

[↑ Back to top](#turning-force-dynamometer-lab)

---

## Settings you can change

All of these are in the **Cutting & chain parameters** tab.

### Cutting parameters

| Setting | Symbol | What it means | Range |
| --- | --- | --- | --- |
| Workpiece material | — | Aluminium 6061, mild steel, or stainless steel 316L | — |
| Workpiece diameter | D | How thick the bar is | 20–80 mm |
| Cutting speed | Vc | How fast the bar surface moves past the tool | 20–500 m/min |
| Feed | f | How far the tool moves along the bar each turn. Sets the chip thickness. | 0.05–0.5 mm/rev |
| Depth of cut | ap | How deep the tool cuts into the bar | 0.25–5 mm |
| Approach angle | κr | Angle of the cutting edge to the bar | 45–95° |
| Nose radius | rε | How rounded the tool tip is | 0.2–1.2 mm |
| Rake angle | γ | Tilt of the tool's top face. A bigger angle means less force. | −6 to 20° |
| Flank wear | VB | How worn the tool is | 0–0.4 mm |

### Measurement equipment

| Setting | What it does |
| --- | --- |
| Amplifier range | The largest force it can show. Too small and the signal clips (flat top); too large and small forces get lost in noise. |
| Amplifier time constant τ | How long the amplifier holds a steady signal. **Use Long (DC) for turning.** A short τ makes the force fade away. |
| Sampling rate fs | How many readings per second are recorded. |
| Low-pass filter fc | Removes fast wiggles above this frequency. |
| Mounted natural frequency fn | How stiff the sensor setup is. A long tool overhang lowers it. |
| Playback speed | Slows the animation so you can follow it. Doesn't change the forces. |

You can also switch real-world problems on and off: **wobbly bar (runout), interrupted cut** (a slot in the bar), **vibration, crosstalk** between channels, **noise, charge drift,** and **skipping the amplifier reset**.

[↑ Back to top](#turning-force-dynamometer-lab)

---

## Experiments to try

Each one takes a few minutes. **Write down what you expect before you run it.**

1. **Double the feed.** Change f from 0.1 to 0.2 mm/rev. Does the force double? (Hint: it rises, but by less than double. Why?)
2. **Turn the edge.** Change κr from 45° to 90°. What happens to Ff and Fp? Does Fc change much?
3. **Wear out the tool.** Increase VB from 0 to 0.3 mm. Which force grows the most?
4. **Speed it up.** Increase Vc. The bar spins faster, but does the force change in this model? (See *Model limitations* below.)
5. **Forget to zero.** Tick *Skip amplifier reset* and cut. What happens to the average force?
6. **Use a short time constant.** Set τ to 0.2 s and run a long cut. Why does the force fade even though the cut hasn't changed?
7. **Change material.** Cut aluminium, then stainless steel, with the same settings. How much higher are the forces?

Tip: the **Parameter sweep** in the *Experiment log* tab shows the trend instantly. Then check it with a real (simulated) cut.

[↑ Back to top](#turning-force-dynamometer-lab)

---

## Key terms

| Term | Plain-language meaning |
| --- | --- |
| **Dynamometer** | A force sensor. Here it sits under the tool and measures the force in three directions at once. |
| **Piezoelectric** | Some crystals, such as quartz, make an electric charge when squeezed. More force gives more charge. |
| **Charge amplifier** | Turns the tiny charge from the crystals into a voltage a computer can record. |
| **Fc** (cutting force) | The biggest force. Pushes down on the tool as the bar spins. |
| **Ff** (feed force) | Pushes back along the bar, against the direction the tool moves. |
| **Fp** (passive force) | Pushes the tool away from the bar. |
| **F** | Total force: √(Fc² + Ff² + Fp²). |
| **Spindle speed N** | How many turns per minute the bar makes: N = 1000 · Vc / (π · D). |
| **Specific cutting force kc** | Force needed per mm² of chip: kc = Fc / (ap · f). It falls as the chip gets thicker. |
| **Time constant τ** | How quickly the amplifier lets a steady signal leak away. Turning forces are steady, so τ must be long. |
| **Natural frequency** | The frequency at which the setup "rings" if struck. An interrupted cut can make it ring. |
| **Drift** | Slow wandering of the signal caused by charge leaking away. |

[↑ Back to top](#turning-force-dynamometer-lab)

---

## Tips and troubleshooting

| Problem | What to do |
| --- | --- |
| **The lab page doesn't load** | Check your internet connection, then refresh (F5). |
| **3D view is blank** | Check your internet connection and refresh (F5). The plots and settings still work without it. Try Chrome, Edge or Firefox. |
| **Force doesn't start at zero** | Click **Reset / zero amplifier** just before the cut. |
| **Signal is flat at the top** | It is clipping. Choose a larger *Amplifier range*. |
| **Force fades during the cut** | Set *Amplifier time constant τ* to **Long (DC)**. |
| **My saved trials disappeared** | Trials are saved in this browser only. Clearing browser data or changing computer erases them. Click **Export trials CSV** to keep a copy. |
| **How do I open the CSV?** | In Excel, MATLAB or Python. The first lines of the file record the settings you used. |
| **Screen feels cramped** | Use a laptop or desktop. A mouse makes the 3D view easier to use. |

[↑ Back to top](#turning-force-dynamometer-lab)

---

## For instructors

### Hosting on GitHub Pages

1. In this repository go to *Settings → Pages*.
2. Under *Build and deployment*, choose *Deploy from a branch*, then `main` and `/ (root)`. Save.
3. After about a minute the lab is live at `https://<user>.github.io/turning-dynamometer-lab/`.

This repository is already published at <https://nabilkhalil.github.io/turning-dynamometer-lab/>. Every push to `main` updates the live lab automatically.

**Adding it to Moodle / URLearn:** add a *URL* resource pointing to that address, or embed it with an iframe in a *Page* resource (height ≈ 1600 px).

**Running locally:** double-click `index.html`, or serve the folder with `python -m http.server`.

**Fully offline labs:** download `three.min.js` and `OrbitControls.js` (Three.js version 0.128.0), place them next to `index.html`, and change the two `<script src>` lines to the local file names.

### Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole application (HTML, CSS and JavaScript). No build step, no server code. |
| `README.md` | This guide. |

---

## Under the hood (technical reference)

This section is for anyone who wants to check the model or extend the code. Click a heading to open it.

<details>
<summary><b>The instrument</b></summary>

The dynamometer is modelled on a **Kistler 9257B-type** three-component piezoelectric dynamometer on the cross slide of a lathe, with the tool holder clamped on its cover plate.

Channels: **x = Ff** (feed, along the spindle axis), **y = Fp** (passive, radial), **z = Fc** (cutting, vertical).

</details>

<details>
<summary><b>Equations</b></summary>

#### Kinematics

```text
N    = 1000 · Vc / (π · D)        rpm
Vf   = f · N                      mm/min
Q    = Vc · ap · f                cm³/min (material removal rate)
Pc   = Fc · Vc / 60 000           kW
Ra   ≈ f² / (32 · rε)             theoretical roughness
```

#### Kienzle force model (Kienzle, 1952)

```text
κ   = κr · 2ap / (2ap + rε)                   effective approach angle with nose radius
h   = f · sin κ,   b = ap / sin κ
kc  = kc1.1 · h^(−mc) · (1 − (γ − 6°)/100)
Fc  = kc · b · h
FT  = rT · Fc,   Ff = FT · sin κ,   Fp = FT · cos κ
wear:         Fc · (1 + 0.6·VB),   FT · (1 + 2.0·VB)
runout:       ap(θ) = ap + e · cos θ
interrupted:  ap = 0 over the keyway angle
F_dynamometer = force on the tool,   F = √(Fc² + Ff² + Fp²)
```

The force is quasi-static. It varies with time only through runout (once per revolution, N/60) or an interrupted cut (one impact per revolution), so the model shows entry transients and impact ringing but no tooth-passing pulses.

#### Measurement chain

```text
Structure   G(s) = ωn² / (s² + 2ζωn s + ωn²)   per axis (bilinear biquad)
Crosstalk   F' = C · F
Charge      Q  = S · F' + Q_offset + Q_drift + noise
Amplifier   high-pass with time constant τ (none in Long/DC mode)
            V  = Q / (S · range),  clipped at ±10 V   (ideal: V = −Q/Cf)
Filter/ADC  2nd-order Butterworth at fc, sampled at fs, 16-bit
Displayed   F  = V · range
```

Per-sensor loads (educational): the tool overhangs the cover plate, so the sensor pair nearest the workpiece carries most of Fc and the far pair can go into tension. Their sum still equals Fc.

</details>

<details>
<summary><b>Where the numbers come from</b></summary>

The lab labels every constant with one of three categories, also shown in the *Constants & sources* tab:

- **A: Verified manufacturer specifications** (Kistler 9257B product page). Cover plate 170 × 100 mm; range Fx, Fy ±5 kN, Fz −5…+10 kN; sensitivity −7.5, −7.5, −3.7 pC/N (nominal); natural frequency ≈ 3.5 kHz (sensor, free); stiffness Cx, Cy 1 kN/µm; Fischer 9-pin flange connector; preloaded sensors.
- **B: Engineering equations and published data.** The kinematics and cutting power equations above; the Kienzle law (Kienzle, 1952); theoretical Ra; quartz d11 ≈ 2.3 pC/N; charge-amplifier relations; sampling theorem.
- **C: Educational assumptions.** Material constants kc1.1 / mc / rT (aluminium 700 / 0.25 / 0.35, mild steel 1500 / 0.25 / 0.45, 316L 2000 / 0.21 / 0.50 N/mm²); rake correction; effective κ with nose radius; wear factors; process noise; tool overhang 40 mm and dynamometer geometry; Cz = 2 kN/µm; ζ = 0.04; adjustable mounted fn; crosstalk matrix; residual offset, drift (exaggerated) and noise; τ options; ADC; workpiece size; carriage travel compressed ×10 visually (feed and forces unchanged).

The lab never invents Kistler calibration coefficients. A real instrument is always used with its own calibration sheet.

</details>

<details>
<summary><b>Model limitations</b></summary>

The model does **not** include any change of force with cutting speed, built-up edge, chip segmentation, thermal effects, workpiece deflection, or chatter. Kistler also makes dedicated turning dynamometers; they are not modelled. Use the lab to build intuition and plan experiments. Only publish forces measured with a calibrated instrument.

</details>

<details>
<summary><b>Code structure</b></summary>

Everything is in `index.html`, split into independent modules:

| Module | Responsibility | Depends on |
| --- | --- | --- |
| 1 `Model` | Specifications, material constants, kinematics, Kienzle turning force model. Pure JS. | — |
| 2 `Chain` | Measurement chain: 2nd-order structure, crosstalk, quartz charge, offset/drift/noise, charge amplifier with time constant τ, saturation, low-pass filter. | Model |
| 3 `Sim` | Simulation clock at 100 kHz internal rate; spindle rotation and feed; runout and interrupted cut; sampling at fs with 16-bit ADC; ring buffer. | Model, Chain |
| 4 Plotting | Canvas plots (force–time, spectrum, trials, sweep). No chart library. | — |
| 5 `Scene3D` | Three.js lathe: bed, chuck, workpiece, carriage, dynamometer with four sensors, tool holder, cable, charge amplifier, DAQ; anatomy views, deflection, vectors, force path, picking. | Sim (read-only) |
| 6 Content | Component notes, constants table with categories, sources. | — |
| 7 UI | Guided procedure (13 steps), free mode, parameter controls, dashboard, export. | all |
| 8 Experiment log | `localStorage` trials, CSV export, parameter sweep. | Model |
| 9 Assessment | 15 concept questions, 4 simulator-based tasks, scoring, report. | Sim, Model |

To split the code into separate files, move each module into `js/<module>.js` in the order above and load them as plain scripts. The modules talk to each other only through the objects named in the table.

External dependencies: Three.js r128 (from jsDelivr) and Google Fonts (optional, with fallbacks).

</details>

---

## Sources

- Kistler, *Multicomponent dynamometer, 5 kN, cover plate 100x170 mm / 9257B*, item 18007542. <https://www.kistler.com/CH/en/p/multicomponent-dynamometers-9257b/000000000018007542>
- O. Kienzle, *Die Bestimmung von Kräften und Leistungen an spanenden Werkzeugen und Werkzeugmaschinen*, VDI-Z 94 (1952) 299–305.
- S. Kalpakjian, S. R. Schmid, *Manufacturing Engineering and Technology*.
- IEEE Std 176-1987, *IEEE Standard on Piezoelectricity*.
