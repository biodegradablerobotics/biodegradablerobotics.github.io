#
# Snake Biomechanics Background and Initial Specifications

Team 3: SNEK (Sustainable &#39;N Eco-friendly Kobra)

Chris Breaux, George Muhn, Lien White, Timothy Graunke

##


## Candidate Organism

Our candidate organism is the red racer snake _Coluber flagellum piceus_ [1].

1. **List five of the most closely related research references on topics pertinent to your project, in IEEE format. Identify three citations which are most useful in creating initial specifications for your robot.**
  1. \* [What Defines Different Modes of Snake Locomotion?](https://academic.oup.com/icb/article/60/1/156/5818495?login=true) [2]
  2. [Analysis of Snake Movement Forms for Realization of Snake-like Robots](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&amp;arnumber=774054) [3]
  3. [Snake-like locomotion: Experimentations with a biologically inspired wheel-less snake robot](https://www.sciencedirect.com/science/article/pii/S0094114X08001791?casa_token=6d2-Cx3ZBlwAAAAA:4AvpvndeUjNc-Te5b_yt8oC4ng0ITnHuLjddWn1s9K9acWpJJon6TGRk86L_CripJWyUtYQxhTM) [4]
  4. \* [The mechanics of slithering locomotion](https://www.pnas.org/content/pnas/106/25/10081.full.pdf) [5]
  5. \* [The Biomechanics of Multi-articular Muscle–Tendon Systems in Snakes](https://academic.oup.com/icb/article/60/1/140/5811566?login=true) [6]

[2] describes the most commonly recognized modes of snake locomotion including rectilinear, lateral undulation, sidewinding, and concertina. Rectilinear locomotion is the linear shortening and lengthening of the snake&#39;s body to creep forward. Lateral undulation is the propagation of lateral waves towards the snake&#39;s tail that propel it forward. Sidewinding differs in that there are static regions of the snake&#39;s body that plant on the ground and push the snake sideways. Concertina is similar to sidewinding in that there are static regions of the snake&#39;s body, usually in bent shapes, that plant on the ground and push or pull the rest of the body forward. This paper proposes five distinct types of lateral undulation and four distinct types of concertina for a total of 11 distinct gaits. We will pick one of the four primary modes of locomotion to reproduce in our robot.

[5] paper develops a theoretical model for slithering locomotion that relies on the directional frictional properties of the scales combined with changing weight distribution. They experimentally measure the coefficient of friction of scales. They found that body inertia is not central to slithering locomotion, but motion arises by the interaction of surface friction and internal body forces. The body length, slithering angle, and slithering period were normalized at 30cm, 20deg, and 2s, so we will start with those parameters for our robot.

[6] This paper compares the performance of multi-articular and mono-articular muscular models of snakes. A multi-articular model describes muscles spanning multiple joints and must partition performance across the joints. A mono-articular model describes one joint actuated by one muscle. Multi-articular models partitioning of muscle cross-sectional area results in a small net loss in performance, but can reduce the forces needed in each muscle. Highly tendinous spans increase performance at lower metabolic cost but greater muscle strain, while highly muscular spans increase metabolic cost with no effect on muscle strain. We will consider both multi-articular and mono-articular models for our robot.

**Existing Bio-Inspired Robots**

1. **List five of the most closely-related research references on topics pertinent to your project in IEEE format. Identify three citations which are most useful in creating initial specifications for your robot.**
  1. [Analysis and control of a gait of snake robot](https://www.jstage.jst.go.jp/article/ieejias1987/120/3/120_3_372/_article/-char/ja/)[7]
  2. \*[Design of a modular snake robot](https://www.semanticscholar.org/paper/Design-of-a-modular-snake-robot-Wright-Johnson/698ca88c612ba132db0fca64ae4d8c42a27a6eb7) [8]
  3. [Modular Snake Robots](http://biorobotics.ri.cmu.edu/projects/modsnake/) [9]
  4. \*[AmphiBot II](https://infoscience.epfl.ch/record/142759/files/crespi06.pdf)[10]
  5. \*[Design and Architecture of a Series Elastic Snake Robot](https://www.semanticscholar.org/paper/Design-and-architecture-of-a-series-elastic-snake-Rollinson-Bilgen/43a417355f89692cb26a412d0d9aab257c6d95c9)[11]

[8] focuses on a snake robot made from easily accessible actuators and serial communications. The design chooses to model the &quot;string type&quot; robots in order to create a snake using servos that operate at the retrieval of a serial sensor signal via RS-485 from a previous link. The paper also addresses the challenges the engineers faced, such as those related to tangling wires and heated electronics. What is especially unique about this paper in comparison to others is it&#39;s detailed section on creating a &quot;skin&quot; for the snake bot. The skins were created to block dirt from entering into the electronics, which makes the reader assume their snake was meant to travel outdoors. This could help our team with a preliminary design idea to base our biodegradable robot on due to its simplicity in comparison to other snake bots. We also want to design our snake robot to be fit for the outdoors and soil and the section on the snake&#39;s skin may help inspire ideas for this area of our project.

[10] explains the design of a snake robot suitable for land crawling and swimming. The Amphibot II emcompasses a total of 7 degrees of freedom with one including the head. It also uses a PIC microcontroller to run DC motors and PD control encoders. What is unique about this design is the control system which uses a central pattern generator (or CPG) to output coupled oscillations as the snake&#39;s movement. The benefit of using a CPG is that any potential user of the AmphiBot II has full control over the final locomotion design. The user can change its speed and direction without having to focus on each degree of freedom of the robot. This design could help the team better understand the calculations behind the systems control design for our snake.

[11] details the design and architect behind a working snake robot composed of 1 DOF link created by the authors. They specify the materials, hardware, and control methods used. It also provides data related to velocity and torque over time. What makes this paper especially unique is its clearly listed specifications table, which could help our team create preliminary specifications for our own snake robot. The fact that they also provided their PID control template could help the team when it came to the software development of our snake robot.

**Specifications Table**

| **Parameter** | **Unit** | **Value Range** | **Reference** |
| --- | --- | --- | --- |
| Mass | kg | 0.115-0.256 | [1] |
| Body Length | meters | 0.33-1.65 | [5] |
| \*Slithering Period | seconds | 2-5 | [5] |
| Slithering Angle | degrees | 20-25 | [5] |
| Speed | m/sec | 0.100-0.150 | [5] |
| \*\*Power | W | 0.29 - 0.653 | [5] |

\*a slithering period is defined as a single right-left motion

\*\*Power = [0.2 \* (0.115, 0.256)kg \* 9.81m/s^2 \* 1.3m/s] = **0.293 - 0.653 watts**

**Figures of Biological System**

![](RackMultipart20210207-4-1mmkxpn_html_f377bc3642301c58.png)

Figure 1.

The musculoskeletal system of a snake that shows how a snake&#39;s muscle contracts and relaxes then interacting with its skeletal system. This system creates a S motion but straight path [2].

![](RackMultipart20210207-4-1mmkxpn_html_5f6d1614008f1a76.jpg)

Figure 2.

&quot;Dynamics of snake locomotion. (A–C) Position (X , Y ) and orientation theta of the snakes on a horizontal surface. Open circles show experimental results; solid lines show the theoretical results from a lifted-snake model, dashed lines for a uniform-weight model. Error bars show the standard deviation of the measurement. (Insets) (a&#39; and a&quot; ) show photographic sequences of snakes moving on smooth and rough surfaces respectively. (D) Snakes&#39; forward speeds U on a plane inclined at angle phi. Smooth curves represent theoretical predictions of steady-state speeds using uf given in the figure and frictional anisotropies of ut= 1.8 uf, ub= 1.3 f. Three regimes of motion exist for phi \&lt; 0°, the snake successfully slithers downhill; for 0°\&lt;phi\&lt; 7°, the snake successfully slithers uphill; for phi \&gt; 7°, the snake slides backwards when slithering uphill.&quot; [5].

**Simple Engineering Representation**

![](RackMultipart20210207-4-1mmkxpn_html_faaa3efb0a0c0beb.jpg)

![](RackMultipart20210207-4-1mmkxpn_html_e868f576ea4c7040.jpg)

##


## **Discussion**

1. **Discuss / defend your rationale for the size animal you selected in terms of your ability to replicate key features remotely with limited material selection.**

The largest red racer is 256 grams and 1.65 meters. This is not a lot of material or a very large footprint, so it will be relatively easy to reproduce. The size of the animal is not too large or too small to be built by disposable materials and use typical actuators and power sources.

1. **Find a motor and battery that can supply the mechanical power needs obtained above.** _Consider that motor efficiencies may be as high as 95%, but if you can&#39;t find it listed, assume you find a more affordable motor at 50-70% efficiency. Compare the mechanical watts/kg for the necessary motor and battery vs the animal&#39;s mechanical power/mass above? Which one is more energy dense?_

A 150:1 micrometal gear motor [12] and battery [13] that could fit our specifications for creating a snake like robot. This motor is small, light and produces a good amount of torque for our desired outcome. The battery is also small and light but would require a second battery in series to obtain the correct voltage for the motors. The batteries would also provide enough amp hours to power 1 motor for 2.6 hours at max current efficiency and power 3 motors for 55min at max efficiency. A drawback is the max efficiency of the motor is 33%.

For power rating output power for the motor at max efficiency is 0.3 Watts. This would provide a watts/kg ratio of 31.78 watt/kg, for purely the motor. A snake&#39;s average power to weight ratio is around 2.5 watt/kg. This would allow the team ~110g of weight for the rest of the material for the s.n.e.k. robot.

##


## **References**

[1] Howard Clark, Coachwhip (Masticophis flagellum), Sonoran Herpetologist 2010 23(11):150-154, [https://tucsonherpsociety.org/amphibians-reptiles/snakes/coachwhip/](https://tucsonherpsociety.org/amphibians-reptiles/snakes/coachwhip/)

[2] Bruce C Jayne, What Defines Different Modes of Snake Locomotion?, Integrative and Comparative Biology, Volume 60, Issue 1, July 2020, Pages 156–170, [https://doi.org/10.1093/icb/icaa017](https://doi.org/10.1093/icb/icaa017)

[3] S. Ma, &quot;Analysis of snake movement forms for realization of snake-like robots,&quot; Proceedings 1999 IEEE International Conference on Robotics and Automation (Cat. No.99CH36288C), Detroit, MI, USA, 1999, pp. 3007-3013 vol.4, doi: 10.1109/ROBOT.1999.774054.

[4] Z.Y. Bayraktaroglu, Snake-like locomotion: Experimentations with a biologically inspired wheel-less snake robot, Mechanism and Machine Theory, Volume 44, Issue 3, 2009, Pages 591-602, ISSN 0094-114X, [https://doi.org/10.1016/j.mechmachtheory.2008.08.009](https://doi.org/10.1016/j.mechmachtheory.2008.08.009).

[5] David L. Hu, Jasmine Nirodya, Terri Scotta, Michael J. Shelleya, The mechanics of slithering locomotion, PNAS, vol. 106, no. 25, Pages 10081-10085, June 23, 2009, [www.pnas.orgcgidoi10.1073pnas.0812533106](about:blank)

[6] Henry C Astley, The Biomechanics of Multi-articular Muscle–Tendon Systems in Snakes, Integrative and Comparative Biology, Volume 60, Issue 1, July 2020, Pages 140–155, [https://doi.org/10.1093/icb/icaa012](https://doi.org/10.1093/icb/icaa012)

[7] Pavel Prautsch, Tsutomu Mita, Tetsuya Iwasaki, Analysis and Control of a Gait of Snake Robot, IEEJ Transactions on D (Industrial Application), 2000, Vol. 120, No. 3, p. 372-381, [https://doi.org/10.1541/ieejias.120.372](https://doi.org/10.1541/ieejias.120.372)

[8] Wright, C., Johnson, A.M., Peck, A., McCord, Z., Naaktgeboren, A., Gianfortoni, P., Gonzalez-Rivero, M., Hatton, R.L., &amp; Choset, H. (2007). Design of a modular snake robot. 2007 IEEE/RSJ International Conference on Intelligent Robots and Systems, 2609-2614.

[9] Biorobotics Lab Carnegie Mellon University, Modular Snake Robots, 2013, http://biorobotics.ri.cmu.edu/projects/modsnake/

[10] Alessandro Crespi, Auke Jan Ijspeert, AmphiBot II: An Amphibious Snake Robot that Crawls and Swims using a Central Pattern Generator, Proceedings of the 9th International Conference on Climbing and Walking Robots Brussels, Belgium - September 2006

[11] Rollinson, D., Bilgen, Y., Brown, B., Enner, F., Ford, S., Layton, C., Rembisz, J., Schwerin, M., Willig, A., Velagapudi, P., &amp; Choset, H. (2014). Design and architecture of a series elastic snake robot. 2014 IEEE/RSJ International Conference on Intelligent Robots and Systems, 4630-4636.

[12] &quot;Pololu - 150:1 Micro Metal Gearmotor MP 6V,&quot; _Pololu Robotics &amp; Electronics_. [Online]. Available: https://www.pololu.com/product/2368/specs. [Accessed: 07-Feb-2021].

[13] &quot;AKZYTUE 3.7V 400mAh 802525 Lipo Battery Rechargeable Lithium Polymer ion Battery Pack with JST Connector,&quot; _Amazon.com_. [Online]. Available: https://www.amazon.com/AKZYTUE-Battery-Rechargeable-Lithium-Connector/dp/B07TVDNQNS/ref=sr\_1\_2?dchild=1&amp;keywords=3.7V+400mAh+Lithium+Polymer&amp;qid=1612665237&amp;s=hpc&amp;sr=1-2. [Accessed: 06-Feb-2021].