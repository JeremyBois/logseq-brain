file:: [PCBDesignTutorialRevA_1689442289559_0.pdf](../assets/PCBDesignTutorialRevA_1689442289559_0.pdf)
file-path:: ../assets/PCBDesignTutorialRevA_1689442289559_0.pdf
alias:: PCB Design & Layout Tutorial
type:: [[Book]]
author:: #[[Dave Jones]]
tags:: PCB, Électronique, Formation
link:: [Front page](https://alternatezone.com/electronics/pcbdesign.htm)
[[Jul 15th, 2023]]
***

- ![Viewer](../assets/PCBDesignTutorialRevA_1689442289559_0.pdf) | [PDF](../assets/PCBDesignTutorialRevA_1689442289559_0.pdf)
  ***
-
- Make sure the finer grid you choose is a nice even division of your standard 100 thou. This means 50, 25, 20, 10, or 5 thou. Don’t use anything else, you’ll regret it.
  ls-type:: annotation
  hl-page:: 5
  hl-color:: yellow
  id:: 64b2d834-69e0-4682-9d93-d1eb16699c57
	- 100 thou (0.1 inch) = 2.54mm, and 200 thou (0.2 inch) = 5.08mm
	  ls-type:: annotation
	  hl-page:: 5
	  hl-color:: yellow
	  id:: 64b2d998-5c3f-4d41-823a-0f6669184866
	- Unité souvent utilisée pour la grille d'aimantage
- The second major rule of PCB design, and the one most often missed by beginners, is to lay out your board on a fixed grid. This is called a “snap grid”, as your cursor, components and tracks will “snap” into fixed grid positions. Not just any size grid mind you, but a fairly coarse one.
  ls-type:: annotation
  hl-page:: 5
  hl-color:: yellow
  id:: 64b2d820-b2ed-4d42-84dd-b44d27c30774
- As a general rule though, the bigger the track width, the better. Bigger tracks have lower DC resistance, lower inductance, can be easier and cheaper for the manufacturer to etch, and are easier to inspect and rework.
  ls-type:: annotation
  hl-page:: 6
  hl-color:: yellow
  id:: 64b2dd8e-2806-4903-8cd2-0213113ab233
- As a start, you may like to use say 25 thou for signal tracks, 50 thou for power and ground tracks, and 10-15 thou for going between IC and component pads.
  ls-type:: annotation
  hl-page:: 6
  hl-color:: yellow
  id:: 64b2de17-555d-4193-9c53-c026e132e1ea
	- In practice, your track width will be dictated by the current flowing through it, and the maximum temperature rise of the track you are willing to tolerate. Remember that every track will have a certain amount of resistance, so the track will dissipate heat just like a resistor. The wider the track the lower the resistance
	  ls-type:: annotation
	  hl-page:: 6
	  hl-color:: yellow
	  id:: 64b2df03-16c0-4ab4-ae22-d1f07c969016
- As a simple rule of thumb, the pad should be at least 1.8 times the diameter of the hole, or at least 0.5mm larger. This is to allow for alignment tolerances on the drill and the artwork on top and bottom layers. This ratio gets more important the smaller the pad and hole become, and is particularly relevant to vias.
  ls-type:: annotation
  hl-page:: 7
  hl-color:: yellow
  id:: 64b2dfd8-f4fa-4ee9-9997-1f571a996534
	- Pin 1 of the chip sould always be a different pad shape, usually rectangular, and with the same dimensions as the other pins.
	  ls-type:: annotation
	  hl-page:: 7
	  hl-color:: yellow
	  id:: 64b2e013-c119-41fe-bac0-5249c7d4c628
	- Octagonal pads are seldom used, and should generally be avoided. As a general rule, use circular or oval pads unless you need to use rectangular.
	  ls-type:: annotation
	  hl-page:: 8
	  hl-color:: yellow
	  id:: 64b2e027-da23-4f65-9128-c43091024720