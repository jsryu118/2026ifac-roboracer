---
title: ROBORACER GRAND PRIX Rules
layout: page
section: race
language: en-US
base_url: rules.html
---

<style>
.post ol {
  list-style-type: lower-alpha;
}

.post ol ol,
.post ul ol {
  list-style-type: lower-roman;
}
.post ol, .post ul, .post p {
  margin-bottom: 0rem;
}
h2, h3, h4, h5, h6 {
  margin-top: 1rem;
  margin-bottom: 1rem;
}
</style>


*Last Updated: 2026-07-15*


**Table of content**
- ToC
{:toc}


# 1. Overview

The international ROBORACER autonomous racing competition is open to teams of all levels. A team may consist of any number of members, but each participant must be a **member of only one team**.

The competition takes place as an in-person event at **IFAC 2026**, held at **BEXCO**, Busan, from **Monday, August 24** to **Thursday, August 27, 2026**.

**ROBORACER GRAND PRIX schedule: Monday, August 24 – Thursday, August 27, 2026**

Teams can **register** for the competition through the **official website**.

## 1.1 Competition Generals

1. The competition consists of five phases:
   - **Phase 0**: Submission of the team's technical materials on autonomous driving
   - **Phase 1**: Registration and inspection
   - **Phase 2**: Mapping and practice sessions (mapping, official practice, free practice)
   - **Phase 3**: Qualifying (missions, time trial)
   - **Phase 4**: Head-to-head races

2. Teams registered for the in-person competition must provide and build their own vehicles according to the constraints listed below. Each team must also have its own unique vehicle (i.e. one lab cannot enter multiple teams with a single vehicle).

3. To improve the quality of future ROBORACER competitions, the winner of each race is encouraged to open-source their algorithm code in the [ROBORACER Autonomous Racing Community repository](https://github.com/f1tenth) on Github under an open-source license.

# 2. Technical Material Submission

1. Teams must submit technical materials about their car during the pre-competition registration process.
2. No specific format is required.
3. The submission must include a summary of the **software and hardware technology** of the team's autonomous vehicle.
4. Please respect the deadline.

# 3. Registration and Inspection

## 3.1 Vehicle Class

The **vehicle class** only allows vehicles that satisfy the following constraints:

1. Vehicles must be built according to the ROBORACER guidelines, but alternative parts may be allowed as long as they comply with the regulations. Anything unclear or ambiguous must be confirmed with the race organizers in advance.

2. Each vehicle is inspected as part of qualifying to confirm it meets the criteria. Vehicles that do not meet the criteria cannot participate.

3. **The ROBORACER competition is an algorithm competition. Hardware that creates an advantage is not allowed**.

4. **Chassis**:
   The race is designed around **1:10 Traxxas** chassis (e.g. TRA74054, TRA6804R). These chassis are recommended, but chassis generally within 15% of the Traxxas vehicle dimensions are allowed (238mm ≤ width ≤ 341mm, 454mm ≤ length ≤ 654mm). Both **4WD and 2WD** are allowed.

5. **Tires**:
   **No restrictions** (both sponge and rubber allowed). However, **chemical additives are strictly prohibited**.

6. **Main computing unit**:
   **No restrictions** on specifications. Only one computing unit may be used.

7. **LiDAR**:
   **No restrictions** on specifications. Only one LiDAR sensor may be used. **3D LiDAR** is also allowed.

8. **Camera**:
   Both **single cameras** (e.g. Logitech C270, Logitech C920, Raspberry Pi Camera Module V2, Arducam) and **stereo cameras** (e.g. Intel Realsense, ZED) are allowed. Cameras that provide additional information such as **detection or VIO results** from in-camera processing are **not allowed**. (Depth information is allowed.)

9. **Motor**:
   **No restrictions** on specifications. Only a **single motor** may be used in the powertrain.

10. **Battery**:
    **4S LiPo battery** or **3S and below**. There is no limit on the number of batteries, as long as the total cell count does not exceed 4S (e.g. 2S + 2S is allowed).

11. **Detection box**:
    The vehicle must be easily detectable by the opponent's LiDAR. Therefore, the vehicle must occupy a rectangular space of at least **12×12cm** on every horizontal plane between **10~30cm** above the ground.
    - Occupying only 3 faces is not allowed. All 4 faces must be enclosed.

12. **Foam bumper**:
    Bumpers must be soft to minimize damage. When more than one vehicle is on the track, these two components (detection box and foam bumper) must be attached.

13. **Other sensors**:
    Other sensors (IMU, encoders, custom electronic speed controllers) are allowed. Indoor GPS sensors (e.g. Marvelmind) are **not allowed**.

## 3.2 Track and Racing Environment

The competition takes place at BEXCO, Busan. The environment where the track will be built has the following characteristics:

<center>
<img src="../images/environment/bexco_hall_1.jpg"  style="width: 25vw" />
</center>

The floor of Hall 5A on the 3rd floor of BEXCO Exhibition Center 2, where the track is installed, is hardened concrete with a urethane coating finish. This surface is characterized by a significantly lower friction coefficient and a smoother finish than typical asphalt pavement.

The track size is approximately **8 m × 22 m**.

<center>
<img src="../images/rules/track_layout_2026.png" style="width: 30vw; min-width: 320px;" />
</center>

This is the approximate map shape, and it may change slightly.

## 3.3 Inspection

- The purpose of the inspection is to confirm that the vehicle meets the competition requirements and is not dangerous to the environment, opponents, or people.
- Vehicles must be built according to the ROBORACER guidelines, but alternative parts may be allowed as long as they comply with the regulations.
- Vehicle inspection takes place on the first day of the competition.
- The inspection is performed by the race referees.
- The inspection must be completed **before practice**, and a **re-inspection is required after any hardware change**.

### 3.3.1 Software Inspection

- Teams must demonstrate that the emergency brake can be operated in a **toggle (on/off) manner**.
- For the toggle-type emergency brake, **use by a human anticipating a collision is prohibited.**

### 3.3.2 Hardware Inspection

- **Chassis Dimension**: the vehicle size must comply with the regulations specified in section 3.1.
- **Detection Box Dimension**: the detection box must occupy at least **12 × 12 cm** on horizontal planes at a height of **10~30 cm** above the ground.

# 4. Mapping and Practice

## 4.1 Mapping

- Mapping proceeds as a **group session** — all teams within the group map together on the track at the same time.
- **Algorithm testing is prohibited during the group mapping session.**
- Teams without a map file may receive one from nearby teams, but this is unrelated to the organizers.
- In this competition, **png, yaml** (for **particle filter** localization) and **pbstream** (for **cartographer** localization) files of the track are provided.

## 4.2 Practice

- Each team may prepare multiple vehicles, but only one vehicle per team may be on the track.
- Sample obstacles are provided.
- No liability is assigned for accidents that occur during practice.
- However, a team involved in an accident is obliged to explain its algorithm upon the referee's request.
- Practice proceeds in groups, and depending on the situation, practice time open to all teams may also exist.

# 5. Qualifying (Missions, Time Trial)

<!-- <center>
<img src="../images/rules/qualification.png"  style="width: 20vw" />
</center> -->

<!--수정 필요-->

## 5.1 General

- Practice and qualifying both use the same track.
- Every stage of qualifying must be completed within **8 minutes**.
  - This may change depending on the total number of participating teams.
- Qualifying consists of **3 missions** — **Q1, Q2, Q3** — and **1 achievement condition** called **Fully Autonomous**.
- Q1 through Q3 proceed sequentially and cannot be skipped.
- Between Q1, Q2, and Q3 there is **one buffer lap** each for installing and removing obstacles.

## 5.2 Qualifying 1 (Q1)

- Qualifying 1 aims to complete **3 laps** **without collision** on an **obstacle-free track**.
- **No obstacles are placed on the track during Q1.**
- Vehicles that do not pass Qualifying 1 are ranked by how many laps they completed without collision.
- Vehicles that pass Qualifying 1 move on to Qualifying 2.

## 5.3 Qualifying 2 (Q2)

- Qualifying 2 aims to complete **3 laps** **without collision** against **random obstacles**.
- The random obstacles in Qualifying 2 are placed by the referees, with a total of **2** placed. The obstacle positions are not announced in advance.
- Vehicles that do not pass Qualifying 2 are ranked by how many laps they completed without collision.
- Vehicles that pass Qualifying 2 move on to Qualifying 3.

## 5.4 Qualifying 3 (Q3)

- Qualifying 3 aims to achieve the **minimum lap time** on an obstacle-free track for 2 minutes.
- The shortest lap time achieved while running freely for 2 minutes is used.
- If human intervention occurs, the lap time is invalidated.

## 5.5 Fully Autonomous (Achievement Condition)

- The achievement condition applies at every moment of qualifying.
- The achievement condition is as follows.
  - **A team whose vehicle was not directly or indirectly influenced by a person during the entire qualifying process**
  - Cases of being stopped for more than 5 seconds are excluded.
- Direct or indirect influence includes:
  - Touching the vehicle
  - Operating a joystick
  - Touching the keyboard/mouse
  - Operating the computer
- For a perfect achievement, poses like the following are recommended.

<center>
<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;">
<img src="../images/rules/ex_joy.png" style="width: 400px; max-width: 45%;" />
<img src="../images/rules/ex_laptop.png" style="width: 400px; max-width: 45%;" />
</div>
</center>

## 5.6 Static Obstacles

- The obstacles placed randomly during Q2 are static obstacles.
- The detailed regulations follow [8. Static Obstacles](#8-static-obstacles).

## 5.7 Invalidated Records

- If a human intervenes and affects the vehicle, the **lap time is invalidated** and the lap is **excluded from the completed lap count**.
- If there is contact with a static obstacle, the **lap time is invalidated** and the lap is **excluded from the completed lap count**.
- If the vehicle touches the track but can continue driving without human intervention, it is considered minor contact and the record remains valid.

## 5.8 Final Ranking Decision

- The final qualifying ranking is decided by the following criteria, in order.
  - Whether Fully Autonomous was satisfied
  - The number of qualifying missions passed
  - The record of the last qualifying mission completed
- An example of the final ranking decision is as follows.
  - Assume there are 12 teams in total.
  - Assume 3 teams satisfied Fully Autonomous, 3 teams passed Q3 (without FA), 3 teams failed Q2 (passed Q1), and 3 teams failed Q1.
  - Among the teams that satisfied the Fully Autonomous condition, ranks 1 to 3 are assigned by Q3 record.
  - Among the teams that passed Q3 (without Fully Autonomous), ranks 4 to 6 are assigned by Q3 record.
  - Among the teams that failed Q2, ranks 7 to 9 are assigned by the number of laps partially completed in Q2.
  - Among the teams that failed Q1, ranks 10 to 12 are assigned by the number of laps partially completed in Q1.

### 5.8.1 Qualifying Example

<table>
<thead>
<tr>
<th>Rank</th>
<th>Fully Autonomous</th>
<th>Q3 (fastest lap)</th>
<th>Q2 (laps completed)</th>
<th>Q1 (laps completed)</th>
</tr>
</thead>
<tbody>
<tr><td>1</td><td>O</td><td>10.8 s</td><td>3</td><td>3</td></tr>
<tr><td>2</td><td>O</td><td>11.2 s</td><td>3</td><td>3</td></tr>
<tr><td>3</td><td>O</td><td>13.0 s</td><td>3</td><td>3</td></tr>
<tr><td>4</td><td>X</td><td>9.9 s</td><td>3</td><td>3</td></tr>
<tr><td>5</td><td>X</td><td>10.1 s</td><td>3</td><td>3</td></tr>
<tr><td>6</td><td>X</td><td>12.2 s</td><td>3</td><td>3</td></tr>
<tr><td>7</td><td>X</td><td>-</td><td>2</td><td>3</td></tr>
<tr><td>8</td><td>X</td><td>-</td><td>1</td><td>3</td></tr>
<tr><td>9</td><td>X</td><td>-</td><td>0</td><td>3</td></tr>
<tr><td>10</td><td>X</td><td>-</td><td>-</td><td>2</td></tr>
<tr><td>11</td><td>X</td><td>-</td><td>-</td><td>1</td></tr>
<tr><td>12</td><td>X</td><td>-</td><td>-</td><td>0</td></tr>
</tbody>
</table>

## 5.9 Cautions

- For other common cautions, see [7. Common Cautions](#7-common-cautions-important).

## 5.10 Reference Video

<center>
  <iframe width="896" height="504" style="max-width: 70%;" src="https://www.youtube.com/embed/SlJMuDHodnY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</center>

# 6. Head-to-Head Races

<!-- <center>
<img src="../images/rules/head_to_head.png"  style="width: 13vw" />
</center> -->

<!--수정 필요-->

## 6.1 Tournament Format

- Head-to-head races proceed in a **Double Elimination** format.
- Each team is eliminated after **two losses**.
- **Day 3 (August 26):** Winners Bracket — no team is eliminated on this day.
- **Day 4 (August 27):** Losers Bracket races begin. Teams eliminated from the Winners Bracket join the Losers Bracket.
- The final winner is decided through the bracket.
- Depending on the number of participating teams, a regular tournament may be used instead.

## 6.2 General

- The two vehicles start from different start lines located on opposite sides.
- A total of 3 static obstacles are used. After all teams complete their race preparations, each participating team installs one obstacle, and the referee installs the other one.
- The static obstacles on the track are removed when the leading vehicle has completed 10 laps.
- Each vehicle must be the first to complete 20 laps within the time limit while avoiding obstacles and the opponent.

## 6.3 Objective

- Be the first to complete 20 laps.
  - Races before the quarterfinals may be adjusted to 10 laps.

## 6.4 Random Static Obstacles

- The detailed regulations follow [8. Static Obstacles](#8-static-obstacles).

## 6.5 Collisions

- Track boundary and static obstacles
  - If the race can continue, it must continue without interruption.
- Vehicle vs. vehicle
  - **Do not stop the race at the team's discretion without the referee's stop signal.**
  - If the offending vehicle is clear but did not overtake, the race continues as is.
  - If the victim vehicle is clear and cannot drive, the collision is severe, or it is overtaken, the race is stopped.

## 6.6 Cautions

- Vehicles whose detection box violates the regulations cannot participate in the race.
- For contact and accidents that occur while driving side by side, the race is not stopped if there is no clear offender.
- For other common cautions, see [7. Common Cautions](#7-common-cautions-important).

# 7. Common Cautions (Important)

## 7.1 Vehicle Computation, Communication & Control

- **All computation must be performed onboard the vehicle.**
- **No data may be transmitted to the vehicle during normal driving.**
- **Manual (human) emergency braking during normal driving is strictly prohibited.**
- **Using** or **pressing** a joystick during a race is **not allowed**.
  - Please change the module for **switching** between autonomous ↔ human control from a "**press and hold**" style to an "**on/off**" **toggle** style.
- Only one laptop may be connected, for visualization (e.g. RViz) or debugging purposes.

## 7.2 Safety

- If driving is difficult or dangerous due to a collision, the vehicle must be emergency-stopped immediately.
- People are prohibited from being on the track.
- Sharing one vehicle across multiple teams is strictly prohibited.
- Whenever more than one vehicle can be on the track, the detection box must be attached. (e.g. it does not need to be attached during qualifying.)

## 7.3 Track & Obstacle Handling

- If the vehicle is stopped too close to an obstacle ahead (an opponent vehicle or a static obstacle) and cannot make an avoidance maneuver, it may be moved back slightly.
- In the finals, a collision with an obstacle is fine as long as the vehicle can keep driving. For how obstacle contact affects qualifying records, see [5.7 Invalidated Records](#57-invalidated-records).
- If the vehicle is taken off the track and put back for any reason, its heading may be adjusted slightly, but it must be placed back at the **position where it left**.
- If there is contact with the track, even if the record is not invalidated, the track must be **restored to its original position immediately**.
- If there is contact with an obstacle, it must be restored to its original position immediately.

## 7.4 Operations

- **No appeals regarding Wi-Fi are accepted.** Make sure your autonomous system is designed to operate independently of Wi-Fi conditions. We will ask teams not participating in a race to turn off their Wi-Fi, but this is purely to ease teams' visualization and debugging — not for algorithm performance.
- All hardware repair and maintenance on the track (repairing broken parts, recalibrating sensors, swapping batteries, etc.) is prohibited.
- The dedicated time for **mapping**, **official practice**, and **qualifying** may vary depending on the number of participating teams.
- The dedicated time for **mapping** and **official practice** sessions is assigned on a **first-come, first-served basis**, and only teams that have **successfully completed registration and inspection** are eligible.

# 8. Static Obstacles

**Common**

- Each obstacle is smaller than 0.5m x 0.5m.
- Obstacles are removed safely when the vehicle is not affected.
  - Removal may be slightly delayed depending on the race situation.
- Obstacles must be restored immediately after a collision.
  - The restoration process must not affect the opponent.
- The minimum distance between obstacles is 1m.
- Even with an obstacle in place, the track width must provide a minimum clearance of 0.5 m.

**Qualifying only**

- Random obstacles are placed by the referees, with a total of **2** placed.
- The obstacles are removed after Q2 is completed.
- The obstacle positions are not announced in advance.

**Finals only**

- The participating teams and the referee each place one obstacle, for a total of 3 static obstacles.
- The obstacles are removed once a vehicle completes half of the race.
- The obstacle positions are set after both vehicles have finished their preparations at the start lines.
  - After the obstacles are placed, modifying code or changing paths is prohibited.
  - After the obstacles are placed, only the start signal may be transmitted to the vehicle.
- Obstacles cannot be placed within 1m of the start positions.

# 9. Penalties

**Rulings on incidents are at the discretion of the on-site referees and must be respected.**

Even for an incident involving **multiple violations**, only **one penalty** is applied per incident.

<table>
<thead>
<tr><th>Violation</th><th>Qualifying</th><th>Finals</th></tr>
</thead>
<tbody>
<tr><td>Human path modification or selection based on obstacle position</td><td><span style="color:#e67e22; font-weight:bold;">one-rank demotion</span></td><td><span style="color:#e74c3c; font-weight:bold;">1-lap penalty</span></td></tr><tr><td>Using a joystick, keyboard, or mouse during a race <sup>[a]</sup></td><td><span style="color:#e67e22; font-weight:bold;">one-rank demotion</span></td><td><span style="color:#b8860b; font-weight:bold;">warning</span></td></tr>
<tr><td>Failing to actively repair a track damaged by a collision <sup>[b]</sup></td><td><span style="color:#e67e22; font-weight:bold;">one-rank demotion</span></td><td><span style="color:#b8860b; font-weight:bold;">warning</span></td></tr>
<tr><td>False start</td><td>-</td><td><span style="color:#b8860b; font-weight:bold;">warning</span></td></tr>
<tr><td>Detection box not properly secured <sup>[c]</sup></td><td>-</td><td><span style="color:#b8860b; font-weight:bold;">warning</span></td></tr>
<tr><td>Indirect interference with the opponent's vehicle during a race <sup>[d]</sup></td><td>-</td><td><span style="color:#b8860b; font-weight:bold;">warning</span></td></tr>
<tr><td>Minor rear-end collision</td><td>-</td><td><span style="color:#b8860b; font-weight:bold;">warning</span></td></tr>
<tr><td>Direct interference with the opponent's vehicle <sup>[e]</sup></td><td>-</td><td><span style="color:#e74c3c; font-weight:bold;">1-lap penalty</span></td></tr>
<tr><td>Causing an accident with a heavy impact</td><td>-</td><td><span style="color:#e74c3c; font-weight:bold;">1-lap penalty</span></td></tr>
<tr><td>Accumulating 3 warnings</td><td>-</td><td><span style="color:#e74c3c; font-weight:bold;">1-lap penalty</span></td></tr>
<tr><td>Accumulating penalty laps totaling 3 extra laps</td><td>-</td><td><span style="color:#8b0000; font-weight:bold;">disqualification</span></td></tr>
</tbody>
</table>

**Details**

1. **Using a joystick, keyboard, or mouse**: Allowed exceptions:
   - When the vehicle is removed from the track
   - Sending an initial guess for re-localization
   - When the referee declares a race stop and an emergency stop is needed
   - Sending the start signal at a start or restart
   - When an emergency stop is needed because the vehicle cannot drive due to a collision
   - When an emergency stop is needed because the vehicle is stuck on an obstacle for more than 5 seconds
   - When an emergency stop is needed to prevent abnormal driving (ex. driving in reverse)
   - Stopping the vehicle after the race has ended
2. **Failing to repair a damaged track**: a new warning may be issued each lap if it is not properly repaired
3. **Detection box not properly secured**: a new warning may be issued each lap if it is not properly fixed
4. **Indirect interference with the opponent's vehicle**: being detected by the opponent vehicle's detection module while going to fix the track, affecting its driving.
5. **Direct interference with the opponent's vehicle**: physically contacting the opponent's vehicle while going to fix the track, affecting its driving

## 9.1 Example Cases

<table>
<tbody>
<tr><td style="vertical-align: top;"><img src="../images/rules/examples/valid1_주행가능.gif" style="width: 1440px; max-width: 100%;" /></td><td style="vertical-align: top;"><strong>Case 1</strong>: Contact with the track occurs, but the vehicle can continue driving in autonomous mode<br>No penalty in either qualifying or finals. However, the track must be corrected immediately after a collision.</td></tr>
<tr><td style="vertical-align: top;"><img src="../images/rules/examples/valid2_sujung.gif" style="width: 1440px; max-width: 100%;" /></td><td style="vertical-align: top;"><strong>Case 2</strong>: Contact with the track makes it impossible for the vehicle to continue driving<br>In qualifying, the lap time is invalidated. In finals, there is no penalty. When repairing the track, it is important not to affect the opponent's vehicle. Even if the repair is delayed slightly, it must be done when the opponent is not affected.</td></tr>
<tr><td style="vertical-align: top;"><img src="../images/rules/examples/invalid3_조이사용.gif" style="width: 1440px; max-width: 100%;" /></td><td style="vertical-align: top;"><strong>Case 3</strong>: After a collision, the vehicle is manually operated with a joystick and the race continues<br>In qualifying, in addition to lap time invalidation, the team is also demoted one rank. In finals, one warning is issued.</td></tr>
<tr><td style="vertical-align: top;"><img src="../images/rules/examples/invalid2_장애물_터치.gif" style="width: 1440px; max-width: 100%;" /></td><td style="vertical-align: top;"><strong>Case 4</strong>: Contact or collision with an obstacle occurs<br>Regardless of severity, even minor contact invalidates the lap time in qualifying. In finals, there is no penalty.</td></tr>
<tr><td style="vertical-align: top;"><img src="../images/rules/examples/invalid4_5초이상움직임X.gif" style="width: 1440px; max-width: 100%;" /></td><td style="vertical-align: top;"><strong>Case 5</strong>: The vehicle cannot proceed and stops in front of an obstacle for 5+ seconds<br>In qualifying, Fully Autonomous cannot be achieved. In finals, there is no penalty, and the vehicle may be taken off the track to adjust parameters.</td></tr>
</tbody>
</table>
