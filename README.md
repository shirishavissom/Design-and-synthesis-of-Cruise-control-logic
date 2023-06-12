# Design-and-synthesis-of-Cruise-control-logic
Synthesized the RTL Design with a specific library for 180nm technology to build gate-level netlist, performed Pre-layout STA and also designed the SDC constraint. Generated SPEF Files to determine the Parasitic RC of the nets for crosstalk and signoff STA analysis.

Synthesized the RTL Design with a specific library for 180nm technology to build gate-level netlist, performed Pre-layout
STA and also designed the SDC constraint. Performed the entire PD flow and analyzed the routing topology to reduce
congestion. Generated SPEF Files to determine the Parasitic RC of the nets for crosstalk and signoff STA analysis.

During my learning process, I gained familiarity with the fundamentals of synthesis using Design Vision by working on a straightforward example known as the "cruise control design." Following the synthesis stage, I conducted a pre-layout static timing analysis on the synthesized design. This involved defining constraints for the design and verifying the timing of all the paths within the design.

Next, I utilized the synthesized Verilog netlist generated for the cruise control logic to proceed with the "Place and Route" step. This step involves placing the circuit components and routing the interconnections on a die or chip, effectively mapping the design onto a physical layout. This process prepares the design for further steps such as physical verification, layout optimization, and eventually fabrication.

![Symbol view](https://user-images.githubusercontent.com/112213946/227419678-2adab86a-1803-4e88-86d6-fe5ee5883759.png)

In the initial phase of our project, we embarked on Logic Synthesis, which involved synthesizing the logic utilizing a specific library tailored for the 180nm technology. To ensure accurate synthesis, we accessed the Synopsys database format (db) file for the standard 180nm technology from the provided Google drive. The synthesis process was carried out in accordance with the characteristics and specifications outlined in this library file, encompassing optimization parameters such as power, timing, and area.

Our design entailed the creation of a Verilog model comprising a Finite State Machine (FSM). Additionally, we developed a corresponding test bench for simulation purposes. Following the completion of the design, we initiated the synthesis phase. The target library employed in this step represented the actual library utilized for optimization during the synthesis process. Furthermore, we included the link library, which encompassed the target library as well as any additional libraries required for macros present in the design.

To continue, we placed the Verilog behavioral code of the Cruise Control Logic in the designated ~/synthesis/verilog folder. We then repeated the aforementioned procedure to optimize the logic and generate the final synthesized Verilog netlist, incorporating the desired characteristics and constraints outlined by the target library.
We analyse the cruisecontrol.v file. Set attributes as an logical hierarchy window

Generated Area and constraints
![area_2](https://user-images.githubusercontent.com/112213946/227419879-129f7274-6e1f-4cd3-888e-3e14ac82b856.png)

created design constraints
![firstop](https://user-images.githubusercontent.com/112213946/227419968-0e517f4e-5725-4be5-9230-9b0935f0352a.png)

Synthesized the verilog netlist
![image](https://user-images.githubusercontent.com/112213946/227420068-e025d51b-b299-482a-87f2-39c32abd470e.png)
![image](https://user-images.githubusercontent.com/112213946/227420146-7b8f8e95-b5b4-495e-bff2-754b43095016.png)
![image](https://user-images.githubusercontent.com/112213946/227420115-51754584-0107-402d-ae2c-f565a74aca76.png)

Register count
![image](https://user-images.githubusercontent.com/112213946/227420417-31a0d00e-ccd6-48ba-9732-19c10e6f4d64.png)

In Part B, we delve into Static Timing Analysis (STA), which is a crucial step in assessing the timing requirements of the circuit. Timing analysis can be performed at various design stages, such as pre-layout using wire-load models or post-layout with actual wires.

To conduct the timing analysis, we utilize PrimeTime® (PT), the prominent static timing analysis (STA) tool developed by Synopsys. PT is widely recognized and employed within the industry due to its high accuracy and reliability. While Design Compiler also includes its own timing engine, it does not offer the same level of precision as Primetime. Furthermore, Primetime has the capability to account for signal integrity effects, such as coupling noise caused by cross talk, and can analyze intricate interconnect structures within the design.

By leveraging the power of Primetime, we can ensure comprehensive timing analysis that takes into account both the inherent timing constraints and potential signal integrity issues, resulting in a more accurate assessment of the circuit's timing requirements.
Max path: 
![image](https://user-images.githubusercontent.com/112213946/227420396-bb8cf002-d920-4383-bddf-e78835c6d2d1.png)
![image](https://user-images.githubusercontent.com/112213946/227420475-72b32d24-c2e8-4050-acd7-1e7bad297688.png)

Min path:
![image](https://user-images.githubusercontent.com/112213946/227420526-fba06148-fdae-451c-a6b5-eed7f03a7919.png)
![image](https://user-images.githubusercontent.com/112213946/227420531-0244e1e2-4536-4992-827c-c8ed2a51d20f.png)

Layout:
![Layout](https://user-images.githubusercontent.com/112213946/227420654-b2c80a81-1774-4caa-a524-f6fabf583075.png)





