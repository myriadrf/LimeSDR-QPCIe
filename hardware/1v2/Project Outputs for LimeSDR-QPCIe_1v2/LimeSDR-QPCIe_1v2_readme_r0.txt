Board Description
-----------------

board designation           : LimeSDR-QPCIe
board version		        : v1.2
board type                  : Lead Free
board size                  : 208.8 mm x 129.5 mm
board thickness             : 1.6 mm +/- 10 %
board material              : IT-180A
number of layers            : 14 (12 inner)

Stackup:
	Via nr.		Via type		Drill diameter			Ring diameter		Additiona specs./Info
		#1		Throughole			0.2 mm					0.4 mm
		#2		Throughole			0.2 mm					0.35 mm			In pad. Resin filled with metal cap (IC1, IC4)
		 

Top layer copper foil thickness: 17.5 um
Dielectric thickness between Top layer and 2nd layer: 173 um (6.8 mils)
Dielectric between Top layer and 2nd layer relative permittivity (Er): 4.2

Bottom layer copper foil thickness: 17.5 um
Dielectric thickness between L13 layer and Bottom layer: 173 um (6.8 mils)
Dielectric between L13 and Bottom layer relative permittivity (Er): 4.2

Internal layer copper foil thickness: 35um

minimum finished hole size  :  200 um
minimum spacing             :  100 um
minimum track width         :  100 um

drill diameters             : finished hole

plating finish (both sides) : immersion gold
                              0.05-0.10 um of gold over
                              2.50-5.00 um of nickel

plating finish PCI fingers (both sides) : immersion gold
                              30 micro inches of gold over
                              50 micro inches of nickel
							  
PCB edges below PCI express fingers must be chamfered. Chamfer height 1.4 mm, angle 20 (+/-5) degrees. Edges must be free of cutting burrs. Details given on PCB.
							  
Top silkscreen              : Required
Bottom silkscreen           : Required

Drill files
-----------------
   - LimeSDR-QPCIe_1v2.DRR -> Drill report detailing the tool assignments, hole sizes, hole count and tool travel. 
   
   - Throughole vias are covered in the following files:
   								File Name																	Start Layer						Stop Layer
						LimeSDR-QPCIe_1v2-RoundHoles.TXT															Top									Bottom
   - Slotholes are covered in the following files:
						LimeSDR-QPCIe_1v2-SlotHoles.TXT															Top									Bottom	
						
	- IMPORTANT! Hole diameters are final manufactured diameters INCLUDING HOLE METALIZATION.
	
Gerber files
---------------

			File Name					Layer/Comment
		LimeSDR-QPCIe_1v2.GTL				Top (RF/GND)
		LimeSDR-QPCIe_1v2.G1				L2  (GND)
		LimeSDR-QPCIe_1v2.G2				L3  (PWR/Signal/GND)
		LimeSDR-QPCIe_1v2.G3				L4  (PWR/GND)
		LimeSDR-QPCIe_1v2.G4				L5  (GND)
		LimeSDR-QPCIe_1v2.G5				L6  (Signal/PWR/GND)
		LimeSDR-QPCIe_1v2.G6				L7  (GND)	
		LimeSDR-QPCIe_1v2.G7				L8  (Signal/PWR/GND)
		LimeSDR-QPCIe_1v2.G8				L9  ((PWR/Signal/GND))
		LimeSDR-QPCIe_1v2.G9				L10 (Signal)
		LimeSDR-QPCIe_1v2.G10				L11 (GND)
		LimeSDR-QPCIe_1v2.G11				L12 (CLK/Signal)
		LimeSDR-QPCIe_1v2.G12				L13 (GND)
		LimeSDR-QPCIe_1v2.GBL				Bottom (Signal/PWR/GND)

		 
		LimeSDR-QPCIe_1v2.GPB				Bottom Pad Master
		LimeSDR-QPCIe_1v2.GPT				Top Pad Master

		LimeSDR-QPCIe_1v2.GTO				Top Overlay
		LimeSDR-QPCIe_1v2.GTP				Top Paste
		LimeSDR-QPCIe_1v2.GTS				Top Solder

 
		LimeSDR-QPCIe_1v2.GBS				Bottom Solder
		LimeSDR-QPCIe_1v2.GBP				Bottom Paste
		LimeSDR-QPCIe_1v2.GBO				Bottom Overlay


		LimeSDR-QPCIe_1v2.GM1				Mechanical 1 (Board Cutout)


		LimeSDR-QPCIe_1v2.GM14				ASM BOT (Assembly bottom)
		LimeSDR-QPCIe_1v2.GM15				ASM TOP (Assembly top)
		
  
Important Notes
---------------
0.35mm ring and 0.2mm drill via-in-pads must be resin filled with metal cap (IC1 and IC4).

IC1 and IC4 thermal pad vias must be resin filled with metal cap.

IC1 and IC4 thermal pad vias with 0.5mm ring and 0.2mm drill must be left open (NO resin fill with metal cap). 4 vias in total, marked with note in mechanical 1 (*.GM1) gerber file.

DRCs must be run on Gerber files before building boards.

All through hole vias may be plated shut.

Solder mask : dark blue (LP-4G/B-50), both sides, halogen free, glossy finish (NOT matte).

Silkscreen : white epoxy ink, halogen free, both sides. No silkscreen on pads.

Electrical test : 100 % netlist.

Boards are to be individually bagged.

Design software used : Altium Designer 16.1.11 (build 255) under VGTU commercial license 

Controlled Impedance
--------------------

  * 100 Ohm coplanar differential pair without ground (Top layer) characteristics:
	Top layer copper foil thickness: 17.5 um
	Track width = 0.2 mm (7.874 mils)
	Track spacing = 0.1 mm (3.937 mils)
	Track width/spacing ratio = 2
	Dielectric thickness from top to L2 = 173um (6.8 mils)
	Dielectric between Top layer and 2nd layer relative permittivity (Er): 4.2
        
	Approximate coupled microstrip line impedance = 100.7 Ohms (+/- 10% tolerance)
	
  * 50 Ohm coplanar waveguide without ground (Top layer) characteristics:
	Top layer copper foil thickness: 17.5 um
	Track width = 0.309 mm (12.165 mils)
	Dielectric thickness from Top to L2 = 173um (6.8 mils)
	Dielectric between Top layer and 2nd layer relative permittivity (Er): 4.2
        
	Approximate microstrip line impedance = 49.99 Ohms (+/- 10% tolerance)

  * 50 Ohm coplanar waveguide with GND (Bottom layer) characteristics:
	Bottom layer copper foil thickness: 17.5 um
	Track width = 0.254 mm (10 mils)
	Distance to GND: 0.1 mm (3.937 mils)
	Dielectric thickness from Bottom to L13 = 173um (6.8 mils)
	Dielectric between Bottom layer and L13 relative permittivity (Er): 4.2
        
	Approximate microstrip line impedance = 49.99 Ohms (+/- 10% tolerance)
	
  * 85 Ohm coupled microstrip line (Top layer, PCI traces) characteristics:
    Top layer copper foil thickness: 17.5 um
	Track width = 0.25 mm (9.84 mils)
	Track spacing = 0.1 mm (3.93 mils)
	Track width/spacing ratio = 2.5
	Dielectric thickness from Top to 2nd layer = 173um (6.8 mils)
	Dielectric between Top layer and 2nd layer relative permittivity (Er): 4.2
	
	Approximate coupled microstrip line impedance = 85 Ohms (+/- 10% tolerance)	
	
  * 85 Ohm coupled microstrip line (Bottom layer, PCI traces) characteristics:
    Bottom layer copper foil thickness: 17.5 um
	Track width = 0.25 mm (9.84 mils)
	Track spacing = 0.1 mm (3.93 mils)
	Track width/spacing ratio = 2.5
	Dielectric thickness from L13 to Bottom layer = 173um (6.8 mils)
	Dielectric between L13 layer and Bottom layer relative permittivity (Er): 4.2
	
	Approximate coupled microstrip line impedance = 85 Ohms (+/- 10% tolerance)
	
  * 90 Ohm coupled microstrip line (Top layer, without GND) characteristics:
	Top layer copper foil thickness: 17.5 um
	Track width = 0.2 mm (6.8 mils)
	Track spacing = 0.1 mm (3.93 mils)
	Track width/spacing ratio = 2
	Dielectric thickness from Top to 2nd layer = 173um (6.8 mils)
	Dielectric between Top layer and 2nd layer relative permittivity (Er): 4.2
        
	Approximate coupled microstrip line impedance = 90.5 Ohms (+/- 10% tolerance)   