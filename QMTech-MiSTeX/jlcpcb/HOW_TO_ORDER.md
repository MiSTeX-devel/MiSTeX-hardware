# How to order
These are the settings I used. You probably
can use cheaper options where I mentioned it,
but I have not tried those, so do that at your own risk.

1. Go to https://cart.jlcpcb.com/quote
2. Click `Add Gerber File`
3. Choose `production_files/GERBER-QMTech-MiSTeX.zip`
4. Material type: FR4-TG155 (optional, costs marginally more, less warping)
5. Surface finish: ENIG (optional, lead free HASL also might work)
6. Impedance control: Yes, JLC04161H-7628, press `Confirm`
7. Leave the rest at default (optionally use `Confirm production file`), activate the Assembly switch
8. Confirm parts placement: Yes (important, the import of those is not perfect and has to be corrected by an employee,
                                 so you need to check if the placements are good)
9. PCBA Qty: I recommend 5, because it only costs about 20% more and does not waste PCBs, but use 2 at your own discretion.
10. Make sure `Assemble top side`  is chosen
11. Click `Confirm`
12. A PCB viewer will come up, press 'Next'
13. Select `production_files/BOM-QMTech-MiSTeX.csv`  as BOM file and `production_files/CPL-QMTech-MiSTeX.csv` as CPL file
14. Press `Process BOM & CPL`
15. A list of parts should come up. Make sure they are all available and press `Next`
16. A window with the component placements comes up. Note that some connectors (USB-C, VGA and TOSLINK)
    can be out of place. Just leave them. A JLCPCB engineer will fix those, and then ask you for review
    after the order has been submitted (Confirm parts placement).
17. Press 'Save to Cart'
18. You can then Check out our cart and order the PCBs
