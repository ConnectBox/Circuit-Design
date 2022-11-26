README.txt

This is a record of the various board layout attempts for the CM4 China format

HAT_CM4_020822.zip
  (THIS FILE.) This is an almost complete layout without placement of the blue (battery active) LEDs,
  the red (battery reversed) LEDs, and the amber (status) LED. Also not placed is the
  memory chip (U5) used to indicate the version of the HAT board. These components are 
  shown at the periphery of the layout but not wired. This .zip file contains the entire 
  project as of 020822.

HAT_CM4_DRC_1.kicad_pcb
  This is just the pcb layout as of late evening 020822. I removed the non-placed components
  from the pcb layout (but not from the schematic) and ran the DRC (Design Rules Check) on
  the design. Then corrected errors. (Some errors I ignored... ex: interfering silk screens)
  but this layout is pretty good. Trace lengths and impedances are correct, for example.