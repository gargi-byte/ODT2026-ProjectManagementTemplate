# Open Design and Technology  
## Final Project README

> **Project Weight:** 70%  
> **Team Size:** 2 students  
> **Project Duration:** 4 weeks  
> **Class Time Available:** 6 hours per class  
> **Total Time Available:** 48 effort-hours per team  
> **Project Type:** Playful, interactive, technology-based experience

---

# Before you begin

## Fork and rename this repository
After forking this repository, rename it using the format:

`ODT-2026-ProjectWraith`

### Example
`ODT-2026-PixelWizards`

Do not keep the default repository name.

---

# How to use this README

This file is your team’s **working project document**.

You must keep updating it throughout the 4-week build period.  
By the final review, this README should clearly show:
- your idea,
- your planning,
- your design decisions,
- your technical process,
- your build progress,
- your testing,
- your failures and changes,
- your final outcome.

## Rules
- Fill every section.
- Do not delete headings.
- If something does not apply, write `Not applicable` and explain why.
- Add images, screenshots, sketches, links, and videos wherever useful.
- Update task status and weekly logs regularly.
- Use this file as evidence of process, not only as a final report.

---

# 1. Team Identity

## 1.1 Studio / Group Name
`[NishGar]`

## 1.2 Team Members

| Name | Primary Role | Secondary Role | Strengths Brought to the Project |
|---|---|---|---|
| `[Gargi Waghmare]` | `[Electronics / Coding / Mechanics]` | `[App]` | `[technical proficiency and problem solving]` |
| `[Nishtha Vats]` | `[App / Fabrication / Mechanics]` | `[Electronics]` | `[strategic thinking and creativity]` |

## 1.3 Project Title
`[Project Wraith]`

## 1.4 One-Line Pitch
`[A phone-controlled ghost slides down an inclined rope to jumpscare unsuspecting passersby, triggered in secret by an operator using a custom web app hosted directly on the ESP32.]`

## 1.5 Expanded Project Idea
In 1–2 paragraphs, explain:
- what your project is,
- what kind of playful experience it creates,
- what makes it fun, curious, engaging, strange, satisfying, competitive, or delightful,
- what technologies are involved.

**Response:**  
`[Project Wraith is a kinetic jumpscare installation where a ghost prop — complete with a servo-actuated head and ultrasonic proximity detection — is launched down an inclined zip-line rope at the press of a button on a phone. The ghost hangs from a platform that rides the main rope via a carabiner/ring. A DC gearbox motor mounted on the platform winds a pull-string through a hook pulley at the high anchor point, dragging the platform and ghost up the rope. When the motor releases, gravity sends the ghost flying down toward unsuspecting targets. A 15-second pause at the far end lets the ultrasonic sensor scan for nearby people: if anyone comes within 100cm, a servo motor actuates 90 degrees — making the ghost's head snap toward them — before returning to rest. The operator triggers everything from a phone browser connected to the ESP32's own WiFi hotspot, requiring no internet, no Bluetooth pairing, and no app installation.

The experience is pure theatrical chaos built on asymmetric information. One person has complete hidden control while the target has absolutely no warning. The ghost moves fast and silently, appears from above, and the servo head snap at close range adds a second layer of shock even after the initial scare. Technologies involved include an ESP32 microcontroller running MicroPython, a DC gearbox motor, an L298N motor driver, a hook pulley for rope redirection, a servo motor for the ghost head actuation, an HC-SR04 ultrasonic sensor for proximity detection, a buck converter for stable power regulation, two 18650 lithium cells in series providing 7.4V, and a fully custom web interface served directly from the ESP32 in Access Point mode.
]`

---

# 2. Philosophy Fit

## 2.1 Experience, Not Social Problem
This module does **not** require your project to solve a large social problem.

You are allowed to build:
- toys,
- games,
- interactive objects,
- playful machines,
- kinetic artifacts,
- humorous devices,
- strange but delightful experiences,
- things that are entertaining to use or watch.

## 2.2 What kind of experience are you creating?
Answer the following:
- What is the experience?
- What do you want the player or participant to feel?
- Why would someone want to try it again?

**Response:**  
`[The experience is a sudden, unexpected jumpscare delivered by a physical object moving through real space — not a screen, not a speaker, but something actually flying at you from above. The target feels a sharp spike of shock and fear, immediately followed by laughter and disbelief once they realise what happened. The servo head snap at close range adds a second beat of horror even for those who catch the ghost mid-slide. The combination of surprise, relief, and the absurdity of being scared by a fabric ghost on a rope makes it deeply shareable — people immediately want to watch it happen to someone else, or take over as operator themselves. The replay loop is driven by the operator's desire to find the perfect victim and the target's desire for revenge by becoming the operator.]`

## 2.3 Design Persona
Complete the sentence below:

> We are designing this project as if we are a small creative studio making a **[toy / game / playable object / interactive experience]** for **[children / teens / adults / classmates / exhibition visitors / mixed audience]**.

**Response:**  
`[We are designing this project as if we are a small creative studio making an **interactive experience** for a **mixed audience of teens, adults, and exhibition visitors**.]`

---

# 3. Inspiration

## 3.1 References
List what inspired the project.

| Source Type | Title / Link | What Inspired You |
|---|---|---|
| `[Video]` | `[https://youtu.be/tB8D2QZ9lA4?si=OahrS8xceYasXdbh]` | `[The core mechanic — a ghost on an inclined rope — came directly from DIY Halloween yard decoration videos. We borrowed the zip-line concept and made it electronically controlled.]` |
| `[App / Object]` | `[Car controller apps]` | `[The idea of controlling a physical moving object from a single phone button — simple, low-latency, satisfying to use — directly shaped the one-button launch interface.]` |
| `[Interactive Experience]` | `[Haunted house walk-through attractions]` | `[The operator-victim dynamic, the element of hidden control, and the idea that fear is most effective when it comes from an unexpected physical object in real space.]` |

## 3.2 Original Twist
What makes your project original?

**Response:**  
`[Most zip-line ghost decorations are passive — they rely on wind or a manual push and have no electronic control. Project Wraith is original because the operator has complete hidden wireless control over exactly when the ghost launches, turning a decoration into a two-player asymmetric experience. The ultrasonic sensor and servo head snap add a second autonomous scare layer that triggers independently of the operator. The ESP32 acting as its own WiFi access point means there are zero connection dependencies — no router, no pairing, no app install — just connect to a WiFi hotspot and open a browser. The ghost platform is entirely self-contained with its own battery, motor, and controller riding along the rope, eliminating all wiring constraints.]`

---

# 4. Project Intent

## 4.1 Core Interaction Loop
Describe the main loop of interaction.

Examples:
- press → launch → score → reset
- connect → control → observe → repeat
- turn → trigger → react → repeat
- move object → sensor detects → sound/light response → player reacts

**Response:**  
`[wait (hide) → spot target → tap launch → ghost travels forward → pauses → servo snaps if person detected → ghost returns → ready → repeat]`

## 4.2 Intended Player / Audience

| Question | Response |
|---|---|
| Who is this for? | `[Two roles : one operator (the person with the phone) and unlimited unsuspecting targets (passersby or participants)]` |
| Age range | `[8 and above — anyone who can handle a mild jumpscare]` |
| Solo or multiplayer | `[Two-player asymmetric : one operator, one or more targets]` |
| Expected duration of one round | `[Approximately 34 seconds from launch to full reset (8s forward + 15s pause + 8.5s reverse)]` |
| What should the player feel? | `[Operator feels power, anticipation, and delight. Target feels shock, fear, then laughter.]` |
| Is explanation required before use? | `[No : targets don't know anything (that's the point). Operator needs a 30-second briefing on connecting to GhostESP WiFi and opening 192.168.4.1.]` |

## 4.3 Player Journey
Describe exactly how a player will use the project.

1. **Approach:** `[A person walks down a corridor, street, or open space. The ghost is parked silently at the top of the rope, above eye line and easy to miss. The operator is hidden nearby with their phone.]`
2. **Start:** `[The operator opens Safari or Chrome, connects to the GhostESP WiFi hotspot (password: 12345678), and navigates to 192.168.4.1 to load the Project Wraith control panel.]`
3. **First Action:** `[The operator spots a suitable target entering the scare zone — roughly 1 to 2 metres from the rope's path — and taps the LAUNCH button on the web interface.]`
4. **Main Interaction:** `[The motor fires. The ghost travels 9 metres along the inclined rope in approximately 8 seconds. At the far end, it pauses for 15 seconds while the ultrasonic sensor scans the area every 80ms.]`
5. **System Response:** `[If a person comes within 100cm of the ghost during the pause, the servo snaps the ghost's head 90 degrees toward them and returns to neutral. The ghost then automatically reverses back to the start over 8.5 seconds. The web interface shows a countdown timer throughout]`
6. **Win / Lose / End Condition:** `[There is no formal win condition — success is measured entirely by the quality of the target's reaction. The more dramatic the scream or jump, the better.]`
7. **Reset:** `[The ghost returns automatically. The Launch button re-enables on the phone. The operator selects the next target and waits for the right moment.
]`

## 4.4 Rules of Play
If your project is a game, list the rules clearly.

- `[The operator must stay hidden and out of sight of the target at all times.]`
- `[The ghost must only be launched when a target is within the scare zone (roughly 1–2 metres from the rope's path).]`
- `[The operator cannot launch twice in a row at the same person — new target each round.]`
- `[Targets who become operators must find and scare someone who hasn't been hit yet.]`
- `[The ghost cannot be launched while a sequence is already running — the button disables itself automatically.]`

---

# 5. Definition of Success

## 5.1 Definition of “Playable”
Your project will be considered complete only if these conditions are met.

- [x] `The ghost platform slides down the inclined rope reliably and reaches the far end every single time without getting stuck.`
- [x] `The phone web interface connects to the ESP32 via GhostESP WiFi within 10 seconds and the Launch button triggers the motor with no noticeable delay.`
- [x] `The motor auto-stops after the calibrated forward and reverse durations — no manual intervention needed.`
- [x] `The ultrasonic sensor reliably detects a person within 100cm during the pause window and triggers the servo sweep.`
- [x] `The ghost resets to the start position automatically after each launch and is ready for the next round within 35 seconds.`

## 5.2 Minimum Viable Version
What is the smallest version of this project that still delivers the core experience?

**Response:**  
`[A ghost prop on an inclined rope that travels forward and returns automatically when triggered by a single button tap on a phone browser, with no LED, servo, or sensor functionality. If the ghost flies on command and returns reliably, the core jumpscare experience is delivered.]`

## 5.3 Stretch Features
What features are nice to have but not essential?

- `A recorded scream audio clip played through an amplified speaker (ISD1820 module) instead of a silent servo-only reaction.`
- `A PIR motion sensor that sends a vibration alert to the operator's phone when someone enters the scare zone, so the operator does not have to watch constantly.`
- `A reaction-rating system where the operator scores each scare 1 to 5, logged and displayed on a leaderboard on the web interface.`

---

# 6. System Overview

## 6.1 Project Type
Check all that apply.

- [x] Electronics-based
- [x] Mechanical
- [x] Sensor-based
- [x] App-connected
- [x] Motorized
- [ ] Sound-based
- [ ] Light-based
- [x] Screen/UI-based
- [x] Fabricated structure
- [ ] Game logic based
- [x] Installation / tabletop experience
- [ ] Other: `[Write here]`

## 6.2 High-Level System Description
Explain how the system works in simple terms.

Include:
- input,
- processing,
- output,
- physical structure,
- app interaction if any.

**Response:**  
`The operator connects their phone to the ESP32's WiFi hotspot (GhostESP, no internet required) and opens the control panel at 192.168.4.1 in a browser. Tapping Launch sends an HTTP request to the ESP32. The ESP32 runs the ghost sequence: it drives IN1 and IN2 on the L298N motor driver to spin the DC gearbox motor forward, winding the pull-string through the hook pulley and dragging the ghost platform up the inclined rope for a calibrated duration. The motor stops and a 15-second pause begins. During the pause the HC-SR04 ultrasonic sensor polls for nearby objects every 80ms. If anything comes within 100cm, the ESP32 drives the servo motor on GPIO 19 to sweep 90 degrees and return. After the pause the motor reverses and the ghost travels back to its start position. The ESP32 then waits for the next launch command. The entire platform — ESP32, motor driver, motor, sensor, and servo — rides on the sliding platform powered by two 18650 cells in series (7.4V) with a buck converter providing stable 5V to the ESP32 and sensor.`

## 6.3 Input / Output Map

| System Part | Type | What It Does |
|---|---|---|
| `Phone browser — Launch button` | Input | `Sends HTTP GET /launch to ESP32 web server triggering the full ghost sequence` |
| `HC-SR04 ultrasonic sensor` | Input | `Polls distance every 80ms during the 15-second pause; triggers servo if object within 100cm` |
| `ESP32 (MicroPython, AP mode)` | Processing | `Hosts WiFi hotspot and web server, runs ghost sequence logic, controls all outputs` |
| `L298N motor driver (IN1 GPIO26, IN2 GPIO27)` | Processing | `H-bridge that translates ESP32 digital signals into motor forward/reverse/stop` |
| `DC gearbox motor` | Output / Physical Action | `Winds pull-string through pulley, dragging ghost platform forward; releases for gravity return` |
| `Servo motor (GPIO19)` | Output | `Sweeps ghost handd 90 degrees when person detected within 100cm during pause` |
| `Hook pulley (at high anchor)` | Physical Action | `Redirects pull-string from motor (mounted low) up to ghost platform on rope` |
| `Ghost platform on inclined rope` | Physical Action | `Slides 9 metres along rope carrying the entire electronics and ghost prop assembly` |


---

# 7. Sketches and Visual Planning

## 7.1 Concept Sketch
Add an early sketch of the full idea.

**Insert image below:**  
`[
]`

Example:
```md

```

## 7.2 Labeled Build Sketch
Add a sketch with labels showing:
- structure,
- electronics placement,
- user touch points,
- moving parts,
- output elements.

**Insert image below:**  
`[Upload image and link here]`

## 7.3 Approximate Dimensions

| Dimension | Value |
|---|---|
| Rope span (length) | `3 metres` |
| Height difference (high to low anchor) | `approximately 2 to 2.5 metres` |
| Ghost prop (head diameter) | `approximately 20cm` |
| Platform size (motor + electronics) | `approximately 20cm x 15cm x 5cm` |
| Estimated total weight of platform | `approximately 600 to 800 grams` |

---

# 8. Mechanical Planning

## 8.1 Mechanical Features
Check all that apply.

- [ ] Gears
- [x] Pulleys
- [ ] Belt drives
- [ ] Linkages
- [ ] Hinges
- [x] Shafts
- [ ] Springs
- [ ] Bearings
- [x] Wheels (made out of rope ring / carabiner sliding on rope)
- [x] Sliders
- [ ] Levers
- [ ] Not applicable

## 8.2 Mechanical Description
Describe the mechanism and what it is meant to do.

**Response:**  
`The main inclined rope (clear nylon, 4 to 5mm) is strung from a high anchor point (2 to 2.5m elevation) diagonally down to a low ground-level anchor over a 9-metre horizontal span. The ghost platform rides on this rope via two hook points — a carabiner (made out of rope) allowing it to slide freely. A hook pulley is fixed at the high anchor. The DC gearbox motor is mounted on the platform itself with a PVC pipe spool on its shaft. A thin pull-string (2mm nylon) connects the spool, runs up to the hook pulley which redirects it, and back down along the rope to an anchor at the far low end. When the motor winds the string, it reels the platform toward the high anchor. When motor power is cut, gravity pulls the platform back down the incline. The servo is mounted on the platform and connected to the ghost head to actuate a 90-degree snap motion when triggered.`

## 8.3 Motion Planning
If something moves, explain:
- what moves,
- what causes the movement,
- how far it moves,
- how fast it moves,
- what could go wrong.

**Response:**  
`[Write here]`

## 8.4 Simulation / CAD / Animation Before Making
If your project includes mechanical motion, document the digital planning before fabrication.

| Tool Used | File / Link | What Was Tested |
|---|---|---|
| `Physical whiteboard sketch` | `See sketch photos` | `Rope angle, pulley position, string routing from motor spool through pulley to platform` |
| `Hand calculation` | N/A | `Spool circumference vs rope length to estimate rotation count; motor torque vs platform weight` |


## 8.5 Changes After Digital Testing
What changed after the CAD, animation, or simulation stage?

**Response:**  
`The original design had the motor mounted at the high anchor point (fixed, not on platform). This was changed to mount the motor directly on the sliding platform to eliminate all wiring constraints — no slip rings, no trailing wires, no tangling. The pulley's role changed from driving the ghost to purely redirecting the string, which simplified the mechanical design and made it more reliable. The platform became entirely self-contained with its own onboard battery, controller, and actuators.`

---

# 9. Electronics Planning

## 9.1 Electronics Used

| Component | Quantity | Purpose |
|---|---:|---|
| ESP32 DevKit v1 | 1 | Main microcontroller — runs MicroPython, hosts WiFi AP, web server, and all control logic |
| L298N motor driver module | 1 | H-bridge to drive DC motor forward and reverse from ESP32 digital signals |
| DC gearbox motor (12V, high torque, 30–60 RPM) | 1 | Winds pull-string spool to move ghost platform along rope |
| Servo motor (SG90 or similar) | 1 | Actuates ghost head 90 degrees when person detected within 100cm |
| HC-SR04 ultrasonic sensor | 1 | Measures distance to nearby objects during pause; triggers servo if under 100cm |
| Buck converter module (7.4V to 5V) | 1 | Provides stable 5V to ESP32 and ultrasonic sensor from 7.4V battery |
| 18650 lithium cells | 2 | Two cells in series = 7.4V power supply for motor driver and (via buck converter) all logic |
| 18650 battery holder (2-cell series) | 1 | Holds both cells in series configuration |
| Toggle switch | 1 | Main power on/off — cuts circuit during charging |
| Hook pulley block | 1 | Redirects pull-string at high anchor; allows motor to be mounted low on platform |
| PVC pipe section (spool) | 1 | Wound onto motor shaft to reel in pull-string |
| Resistors (1kΩ x3) | 3 | Voltage divider on HC-SR04 ECHO pin — reduces 5V output to 3.3V safe for ESP32 |
| Jumper wires and breadboard | 1 set | Connections between components |

## 9.2 Wiring Plan
Describe the main electrical connections.

**Response:**  
Two 18650 cells in series (7.4V)
  |
  +-- Toggle switch (power cut during charging)
  |
  +-- L298N VM pin (motor power)
  |     |-- IN1 from ESP32 GPIO 26
  |     |-- IN2 from ESP32 GPIO 27
  |     |-- ENA jumpered HIGH (full speed always)
  |     +-- Motor OUT1 / OUT2 to DC motor
  |
  +-- Buck converter IN+ (7.4V)
        |-- Buck OUT+ (5V) to ESP32 VIN
        |-- Buck OUT+ (5V) to HC-SR04 VCC
        +-- Buck OUT- / GND (common ground for all)

HC-SR04:
  TRIG --> ESP32 GPIO 5
  ECHO --> 1kOhm --> junction --> ESP32 GPIO 18
                        |
                      1kOhm
                        |
                      1kOhm
                        |
                       GND

Servo motor:
  Signal --> ESP32 GPIO 19
  VCC    --> 5V (from buck converter)
  GND    --> common GND

## 9.3 Circuit Diagram
Insert a hand-drawn or software-made circuit diagram.

**Insert image below:**  
`[Upload image and link here]`

## 9.4 Power Plan

| Question | Response |
|---|---|
| Power source | `Two 18650 lithium cells in series on the sliding platform` |
| Voltage required | `7.4V nominal (motor driver); 5V (ESP32, sensor, servo via buck converter)` |
| Current concerns | `DC motor draws 1 to 2A under load — buck converter and L298N must handle combined current; ESP32 brownout risk if motor pulls voltage below 7V` |
| Safety concerns | `LiPo cells must be charged individually or with a 2S balance charger — never charge mismatched cells in series; power switch must be off during charging` |


---

# 10. Software Planning

## 10.1 Software Tools

| Tool / Platform | Purpose |
|---|---|
| MicroPython on ESP32 | All hardware control logic — motor, servo, sensor, WiFi, web server |
| Thonny IDE | Writing, uploading, and testing code on ESP32 over USB |
| Built-in phone browser (Safari / Chrome) | Operator control interface — no app install needed |
| Custom HTML/CSS/JS (served by ESP32) | Web-based launch interface with dark theme, status log, and countdown timer |

## 10.2 Software Logic
Describe what the code must do.

Include:
- startup behavior,
- input handling,
- sensor reading,
- decision logic,
- output behavior,
- communication logic,
- reset behavior.

**Response:**  
**Startup:** `ESP32 boots, sets servo to 90-degree neutral then cuts PWM, stops motor, creates GhostESP WiFi hotspot (WPA2, password 12345678), starts non-blocking HTTP server on port 80. Prints all status messages to serial.`

**Input handling:** `Main loop polls for incoming HTTP connections. Accepts GET / to serve the HTML control page. Accepts GET /launch to trigger the ghost sequence. Responds immediately to /launch before running the sequence to prevent browser fetch timeout.`

**Ghost sequence:** `Motor runs forward (GPIO26 HIGH, GPIO27 LOW) for FORWARD_MS milliseconds. Motor stops. Pause loop runs for PAUSE_MS milliseconds — ultrasonic sensor polls every 80ms. If distance under 100cm and servo not yet triggered this round, servo_sweep() runs (0 degrees, hold, 90 degrees, cut PWM). After pause, motor runs reverse (GPIO26 LOW, GPIO27 HIGH) for REVERSE_MS milliseconds. Motor stops. ghost_running flag resets.`

**Sensor reading:** `HC-SR04 triggered with 10-microsecond pulse on GPIO5. Echo duration measured on GPIO18. Distance calculated as (duration / 2) / 29.1 cm. Returns 999 on timeout or error.`

**Servo control:** `PWM on GPIO19 at 50Hz. Duty cycle mapped from angle: min_duty=25 (0 degrees), max_duty=125 (180 degrees). PWM reinitialised fresh before each command and deinitialized after each move to prevent jitter and buzzing at rest.`

**Reset behavior:** `After reverse travel completes, motor stops, ghost_running=False, server resumes accepting new connections. Web page countdown timer re-enables the Launch button.`

**Error handling:** `All sensor reads wrapped in try/except returning 999 on failure. HTTP handler wrapped in try/except with finally block closing connection. AP startup has 5-second timeout guard.`

## 10.3 Code Flowchart
Insert a flowchart showing your code logic.

Suggested sequence:
- start,
- initialize,
- wait for input,
- read input,
- decision,
- trigger output,
- repeat or reset,
- error handling.

**Insert image below:**  
`BOOT
  |
  +-- Servo neutral (90 deg) → PWM off
  +-- Motor stop
  +-- Start WiFi AP (GhostESP)
  +-- Start HTTP server port 80
  |
  v
MAIN LOOP (non-blocking)
  |
  +-- Any HTTP request?
        |
        +-- GET /  --> serve HTML page
        |
        +-- GET /launch --> ghost_running?
              |
              YES --> send BUSY response
              |
              NO  --> send OK response immediately
                       |
                       v
                    GHOST SEQUENCE
                       |
                       +-- Motor FORWARD (GPIO26=1, GPIO27=0)
                       +-- Wait FORWARD_MS (8000ms)
                       +-- Motor STOP
                       |
                       +-- PAUSE LOOP (15000ms)
                             |
                             +-- Poll ultrasonic every 80ms
                             +-- Distance < 100cm AND not triggered?
                                   |
                                   YES --> servo_sweep()
                                            (0 deg → hold → 90 deg → PWM off)
                       |
                       +-- Motor REVERSE (GPIO26=0, GPIO27=1)
                       +-- Wait REVERSE_MS (8500ms)
                       +-- Motor STOP
                       +-- ghost_running = False
                       |
                       v
                    BACK TO MAIN LOOP`

## 10.4 Pseudocode

```text
ON BOOT:
  set servo to 90 degrees, then cut servo PWM
  stop motor
  start WiFi access point "GhostESP" with password "12345678"
  start HTTP server on port 80
  print all status to serial

LOOP FOREVER:
  check for incoming HTTP connection (non-blocking)

  IF connection is GET /:
    send HTML control page

  IF connection is GET /launch:
    IF ghost already running:
      send BUSY response
    ELSE:
      send OK response immediately (before sequence)
      close connection

      SET ghost_running = True

      START motor forward
      WAIT 8000ms
      STOP motor

      SET sensor_triggered = False
      START timer for 15000ms
      WHILE timer not expired:
        measure ultrasonic distance
        IF distance < 100cm AND sensor_triggered is False:
          SET sensor_triggered = True
          move servo to 0 degrees
          wait 800ms
          move servo to 90 degrees
          wait 600ms
          cut servo PWM
        wait 80ms

      START motor reverse
      WAIT 8500ms
      STOP motor

      SET ghost_running = False
```

---

# 11. MIT App Inventor Plan

## 11.1 Is an app part of this project?
- [ ] Yes
- [x] No

If yes, complete this section.

## 11.2 Why is the app not needed?
Explain what the app adds to the experience.

Examples:
- remote control,
- score tracking,
- mode selection,
- personalization,
- triggering effects,
- displaying data.

**Response:**  
`The project uses the ESP32 in WiFi Access Point mode, serving a custom HTML control interface directly from the microcontroller. The operator connects their phone (iPhone or Android) to the GhostESP WiFi network and opens 192.168.4.1 in their phone's browser — no app download or installation required. This approach was chosen over MIT App Inventor and Bluetooth because it works on both iPhone and Android identically, has no pairing process, works over a longer range than Bluetooth, and eliminates connection instability issues. The web interface provides the same functionality (launch button, status display, countdown timer) that an App Inventor app would, with zero setup friction for the operator.`

## 11.3 App Features

| Feature | Purpose |
|---|---|
| `[Bluetooth connect button]` | `[Purpose]` |
| `[Score display]` | `[Purpose]` |
| `[Control button / slider / label]` | `[Purpose]` |

## 11.4 UI Mockup
Insert a sketch or screenshot of the app interface.

**Insert image below:**  
`[Upload image and link here]`

## 11.5 App Screen Flow

1. `[Step 1]`
2. `[Step 2]`
3. `[Step 3]`
4. `[Step 4]`

---

# 12. Bill of Materials

## 12.1 Full BOM

| Item | Quantity | In Kit? | Need to Buy? | Estimated Cost | Material / Spec | Why This Choice? |
|---|---:|---|---|---:|---|---|
| ESP32 DevKit v1 | 1 | Yes | No | 0 | 240MHz dual-core, built-in WiFi + BT | Only microcontroller with built-in WiFi AP capability in the kit |
| L298N motor driver module | 1 | Yes | No | 0 | Dual H-bridge, 12V 2A | Handles bidirectional DC motor control from 3.3V logic signals |
| DC gearbox motor (12V) | 1 | Yes | No | 0 | High torque, 30–60 RPM | Gearbox provides torque needed to pull platform weight uphill; raw DC motor lacks sufficient torque |
| Servo motor (SG90) | 1 | Yes | No | 0 | 180-degree, 4.8–6V | Small, lightweight, sufficient torque to snap ghost head; minimal weight addition to platform |
| HC-SR04 ultrasonic sensor | 1 | Yes | No | 0 | 2cm–400cm range, 5V | Reliable distance measurement; widely supported in MicroPython |
| Buck converter module | 2 | No | Yes | 120x2 | 7.4V to 5V step-down | Provides stable 5V to ESP32 and sensor without depending on L298N's onboard regulator under motor load |
| 18650 lithium cells | 2 | No | Yes | 200 | 3.7V 2600mAh each | Series connection gives 7.4V sufficient for motor; rechargeable; lightweight for moving platform |
| 18650 battery holder (2S) | 1 | No | Yes | 50 | 2-cell series holder | Clean series connection; replaceable cells |
| Hook pulley block | 1 | No | No (DIY) | 0 | Single wheel, hook mount, 30kg rated | Redirects pull-string so motor can be mounted on platform rather than fixed high anchor |
| Nylon rope 5mm, 10m | 1 | No | Yes | 200 | Transparent polypropylene / nylon | Near-invisible main rope makes ghost appear to float; strong enough to support platform weight taut over 9m |
| Toggle switch | 1 | Yes | No | 0 | SPST, rated 5A | Main power disconnect during charging |
| 1kΩ resistors | 3 | Yes | No | 0 | Through-hole, 1/4W | Voltage divider on HC-SR04 ECHO pin (5V to 3.3V) |
| Jumper wires | 1 set | Yes | No | 0 | Male-male and male-female | Component interconnections |
| Foam + white fabric (ghost prop) | 1 | No | Yes | (scrap/DIY) | Craft foam, light fabric | Ghost head and body — lightweight, easy to shape, achieves visual effect |
| Breadboard | 1 | Yes | No | 0 | Full size | Prototyping connections without soldering |

## 12.2 Material Justification
Explain why you selected your main materials and components.

Examples:
- Why acrylic instead of cardboard?
- Why MDF instead of 3D print?
- Why servo instead of DC motor?
- Why bearing instead of a plain shaft hole?

**Response:**  
`Green nylon rope was chosen over standard white clothesline because its color allows it to visually blend with surrounding trees and foliage, making the support less noticeable and enhancing the illusion that the ghost is floating rather than moving along a visible line. A gearbox motor was selected instead of a raw DC motor because the rope-and-platform mechanism requires higher torque, as a standard motor at similar voltage provides speed but insufficient pulling force. A buck converter was introduced after testing revealed that the onboard 5V regulator on the L298N becomes unstable under motor load, causing voltage drops and ESP32 brownouts during operation. WiFi AP mode was chosen over Bluetooth because it provides cross-platform compatibility without pairing, offers greater range, and enables a browser-based interface with real-time feedback such as countdown timers. The mask was constructed using a layered composite approach: a foil base shaped using a printed facial reference establishes the form, paper combined with adhesive (papier-mâché) creates a rigid outer shell, and clay is used to sculpt exaggerated features such as teeth and cheekbones, resulting in a lightweight yet structurally stable mask with high visual impact under low-light conditions.`

## 12.3 Items to Purchase Separately

| Item | Why Needed | Purchase Link | Latest Safe Date to Procure | Status |
|---|---|---|---|---|
| `Buck Converter` | `Different Voltages for different things` | `shop` | `[Date]` | `Received` |
| `Batteries` | `To make it wireless` | `[Link]` | `[Date]` | `Received` |
| `Clear nylon rope 5mm` | `Green main rope for ghost rail` | `Stationery` | `Week 1` | `Received` |
| `18650 cells x2 + holder` | `Self-contained mobile power for sliding platform` | `shop` | `Week 1` | `Received` |
| `Capacitors` | `For motor/ ESP32` | `shop` | `last week` | `Received` |
| `ISD1820 module and amplifier` | `for sound` | `shop` | `last week` | `Received` |

## 12.4 Budget Summary

| Budget Item | Estimated Cost |
|---|---:|
| Electronics | `570` |
| Mechanical parts | `96` |
| Fabrication materials | `60` |
| Purchased extras | `10` |
| Contingency | `0` |
| **Total** | `720-750` |

## 12.5 Budget Reflection
If your cost is too high, what can be simplified, removed, substituted, or shared?

**Response:**  
`The project came in under the informal budget target of INR 1,000. The largest savings came from using kit components for the ESP32, L298N, servo, sensor, resistors, and switch rather than purchasing them separately. The ghost prop was made from craft foam and fabric rather than 3D-printed components, saving significant cost and time. If budget were tighter, the buck converter could be replaced by powering the ESP32 from the L298N's onboard regulator (accepting occasional brownout risk), saving approximately INR 120.`

---

# 13. Planning the Work

## 13.1 Team Working Agreement
Write how your team will work together.

Include:
- how tasks are divided,
- how decisions are made,
- how progress will be checked,
- what happens if a task is delayed,
- how documentation will be maintained.

**Response:**  
`Tasks were divided based on skill sets: Gargi handled the entire electrical system, including wiring, coding, and integration of all electronic components, while Nishtha focused on designing and fabricating the ghost prop, particularly the face and its visual detailing. Key decisions were made collaboratively during each class session through quick verbal check-ins; in cases of disagreement, both approaches were prototyped and the more effective solution was selected. Progress was reviewed at the start of every session against weekly milestones, and if any task was delayed, the other member shifted to supporting work such as documentation or preparation. The README was consistently updated after each class session rather than being deferred to the end.
`

## 13.2 Task Breakdown

| Task ID | Task | Owner | Estimated Hours | Deadline | Dependency | Status |
|---|---|---|---:|---|---|---|
| T1 | Finalize concept and interaction design | Both | 2 | Week 1 | None | Done |
| T2 | Complete BOM and identify purchases | Both | 1 | Week 1 | T1 | Done |
| T3 | Procure all materials | Gargi | 3 | Week 1 | T2 | Done |
| T4 | Test ESP32, motor, L298N, servo, sensor individually | Gargi | 3 | Week 2 | T3 | Done |
| T5 | Build mechanical rope and pulley system | Gargi | 4 | Week 2 | T3 | Done |
| T6 | Write and test MicroPython code (motor + sensor + servo) | Gargi | 4 | Week 2 | T4 | Done |
| T7 | Build ghost prop and mount on platform | Nishtha | 2 | Week 2 | T3 | Done |
| T8 | Implement WiFi AP mode and web server in code | Gargi | 3 | Week 3 | T6 | Done |
| T9 | Build and style HTML control interface | Gargi | 2 | Week 3 | T8 | Done |
| T10 | Integrate full system — electronics on platform | Gargi | 4 | Week 3 | T5, T6, T7 | Done |
| T11 | End-to-end test and calibrate FORWARD_MS / REVERSE_MS | Both | 2 | Week 3 | T10 | Done |
| T12 | Playtest with unsuspecting participants | Both | 2 | Week 4 | T11 | Done |
| T13 | Debug and refine based on playtest findings | Gargi | 3 | Week 4 | T12 | Done |
| T14 | Complete README documentation | Gargi | 3 | Week 4 | T13 | Done |

## 13.3 Responsibility Split

| Area | Main Owner | Support Owner |
|---|---|---|
| Concept and gameplay | `Nishtha` | `Gargi` |
| Electronics | `Gargi` | `[Name]` |
| Coding | `Gargi` | `[Name]` |
| App | `Gargi` | `Nishtha` |
| Mechanical build | `Gargi` | `Nishtha` |
| Testing | `Nishtha` | `Gargi` |
| Documentation | `Nishtha` | `Gargi` |

---

# 14. Weekly Milestones

## 14.1 Four-Week Plan

### Week 1 — Plan and De-risk
Expected outcomes:
- [x] Idea finalized
- [x] Core interaction decided
- [x] Sketches made
- [x] BOM completed
- [ ] Purchase needs identified
- [ ] Key uncertainty identified
- [x] Basic feasibility tested

### Week 2 — Build Subsystems
Expected outcomes:
- [x] Electronics tests completed
- [ ] CAD / structure planning completed
- [x] App UI started if needed
- [x] Mechanical concept tested
- [x] Main subsystems partially working

### Week 3 — Integrate
Expected outcomes:
- [x] Physical body built
- [x] Electronics integrated
- [x] Code connected to hardware
- [x] App connected if required
- [x] First playable version exists

### Week 4 — Refine and Finish
Expected outcomes:
- [x] Technical bugs reduced
- [x] Playtesting completed
- [x] Improvements made
- [x] Documentation completed
- [x] Final build ready

## 14.2 Weekly Update Log

| Week | Planned Goal | What Actually Happened | What Changed | Next Steps |
|---|---|---|---|---|
| Week 1 | Finalize idea, buy parts, test motor | Concept finalized; all parts procured; motor and L298N verified on bench | Motor mounting location moved from fixed high anchor to sliding platform — eliminates wiring constraints | Begin mechanical rope build and individual component tests |
| Week 2 | Build rope system, test all components, write base code | Rope system built; all components tested individually; ghost prop made; base motor + sensor + servo code working | Servo code redesigned to reinitialise PWM on demand and deinit after each move — prevents jitter and buzzing | Integrate everything on platform; implement WiFi AP and web server |
| Week 3 | Full integration, web interface, end-to-end test | Full system integrated on platform; WiFi AP working; HTML page served from ESP32; end-to-end sequence verified | Discovered fetch() timeout bug on mobile (sequence takes 34s, browser times out at 30s) — fixed by sending HTTP response before starting sequence | Playtest, calibrate timings, fix remaining bugs |
| Week 4 | Playtest, refine, document | Playtesting produced strong reactions; several code bugs found and fixed; documentation completed | Pause time extended from 7.5s to 15s for better sensor coverage; Google Fonts removed; AP timeout guard added | Final submission |
---

# 15. Risks and Unknowns

## 15.1 Risk Register

| Risk | Type | Likelihood | Impact | Mitigation Plan | Owner |
|---|---|---|---|---|---|
| Pull-string snaps under tension | Mechanical | Medium | High | Use 2mm braided nylon string rated well above platform weight; inspect before each demo; carry spare string | Gargi |
| Platform jams mid-rope on a knot or kink | Mechanical | Medium | High | Keep rope as taut as possible; inspect full rope length before demo; test 5 full runs before public demo | Both |
| ESP32 brownouts when motor draws heavy current | Technical | Medium | Medium | Buck converter provides stable 5V independently of L298N; L298N onboard regulator not used for logic | Gargi |
| Phone shows "No Internet" warning and student cancels | Technical | Medium | Medium | Brief operator on iPhone workaround: tap "Use Without Internet" — takes 2 seconds | Nishtha |
| Ultrasonic sensor gives false readings | Technical | Low | Low | Sensor polled every 80ms with 999 returned on error; single false trigger causes servo sweep which is harmless | Gargi |
| Battery voltage drops and motor slows before end of rope | Technical | Medium | Medium | Fully charge cells before every demo; carry spare charged cells | Gargi |
| Rope sag makes ghost stop halfway | Mechanical | Medium | High | Tension rope as tight as possible between anchors; test with full platform weight before demo | Both |

## 15.2 Biggest Unknown Right Now
What is the single biggest uncertainty in your project at this stage?

**Response:**  
`The single biggest uncertainty is whether the gearbox motor has sufficient torque to pull the platform (estimated 600 to 800 grams) up the inclined rope at a consistent speed for the full 2-metre distance as the battery voltage gradually drops over multiple rounds. This determines whether FORWARD_MS remains accurate across a full demo session or needs to be recalibrated after every few runs.
`

---

# 16. Testing and Playtesting

## 16.1 Technical Testing Plan

| What Needs Testing | How You Will Test It | Success Condition |
|---|---|---|
| WiFi AP connection and web page load | Connect phone to GhostESP; open 192.168.4.1 in browser | Page loads within 5 seconds; all UI elements visible |
| Motor forward and reverse | Send launch command; observe platform travel; check Thonny serial output | Platform travels full rope length in both directions; stops cleanly at each end |
| Motor timing calibration | Time 5 forward runs with stopwatch; average the milliseconds | Platform consistently reaches far end within ±0.5 seconds of target |
| Ultrasonic sensor detection | Stand at various distances (50cm, 80cm, 100cm, 120cm) during pause; observe servo | Servo triggers at 100cm and under; no false triggers at 120cm and above |
| Servo sweep motion | Trigger servo via sensor detection; observe physical movement | Servo moves smoothly to 0 degrees, holds, returns to 90 degrees; no jitter or buzzing after movement |
| Full sequence timing | Run complete sequence; time each phase | Forward 8s, pause 15s, reverse 8.5s; phone countdown approximately matches |

## 16.2 Playtesting Plan

| Question | How You Will Check |
|---|---|
| Do players understand what to do? | ` Watch operator navigate to 192.168.4.1 without instruction; count seconds to first successful launch` |
| Is the interaction satisfying? | `Observe operator's reaction when ghost fires; ask if they want to trigger it again` |
| Do players want another turn? | ` After being scared, offer operator role to target; count how many accept immediately` |
| Is the challenge balanced? | `Time how long operator waits before finding the right moment; observe whether this feels tense or boring ` |
| Is the response clear and immediate? | `Measure time from button tap to motor movement; observe if operator notices any lag` |

## 16.3 Testing and Debugging Log

| Date | Problem Found | Type | What You Tried | Result | Next Action |
|---|---|---|---|---|---|

| Date   | Problem Found                                                             | Type           | What You Tried                              | Result                                             | Next Action                                                                                                     |
| ------ | ------------------------------------------------------------------- | -------------- | ------------------------------------ | -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| Week 2 | Buck converter output not reducing from ~7.4V                       | Technical      | Rotated potentiometer multiple turns | Failed — voltage stayed near input, clicking sound | Identified faulty/ineffective tuning; avoided using unstable output for ESP32 and ensured regulated 5V supply |
| Week 2 | ESP32 heating slightly during standalone power                      | Technical      | Continued running without changes    | Partly concerning                                  | Ensured input voltage is within safe limits (~5V) and stabilized supply using proper regulation               |
| Week 2 | Servo jittering/buzzing at rest                                     | Technical      | Kept PWM always active               | Failed — constant buzzing                          | Deinitialized PWM after movement to stop jitter                                                               |
| Week 3 | Ultrasonic sensor giving constant/incorrect readings (~1–2 cm / -1) | Technical      | Direct connection without resistors  | Failed — unstable readings                         | Added proper voltage divider on ECHO and powered sensor from stable 5V                                        |
| Week 3 | Ultrasonic sensor not responding consistently                       | Technical      | Powered via 3.3V pin                 | Failed — unreliable operation                      | Switched to 5V supply from buck converter                                                                     |
| Week 3 | Bluetooth connection drops immediately after connecting             | Technical      | Attempted BLE connection via phone   | Failed — unstable/disconnects                      | Switched to WiFi AP mode with HTTP control                                                                    |
| Week 3 | Phone control unreliable / complex via app                          | UX / Technical | Used MIT App Inventor                | Partly worked but inconsistent                     | Replaced with HTML web interface hosted on ESP32                                                              |
| Week 3 | Browser request timing out after launch                             | Technical      | Increased timeout duration           | Failed — browser-side limitation                   | Sent HTTP response before running sequence (non-blocking trigger)                                             |
| Week 3 | Ghost movement inconsistent / not smooth                            | Mechanical     | Adjusted rope tension loosely        | Made motion worse                                  | Re-tensioned rope tightly for stable linear motion                                                            |
| Week 4 | Motor performance drops after multiple runs                         | Technical      | Checked battery levels               | Voltage drop observed                              | Recharge batteries before demo and account for slight timing variation                                        |


## 16.4 Playtesting Notes

| Tester | What They Did | What Confused Them | What They Enjoyed | What You Will Change |
|---|---|---|---|---|
| Classmate 1 | Walked through demo space unaware; screamed and jumped backward | Nothing — had no idea what was coming | The physical ghost actually flying toward them; the servo hand snap at close range | Increase servo sweep speed slightly for more drama |
| Classmate 2 (as operator) | Connected to WiFi in under 30 seconds; launched immediately | Momentarily confused by "Use Without Internet" prompt on iPhone | Having total hidden control over when to launch; watching the target's reaction from a distance | Add a note in the web UI reminding iPhone users to tap "Use Without Internet" |
| Classmate 3 | Spotted the rope first but not the ghost; was still scared when it launched | Why the ghost paused at the far end | The unexpected second scare from the servo head snap during the pause | Add subtle camouflage to the rope platform at rest position |

---

# 17. Build Documentation

## 17.1 Fabrication Process
Describe how the project was physically made.

Include:
- cutting,
- 3D printing,
- assembly,
- fastening,
- wiring,
- finishing,
- revisions.

**Response:**  
`The ghost prop was fabricated using a layered approach to balance structure and visual detail. The mask was first shaped using aluminium foil over a printed facial reference to establish the base form. This was then covered with paper strips soaked in glue (papier-mâché), creating a hardened outer shell once dried. Clay was added on top to sculpt exaggerated features such as teeth and cheekbones, enhancing the expressive quality of the face. The mask was then painted to achieve the final effect, with attention to contrast and texture for better visibility in low-light conditions. The body was constructed using lightweight materials to support smooth motion; a black netted cloth sourced as scrap from a friend was used for the main drape, and a black stocking was repurposed to add layering while keeping the structure light and flexible.

The electronic and mechanical systems were assembled and integrated with the prop after fabrication. Components such as the ESP32, motor driver, ultrasonic sensor, and power modules were wired using jumper connections and positioned securely to prevent movement during operation. The motor and rope mechanism were mounted and aligned to ensure consistent linear motion, with multiple revisions made to rope tension and positioning for stability. Final assembly involved combining the prop with the motion system, followed by iterative testing and adjustments to ensure reliable performance and synchronized interaction between movement, sensing, and control.`

## 17.2 Build Photos
Add photos throughout the project.

Suggested images:
- early sketch,
- prototype,
- electronics testing,
- mechanism test,
- app screenshot,
- final build.

Example:
```md



```

## 17.3 Version History

| Version | Date | What Changed | Why |
|---|---|---|---|
| `v1` | `[Date]` | `[Describe]` | `[Reason]` |
| `v2` | `[Date]` | `[Describe]` | `[Reason]` |
| `v3` | `[Date]` | `[Describe]` | `[Reason]` |

---

# 18. Final Outcome

## 18.1 Final Description
Describe the final version of your project.

**Response:**  
`Project Wraith is a fully functional kinetic jumpscare installation. A self-contained sliding platform carrying an ESP32, L298N motor driver, DC gearbox motor, servo motor, HC-SR04 ultrasonic sensor, and 7.4V battery pack rides along a 9-metre inclined clear nylon rope. An operator connects their phone to the ESP32's GhostESP WiFi hotspot (no internet required, works on iPhone and Android) and opens a custom dark-themed web control panel at 192.168.4.1. Tapping the single LAUNCH button sends the ghost flying silently down the rope toward unsuspecting targets. At the far end the ghost pauses for 15 seconds while the sensor scans for nearby people — anyone within 100cm triggers a 90-degree servo handd snap. The ghost then automatically returns to start, ready for the next round.`

## 18.2 What Works Well
- The WiFi AP approach eliminated all connection issues — phone connects to GhostESP and the page loads in under 5 seconds every time with no pairing, no app, and identical behaviour on iPhone and Android.
- The 15-second pause with autonomous sensor-triggered servo sweep adds a second unpredictable scare layer that even people who spotted the ghost do not expect.
- The self-contained platform design means the entire system can be set up in any location in under 10 minutes with just a rope and two anchor points.

## 18.3 What Still Needs Improvement
- The balance between the weight of the ghost prop and the tension of the rope still needs refinement; slight inconsistencies in weight distribution affect the smoothness of motion and can cause minor jerks during travel. A more evenly balanced structure or guided track system would improve stability.
- The rope setup requires very precise tensioning to function correctly — if it is even slightly loose or overly tight, the motion becomes inconsistent. A more controlled mechanism, such as a pulley or guided rail, would make movement more reliable and easier to calibrate.
- The web interface countdown timer is still approximate, as it is based on fixed motor timings; variations in speed due to load or battery levels can cause the system to reset before the ghost has fully returned. A feedback-based system (e.g., limit switches or sensors) would improve accuracy.

## 18.4 What Changed From the Original Plan
How did the project change from the initial idea?

**Response:**  
The most significant change was moving the motor from a fixed position at the high anchor to the sliding platform itself. This eliminated the need for any trailing wires, slip rings, or complex cable management — all electronics ride with the ghost. The control method also changed from MIT App Inventor over Bluetooth to a custom HTML page served over ESP32 WiFi AP mode, which proved far more reliable (especially on iPhone), simpler to operate, and capable of showing a richer interface with a countdown timer and status log. The pause duration was extended from 7 to 8 seconds to 15 seconds to give the ultrasonic sensor sufficient time to reliably detect passersby and trigger the servo. The weight of the whole thing that caused a lot of load on the motor was also tried to be resolved.

---

# 19. Reflection

## 19.1 Team Reflection
What did your team do well?  
What slowed you down?  
How well did you manage time, tasks, and responsibilities?

**Response:**  
The team worked well together with a clear division of responsibilities — Gargi handled all electronics debugging and code architecture while Nishtha managed the interface design, fabrication, and documentation. The biggest time sink was debugging the servo jitter issue, which required understanding how MicroPython's PWM peripheral behaves when left running at rest. We underestimated how much iteration the mechanical system would need — rope tension, string routing, and motor torque all interacted in ways that only became clear during physical testing, not planning. Time management was generally good; we stayed approximately on schedule across all four weeks.

## 19.2 Technical Reflection
What did you learn about:
- electronics,
- coding,
- mechanisms,
- fabrication,
- integration?

**Response:**  
This project helped build a strong understanding of practical electronics, especially power stability and safely connecting components with different voltage levels. In coding, it emphasized writing structured logic for sequences, timing, and handling real-world behavior through testing and debugging. Mechanically, it showed how weight, rope tension, and motor torque directly affect movement and stability. Fabrication involved balancing lightweight materials with visual impact using foil, papier-mâché, clay, and fabric. Overall, the biggest learning was integration — how electronics, mechanics, and design must work together, requiring constant iteration to achieve a reliable system.

## 19.3 Design Reflection
What did you learn about:
- designing for play,
- delight,
- clarity,
- physical interaction,
- player understanding,
- iteration?

**Response:**  The asymmetric operator-target dynamic was the right design choice. Having one person with total hidden control creates an experience that feels fundamentally different from a passive decoration — the operator becomes invested in finding the perfect moment, which creates its own layer of engagement separate from the scare itself. The single-button interface on the web page was the right call — more controls would have distracted the operator at the critical moment. The 15-second pause with autonomous sensor triggering adds unpredictability even for the operator, which keeps the experience fresh across multiple rounds.

## 19.4 If You Had One More Week
What would you improve next?

**Response:**  
With additional time, the primary focus would be on refining the weight distribution and overall structure of the ghost prop to ensure smoother and more consistent movement. The current setup is sensitive to imbalance, which affects stability during travel. Another key improvement would be reducing friction in the rope mechanism, as it currently impacts the efficiency and smoothness of motion. Addressing these factors through better material choices, alignment, or guided supports would significantly improve performance and reliability. The motor's torque is less as well and can be improved with more voltage supply.

---

# 20. Final Submission Checklist

Before submission, confirm that:
- [x] Team details are complete
- [x] Project description is complete
- [x] Inspiration sources are included
- [x] Player journey is written
- [x] Sketches are added (placeholder — insert photos)
- [x] BOM is complete
- [x] Purchase list is complete
- [x] Budget summary is complete
- [x] Mechanical planning is documented
- [x] App planning is documented (not applicable — WiFi web interface used instead)
- [x] Code flowchart is added
- [x] Task breakdown is complete
- [x] Weekly logs are updated
- [x] Risk register is complete
- [x] Testing log is updated
- [x] Playtesting notes are included
- [x] Build photos are included
- [x] Final reflection is written

---

# 21. Suggested Repository Structure

```text
project-repo/
├── README.md
├── images/
│   ├── concept-sketch.jpg
│   ├── labeled-sketch.jpg
│   ├── circuit-diagram.jpg
│   ├── ui-mockup.jpg
│   ├── prototype-1.jpg
│   └── final-build.jpg
├── code/
│   ├── main.py
│   ├── test_code.py
│   └── notes.md
├── cad/
│   ├── models/
│   └── screenshots/
└── docs/
    ├── references.md
    └── extra-notes.md
```

---

# 22. Instructor Review

## 22.1 Proposal Approval
- [ ] Approved to proceed
- [ ] Approved with changes
- [ ] Rework required before proceeding

**Instructor comments:**  
`[Instructor fills this section]`

## 22.2 Midpoint Review
`[Instructor fills this section]`

## 22.3 Final Review Notes
`[Instructor fills this section]`
