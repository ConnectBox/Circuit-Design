README.txt

This is a record of the various board layout attempts for the CM4 China format

HAT_CM4_020822.zip
  This is an almost complete layout without placement of the blue (battery active) LEDs,
  the red (battery reversed) LEDs, and the amber (status) LED. Also not placed is the
  memory chip (U5) used to indicate the version of the HAT board. These components are 
  shown at the periphery of the layout but not wired. This .zip file contains the entire 
  project as of 020822.

HAT_CM4_DRC_1.kicad_pcb
  This is just the pcb layout as of late evening 020822. I removed the non-placed components
  from the pcb layout (but not from the schematic) and ran the DRC (Design Rules Check) on
  the design. Then corrected errors. (Some errors I ignored... ex: interferring silk screens)
  but this layout is pretty good. Trace lengths and impedences are correct, for example.

CM4_HatBat_CHINA/181 (KiCad/Archive/HAT_CM4_181_021722.zip)
  This is the version submitted for board fab to JLCPCB on 2/18/22.
  NOTE: Properties of all components now up to date allowing a nice BOM to be created. Also note that   
   a listing of components PER SIDE is available as CM4_HatBat_CHINA/Gerber_181_021822/HAT_CM4-   
   top.pos and HAT_CM4-bottom.pos. Generated using Pcbnew -> Foe -> FabricateionOutputs -> Component 
   Placement (.pos) -> Separate files for front, back). (Will be very useful during fabrication!)