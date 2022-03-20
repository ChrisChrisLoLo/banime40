# Case STLs

## What files to use

You will need to print one Bottom piece (`Bottom PCB.stl`), one Plate (`Plate Final.stl`), and one top piece (`Top XXXXX.stl`).

Pick the top piece that will accomodate for the layout you want. I recommend looking at each file via Github to get a good sense what each top looks like, but I will provide a short summary here:
- `Top Grid.stl`
    - This top piece has no blockers on it. Good if you want every key to be available
- `Top HHKB 8u.stl`
    - HHKB stlye layout (the "control" key is blocked out). The middle of the bottom row is 8u long (2u blocked out)
- `Top HHKB 6u.stl`
    - Simiar to the above, but this time the "control" and "windows" key is blocked out. Good if you want a 36 key layout
- `Top WKL 6u.stl`
    - The "windows" key is blocked out. The middle gap in the bottom row is 6u wide
- `Top WKL 6,25.stl`
    - Same as the above, only the middle gap is 6.25u wide. This is to allow for 6.25u spacebars to be used.

## Bill of Materials

You will need the following materials outside of the printed/machined parts
- 12x M2 nuts (I used nylon ones)
- 6x M2 5mm-6mm M2 screws (I used metal ones)
- Super Glue
- An M2 jewlery screwdriver
  - Note that some screwdrivers might not be long enough to fit in the case. Try to use the screwdrivers with the long black heads.
- Foam Gaskets
  - These should partially work with KBD D65 gaskets, but what I used was a 1/16 inch thick adhesive neoprene foam sheet since it was what I had.
- Rubber Feet
  - Try to get ones that are 1.5-2mm tall. I found that anything taller makes the case height awkward.

## Recomended FDM settings
You will be able to print everything on an Ender 3 or bigger.
I recommend you printing with supports enabled. The supports are needed for the bottom of the case. You should also use gluestick or even brims to minimize parts warping. I recommend using a gluestick over using brims.

I used cubic infill (though you might be able to get away with less), and I do recommend setting the infill to atleast 50%. Anything lower and I find that you can get some internal "hollowness" noises.

A resolution of 0.16mm worked for me, I wouldn't go thicker than 0.20mm.

I mostly used stock Cura settings aside from this: most tolerances should be built into the model itself for FDM.

## Assembly
Once you have all the parts, you will want to do the following:
- Grab 2 M2 nuts and screw them onto the tip of the screw. Make sure that the nuts are flush with each other.
    - It should kind of look like a chicken leg, with the two nuts on one end and the screw head on the other 
- Apply superglue to the nuts, and push the nuts down into the hex holes found in the top of the case. be sure to push down.
- Leave the "chicken" leg there to dry for 5-10 minutes. Then unscrew the screw from the nuts.
- Repeat this for all remaining holes.
- If you have D65 gaskets, place them on the top and bottom of the case and you're done (you may need to trim the side gaskets though). If you're using a 1/16 inch thick sheet of adhesive foam, cut them out into thin strips, and place them into the top and bottom. There should be 2 layers of adhesive foam stacked on each other to form a gasket approximately 3mm in thickness.
- Pop in switches into the plate, place the plate onto the PCB, and place the plate and PCB on the bottomm piece.
- Place the top piece on and screw in.
- Now you're done!

## Note for SLA printing

The top and bottom piece _should_ be fine for SLA printing, though the switch holes in the plate file might be too loose for SLA. I increased the hole "diameter" by about 0.1mm, as I found that the plate was way too tight for FDM printing. Considering the tighter tolerances of SLA, this adjustment might become an overadjustment.

Experimentation will be required. In the future, if I find the time, I may want to create a new plate file that has the original hole diameters.

## Notes/improvements
 
Be aware that while I'm happy enough with the case enough to use without complaint, there are some details to note that you may be aware of before you assemble a case for yourself. Note that pointing these out, while detrimental to the appeal of my "product", should hopefully make it less frustrating for those who took the risk on trying to assemble one of these. With my current schedule, I cannot make any promise whatsoever to be able to fix these issues. If any of these are burning issues, I invite you to use the step file provided to make your own custom changes.

- Currently, the gaskets (in my case, 2 layers of 1/16 inch thick foam) are too thick, and push fairly firmly against the case. This can make assembly more difficult, as more force needs applied, which may affect the glued in nuts. This also may cause a small gap between the top and bottom piece

- The nut holes are a bit finnicky, as they may not be flush with the top of the case when glued in. This also contributes to a small gap between the top and bottom piece
    - I actively chose nuts over heat inserts as M2 heat inserts are relatively annoying to get, atleast in Canada. Nuts on the other hand, are plentiful and tend to come with M2 screw kits anyways.
    - I may make an outer shrould around the top piece to hide this gap down the road. Another potential solution would be to consider having "nut slots" or detents to hold the nuts in.