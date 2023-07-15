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
- Before you even begin to lay out your PCB, you MUST have a complete and accurate schematic diagram. Many people jump straight into the PCB design with nothing more than the circuit in their head, or the schematic drawn on loose post-it notes with no pin numbers and no order. This just isn’t good enough, if you don’t have an accurate schematic then your PCB will most likely end up a mess, and take you twice as long as it should.
  ls-type:: annotation
  hl-page:: 4
  hl-color:: yellow
  id:: 64b2e0b5-8223-486e-9e65-3b4b07cd2687
  hl-stamp:: 1689444536158
- A “thou” is 1/1000th of an inch, and is universally used and recognised by PCB designers and manufacturers everywhere. So start practicing speaking in terms of “10 thou spacing” and “25 thou grid”, you’ll sound like a professional in no time!
  ls-type:: annotation
  hl-page:: 4
  hl-color:: red
  id:: 64b2e11e-d331-4874-8bd0-e726e30d6151
- This will do 99% of boards. Make sure the finer grid you choose is a nice even division of your standard 100 thou. This means 50, 25, 20, 10, or 5 thou. Don’t use anything else, you’ll regret it.
  ls-type:: annotation
  hl-page:: 5
  hl-color:: blue
  id:: 64b2dcc3-d5e3-4b00-aa19-276287d6eeb8
	- 100 thou (0.1 inch) = 2.54mm, and 200 thou (0.2 inch) = 5.08mm
	  ls-type:: annotation
	  hl-page:: 5
	  hl-color:: green
	  id:: 64b2d998-5c3f-4d41-823a-0f6669184866
	  hl-stamp:: 1689444657208
- The second major rule of PCB design, and the one most often missed by beginners, is to lay out your board on a fixed grid. This is called a “snap grid”, as your cursor, components and tracks will “snap” into fixed grid positions. Not just any size grid mind you, but a fairly coarse one.
  ls-type:: annotation
  hl-page:: 5
  hl-color:: blue
  id:: 64b2d820-b2ed-4d42-84dd-b44d27c30774
  hl-stamp:: 1689444504929
- As a general rule though, the bigger the track width, the better. Bigger tracks have lower DC resistance, lower inductance, can be easier and cheaper for the manufacturer to etch, and are easier to inspect and rework.
  ls-type:: annotation
  hl-page:: 6
  hl-color:: purple
  id:: 64b2dd8e-2806-4903-8cd2-0213113ab233
  hl-stamp:: 1689444667098
- As a start, you may like to use say 25 thou for signal tracks, 50 thou for power and ground tracks, and 10-15 thou for going between IC and component pads.
  ls-type:: annotation
  hl-page:: 6
  hl-color:: purple
  id:: 64b2de17-555d-4193-9c53-c026e132e1ea
  hl-stamp:: 1689444670186
	- In practice, your track width will be dictated by the current flowing through it, and the maximum temperature rise of the track you are willing to tolerate. Remember that every track will have a certain amount of resistance, so the track will dissipate heat just like a resistor. The wider the track the lower the resistance
	  ls-type:: annotation
	  hl-page:: 6
	  hl-color:: purple
	  id:: 64b2df03-16c0-4ab4-ae22-d1f07c969016
	  hl-stamp:: 1689444675444
		- As a rule of thumb, a 10degC temperature rise in your track is a nice safe limit to design around. 
		  ls-type:: annotation
		  hl-page:: 7
		  hl-color:: purple
		  id:: 64b2e14e-4d72-4d5b-8ab9-cf8542e4d8a6
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
- Holes in vias are usually a fair bit smaller than component pads, with 0.5-0.7mm being typical.
  ls-type:: annotation
  hl-page:: 8
  hl-color:: red
  id:: 64b2e06b-42e2-42f4-be1d-e06115e4ec00
  hl-stamp:: 1689444486809
- Polygon can either be “solid” fills of copper, or “hatched” copper tracks in a crisscross fashion. Solid fills are preferred, hatched fills are basically a thing of the past.
  ls-type:: annotation
  hl-page:: 8
  hl-color:: green
  id:: 64b2e18a-fcca-4255-9a5c-25b0430dc7f0
  hl-stamp:: 1689444748606
- Too tight a clearance between tracks and pads may lead to “hairline” shorts and other etching problems during the manufacturing process
  ls-type:: annotation
  hl-page:: 8
  hl-color:: blue
  id:: 64b2e1be-daf9-4f4d-9339-b398c55eaf6a
  hl-stamp:: 1689444801013
	- At least 15 thou is a good clearance limit for basic through hole designs, with 10 thou or 8 thou being used for more dense surface mount layouts. If you go below this, it’s a good idea to consult with your PCB manufacturer first.
	  ls-type:: annotation
	  hl-page:: 8
	  hl-color:: blue
	  id:: 64b2e1dd-401a-451c-ac4f-413baca3a4be
- An old saying is that PCB design is 90% placement and 10% routing
  ls-type:: annotation
  hl-page:: 9
  hl-color:: purple
  id:: 64b2e290-52b0-44d2-9ac5-3a98bf8e9c93
	- Set your snap grid, visible grid, and default track/pad sizes.
	  ls-type:: annotation
	  hl-page:: 9
	  hl-color:: purple
	  id:: 64b2e294-b33b-49d2-87b2-7ee39258a27b
	- Throw down all the components onto the board.
	  ls-type:: annotation
	  hl-page:: 9
	  hl-color:: purple
	  id:: 64b2e297-fd34-42d5-b9c4-03f28c8409f4
	- Divide and place your components into functional “building blocks” where possible.
	  ls-type:: annotation
	  hl-page:: 9
	  hl-color:: purple
	  id:: 64b2e29c-938b-45ea-83e7-9daa8ceb07b0
	- Identify layout critical tracks on your circuit and route them first.
	  ls-type:: annotation
	  hl-page:: 9
	  hl-color:: purple
	  id:: 64b2e2a0-1cfd-4c7c-b0ee-c386af2c1f09
	- Place and route each building block separately, off the board.
	  ls-type:: annotation
	  hl-page:: 9
	  hl-color:: purple
	  id:: 64b2e2a7-28f7-4216-a689-ee2bc84defe2
	- Move completed building blocks into position on your main board.
	  ls-type:: annotation
	  hl-page:: 9
	  hl-color:: purple
	  id:: 64b2e2b0-57b3-4f85-8e82-c9584f0b29a2
	- Route the remaining signal and power connections between blocks.
	  ls-type:: annotation
	  hl-page:: 9
	  hl-color:: purple
	  id:: 64b2e2b3-bd1a-4a8c-acc7-6fefcf3f9a80
	- Do a Design Rule Check.
	  ls-type:: annotation
	  hl-page:: 9
	  hl-color:: purple
	  id:: 64b2e2ba-f78e-45be-9c37-6d83c6d99fbc
	- We have already looked at the grids and track/pad sizes, these should be the first things that you set up before you start doing anything. No exceptions!
	  ls-type:: annotation
	  hl-page:: 10
	  hl-color:: purple
	  id:: 64b2e2f6-0684-44d4-9d11-279306d3ce6e
- The best way to start your layout is to get ALL of your components onto the screen first.
  ls-type:: annotation
  hl-page:: 10
  hl-color:: purple
  id:: 64b2e3b6-a116-4ff6-b800-5ac1140bcfd4
	- With all the components on screen, you should get a good indication of whether or not your parts will easily fit onto the size (and shape) of board that you require.
	  ls-type:: annotation
	  hl-page:: 10
	  hl-color:: purple
	  id:: 64b2e3be-4df0-4e01-a7ba-1e84ceb2b3b6
	- Now analyse your schematic and determine which parts of the design can be broken up into “building blocks”.
	  ls-type:: annotation
	  hl-page:: 10
	  hl-color:: purple
	  id:: 64b2e3c4-9ae4-4e65-9546-e3562cd082c5
		- Digital and analog just do not mix, and will need to be physically and electrically separated
		  ls-type:: annotation
		  hl-page:: 10
		  hl-color:: purple
		  id:: 64b2e432-abc0-4b09-8777-67424f54a53a
		- Another example is with high frequency and high current circuits, they do not mix with low frequency and low current sensitive circuits.
		  ls-type:: annotation
		  hl-page:: 10
		  hl-color:: purple
		  id:: 64b2e438-c50a-411a-b0ca-0d1f0da3588e
- Routing is the process of laying down tracks to connect components on your board. An electrical connection between two or more pads is known as a “net”.
  ls-type:: annotation
  hl-page:: 11
  hl-color:: yellow
  id:: 64b2e4a2-5865-4d81-ac79-2efa461070ba
  hl-stamp:: 1689445542169
	- Keep nets as short as possible. The longer your total track length, the greater it’s resistance, capacitance and inductance. All of which can be undesirable factors.
	  ls-type:: annotation
	  hl-page:: 11
	  hl-color:: yellow
	  id:: 64b2e4b1-3272-4f5a-8c7e-07e292496f4e
	- Tracks should only have angles of 45 degrees.
	  ls-type:: annotation
	  hl-page:: 11
	  hl-color:: yellow
	  id:: 64b2e4dd-a1b8-45d9-bee5-d574fcbb23a1
		- The reasons to avoid right angles are much simpler - it just doesn’t look good, and it may have some manufacturing implications.
		  ls-type:: annotation
		  hl-page:: 11
		  hl-color:: yellow
		  id:: 64b2e4e4-72e8-49b9-8a4f-9ce9145138ee
		- Forget nice rounded track corners,
		  ls-type:: annotation
		  hl-page:: 11
		  hl-color:: yellow
		  id:: 64b2e4ff-23df-4114-aea1-9c350d4fef0b
		- Always take your track to the center of the pad, don’t make your track and pad “just touch”
		  ls-type:: annotation
		  hl-page:: 11
		  hl-color:: yellow
		  id:: 64b2e52d-7ccc-4543-a0fc-6489ecb2f6a0
	- Keep power and ground tracks running in close proximity to each other if possible, don’t send them in opposite directions around the board. This lowers the loop inductance of your power system, and allows for effective bypassing.
	  ls-type:: annotation
	  hl-page:: 12
	  hl-color:: yellow
	  id:: 64b2e84f-10d7-4e27-9ba8-d5453244186e
	- Don’t leave any unconnected copper fills (also called “dead copper”), ground them or take them out.
	  ls-type:: annotation
	  hl-page:: 12
	  hl-color:: yellow
	  id:: 64b2e859-909f-43ab-8f99-1b12d85c8e8c