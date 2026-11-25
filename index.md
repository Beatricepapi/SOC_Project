---
layout: home
title: FPGA VGA Driver Project
tags: fpga vga verilog
categories: demo
---

Welcome to my FPGA VGA Driver Project! In this project, I will be using Verilog and Vivado 2025.1 to display graphics on a VGA monitor using the Basys3 FPGA board. I will first test the example provided by the lecturer and then create my own design.

## Weekly Progress

### Week 1 – Project Setup and VGA Colour Stripes

This week, I started my FPGA VGA project in Vivado 2025.1. First, I created a new project and selected the Basys3 FPGA device. I added the Verilog files provided by the lecturer, including VGATop, VGASync and VGAColourStripes.

I also configured the Clocking Wizard to generate a 25 MHz clock from the 100 MHz input clock.

After setting up the project, I added the testbench and ran the Behavioral Simulation. I looked at the waveforms and observed the clock, synchronization signals, row and column positions, and RGB colour outputs.

Next, I ran synthesis and implementation. I checked the timing summary, which showed no failing endpoints. I then tested the original design on the Basys3 board and displayed the colour stripes on the VGA monitor.

During this week, I learned more about how the VGA signals work and how Verilog can be used to display different colours on a screen.

### VGA Colour Stripes Demonstration

<img width="450" alt="Colour Stripes displayed on VGA monitor" src="https://github.com/user-attachments/assets/9cb5cc04-3e07-4abe-b90d-b89c19be4825">

*Figure 1: Original VGA Colour Stripes design displayed on the monitor using the Basys3 FPGA board.*



<h3>Vivado Project Summary</h3>

<img width="450" alt="Vivado Project Summary" src="https://github.com/user-attachments/assets/dd350128-546d-4699-bd14-1e07bd0900a3">

<p><i>Figure 2: Vivado project setup and design sources.</i></p>

<h3>Behavioral Simulation</h3>

<img width="450" alt="Behavioral Simulation" src="https://github.com/user-attachments/assets/cb2d204a-0d27-4d60-b182-cf83f10b3423">

<p><i>Figure 3: Behavioral simulation showing the VGA signals.</i></p>

<h3>Implementation Results</h3>

<img width="450" alt="Implementation Results" src="https://github.com/user-attachments/assets/682726cf-89e4-47b1-b598-8ca163164127">

<p><i>Figure 4: FPGA implementation and timing results.</i></p>


### Next Week

Next week, I plan to start modifying the original design to display my own image. I have chosen a simple Kawaii Kitty design with a pink background and a white cat face.

### Week 2 – Planning My Own VGA Design

This week, I started planning my own VGA image after completing the original Colour Stripes example.

I decided to create a simple Kawaii Kitty with a pink background and a white cat face. I chose this design because I wanted something different from the original example, but still simple enough to create using Verilog.

My design will include two cat ears, two black eyes, a pink nose and a small mouth. I decided not to add too many details because I want to focus on understanding how the different shapes are displayed.

I plan to use the row and column coordinates from the VGA design to decide where each shape should appear on the 640 x 480 screen.

The next step is to modify the original Colour Stripes module and test the new image in Vivado.


<h3>Step 1 - Pink Background and White Face</h3>

<p>
First, I changed the RGB values to make the background
pink. I then used row and column conditions to draw
a white rectangle in the centre of the screen.
</p>

<img width="450" alt="Pink background and white face" src="https://github.com/user-attachments/assets/b4c68bca-b44e-4b0a-86e1-3ddd73fd3020">

<p><i>Figure 5: First stage of my Kawaii Kitty design showing the pink background and white rectangle.</i></p>

<h3>Step 2 - Adding the Cat Ears</h3>

<p>
Next, I added two white ears using more if statements
with row and column coordinates. I generated a new
bitstream and tested the updated design on the
Basys3 FPGA board.
</p>

<img width="450" alt="White cat face with ears" src="https://github.com/user-attachments/assets/1e5887ff-d2e5-43a9-992a-14c88a88cc44">

<p><i>Figure 6: Second stage of my Kawaii Kitty design with two ears.</i></p>

### What I Learned This Week

This week, I learned how to change the original VGA design to display my own shapes instead of colour stripes. I used the row and column values to control where the shapes appeared on the screen.

I found it easier to build the design one step at a time. First, I tested the background and white rectangle, and then I added the ears. Testing each stage on the Basys3 board helped me check that my changes were working.

Next week, I plan to add the eyes, nose and mouth to complete the cat's face.


### Week 3 – Developing My Kawaii Kitty Design

This week, I continued working on my Kawaii Kitty VGA design in Vivado 2025.1.

During Week 2, I created the pink background, white rectangular face and two ears. My next task was to add the facial features to make the image look more like a cat.

### Adding the Eyes, Nose and Mouth

I modified `VGAColourStripes.v` by adding more `if` statements using the `row` and `col` coordinates.

First, I added two dark square eyes. I then added a small pink rectangle for the nose and a short dark line for the mouth.

I kept the shapes simple because I wanted to use the same method that I had already used for the background, face and ears.

After updating the code, I ran the Behavioral Simulation in Vivado and generated a new bitstream. I programmed the Basys3 FPGA board and tested the updated design on the VGA monitor.

The cat's face displayed correctly with the eyes, nose and mouth in the positions I wanted.

<img width="450" alt="Kawaii Kitty with eyes nose and mouth" src="https://github.com/user-attachments/assets/e611addf-145d-4c73-88c5-5115b12d91cc">

*Figure 7: Kawaii Kitty design displayed on the VGA monitor after adding the eyes, nose and mouth.*

### Improving the Shape of the Cat

After adding the eyes, nose and mouth, I wanted to improve the shape of the cat's head because it still looked quite rectangular.

I changed the conditions for the white face in `VGAColourStripes.v`. Instead of using one large rectangle, I combined smaller rectangular areas with different row and column values.

<img width="450" alt="Kawaii Kitty with rounded pixel edges" src="https://github.com/user-attachments/assets/ac9e25a6-cd8b-4b39-8196-70a5778e9b2a">

*Figure 8: Four overlapping rectangles used to create a rounded pixel-art shape.*

This created small steps around the edges and bottom of the face, making it look more rounded in a pixel-art style.

I kept the eyes, nose, mouth and ears the same.

After modifying the code, I generated a new bitstream and programmed the Basys3 board again. The updated shape displayed correctly on the VGA monitor.

<img width="450" alt="Kawaii Kitty with rounded pixel edges" src="https://github.com/user-attachments/assets/7fffbc9f-cdd7-41ff-a9ed-746b8d4ef039">

*Figure 9: Updated Kawaii Kitty design with stepped edges to create a more rounded face.*


### Improving the Cat's Ears

After making the cat's face more rounded, I decided to improve the ears because they still looked too rectangular.

I modified the ear conditions in `VGAColourStripes.v` by using smaller rectangles with different row and column values. I made each section narrower towards the top to create a more pointed shape.

I used the same method for both ears so they would look similar.

After changing the code, I generated a new bitstream and programmed the Basys3 board again. The updated ears displayed correctly on the VGA monitor, and I was happy with the new shape.

<img width="450" alt="Kawaii Kitty with pixel-style ears" src="https://github.com/user-attachments/assets/d90902c7-3a57-4a5a-845a-3972a640e7a2">

*Figure 10: Kawaii Kitty displayed on the VGA monitor after improving the ears using pixel-style shapes.*

### What I learned this week

This week, I completed the main parts of my Kawaii Kitty design. I added the eyes, nose and mouth, and then improved the shape of the face and ears.

At first, the cat looked quite rectangular, but by combining smaller rectangular areas, I was able to make the edges look more rounded and the ears more pointed.

I learned that I can create different shapes using simple `if` statements and pixel coordinates without needing complicated Verilog code.

I also tested the changes on the Basys3 FPGA board to make sure that each version displayed correctly on the VGA monitor.

I am happy with how my design has developed compared with the original Colour Stripes example.

### My plan for next week

For Week 4, I plan to make a few final improvements to my Kawaii Kitty design.

First, I would like to change the nose and the mouth using pixel coordinates. Adding 2 pink cheeks and a bit of pink inside the ears too.

After that, I plan to use one of the switches on the Basys3 board to make the cat blink. When the switch is off, the eyes will remain open, and when the switch is on, the eyes will change into small horizontal lines to make them look closed.

To do this, I will need to modify the Verilog code and connect the switch input to the graphics module.

I will then run Behavioral Simulation, synthesis and implementation before testing the updated design on the VGA monitor.

My goal is to finish with a simple Kawaii Kitty that has a few extra details and can blink using a physical switch on the FPGA board.


### Week 4 - Testing My Final Static Kawaii Kitty Design

I added pink sections inside the ears, two pink cheeks,
dark brown square eyes, a small pink nose and a pixel-style
mouth.

I continued using `row` and `col` coordinates with `if`
statements to control the positions and colours of the
different shapes on the 640 x 480 VGA display.

Once I completed the static design, I generated a new
bitstream and programmed the Basys3 FPGA board.

The updated Kawaii Kitty appeared on the VGA monitor
with the pink background, white face and all the
facial details in the correct positions.

<img width="450" alt="Final static Kawaii Kitty displayed on VGA monitor" src="https://github.com/user-attachments/assets/0b844dcf-46fd-4939-b158-a52e9bd68cfc">

*Figure 11: Completed static Kawaii Kitty design displayed on the VGA monitor using the Basys3 FPGA board.*

I was happy to see the complete image displayed on the
monitor because it showed how much my design had
improved since the original Colour Stripes example.

The next step is to add the blinking animation to make
the cat more interactive.


### Testing the Blinking Animation on the Basys3 Board

After completing the static Kawaii Kitty design, my final task was to make the cat blink automatically.

First, I renamed my original `VGAColourStripes.v` file to `VGAKawaiiKitty.v` because the project was no longer displaying colour stripes. In this file, I added a counter that uses the 25 MHz clock generated by the Clocking Wizard. The counter increases with each clock cycle and controls when the cat's eyes open and close.

When the eyes are open, they appear as two dark brown squares. When the eyes close, they change into two thin horizontal lines. This allows the cat to blink automatically approximately every three seconds.

I also updated `VGATop.v` by changing the module name from `ColourStripes` to `KawaiiKitty` and renaming the instance to `u_kawaii_kitty`. I kept the original clock, reset, row, column and RGB connections because they were already working correctly.

I checked `VGASync.v` to make sure the VGA timing and the row and column coordinates were correct. I kept the original VGA synchronization logic because the display was already working.

I also updated `Testbench.v` by replacing `ColourStripes` with `KawaiiKitty` so that the testbench would reference my renamed graphics module.

After updating the files, I generated a new bitstream and programmed the Basys3 FPGA board to test the design on the VGA monitor.

The blinking animation worked successfully. The cat's eyes changed from dark brown squares to small horizontal lines before opening again, repeating approximately every three seconds without using a physical switch.

I was happy with the final result because I managed to add an animation while keeping the original appearance of my Kawaii Kitty design.

<img width="450" alt="Kawaii Kitty with closed eyes on VGA monitor" src="https://github.com/user-attachments/assets/d0e030c9-9a9e-4ddb-bd8a-a74218f76d48">

*Figure 12: Final Kawaii Kitty design showing the eyes closed during the blinking animation on the VGA monitor.*

### Final Reflection

Looking back at the four weeks of this project, I can see how much my understanding of Verilog and FPGA design has improved. At the beginning, I was working with the Colour Stripes example provided by the lecturer, and I was mainly trying to understand how the VGA signals worked. By the end, I had developed my own Kawaii Kitty design with different shapes, colours and a blinking animation.

One of the most important things I learned was how the FPGA uses the row and col coordinates to decide what appears on the screen. For example, when I wanted to draw the cat's face, I used conditions such as col >= 170 && col < 470 to define the horizontal boundaries of a rectangular area. I combined these conditions with the row values to control the height and position of each shape.

At first, I used one large white rectangle for the face, but I wasn't happy with how square it looked. I experimented with overlapping rectangles of different sizes to make the edges look more rounded. This helped me understand that I didn't need to create actual curves. By combining several rectangular regions using the || (OR) operator, I could create stepped edges that gave the cat a pixel-art appearance. I used a similar method for the ears, making the sections narrower towards the top.

Another important part was understanding how RGB colours work. For example, I used 12'hFFF to display white and 12'hFAC for the pink background. I learned that the Basys3 VGA output uses 4 bits for each colour channel, allowing me to control the red, green and blue values separately.

The biggest challenge in the final week was adding the blinking animation. Until that point, my design was static, meaning the image stayed the same on the screen. To make the eyes blink, I added a counter inside VGAKawaiiKitty.v that increases on every rising edge of the 25 MHz clock. I used the counter value to decide when the eyes should appear as dark brown squares and when they should change into thin horizontal lines.

For example, I used the condition blink_counter >= 27'd70833333 to control when the eyes close. Since the clock runs at 25 million cycles per second and the counter resets after 75 million cycles, the complete blinking cycle takes approximately three seconds.

I also learned more about how the different Verilog files work together. VGASync.v generates the VGA timing and pixel coordinates, VGATop.v connects the different modules, and VGAKawaiiKitty.v controls the colours and appearance of the cat. Understanding these connections helped me see why changing a module name also required updating its reference in the top-level design and testbench.

I encountered some problems during the project, including syntax errors and difficulties running Vivado simulation. These experiences showed me the importance of checking the error messages, making small changes at a time, and understanding which part of the design could be causing a problem.

My favourite part was seeing the cat displayed on the real VGA monitor, especially when the blinking animation worked. It was satisfying to see that the coordinate conditions and counter I had been working with in Verilog could produce a visible result on the FPGA board.

Overall, this project helped me understand that FPGA graphics are not just about drawing an image. They involve timing, digital logic, clock signals, coordinate comparisons and hardware implementation. I am happy with the way my Kawaii Kitty developed from the original Colour Stripes example into my own animated VGA design.

## **Template VGA Design**

### Project Set-Up

I started by creating a new project in Vivado 2025.1.
I selected the Basys3 FPGA device (xc7a35tcpg236-1)
and added the Verilog files provided by the lecturer.

I also added the Basys3 constraints file and configured
the Clocking Wizard to generate a 25 MHz clock from
the 100 MHz input clock.

### Template Code

The original design uses three main Verilog modules:

- VGATop connects the different modules together.
- VGASync controls the VGA timing and synchronization.
- ColourStripes controls the colours displayed on the screen.

The design displays eight vertical colour stripes
on a 640 x 480 VGA monitor.

### Simulation

I added the testbench provided by the lecturer and
ran the Behavioral Simulation in Vivado.

I observed signals such as clk, hsync, vsync,
row, col and the RGB outputs.

This helped me understand how the VGA timing
and colour signals work.

### Synthesis and Implementation

After simulation, I ran synthesis and implementation
in Vivado.

I checked the implementation results and timing summary.
The timing report showed no failing endpoints.

### Demonstration

I generated the bitstream and programmed the Basys3
FPGA board.

I connected the board to a VGA monitor and successfully
displayed the original eight colour stripes.

This confirmed that the original VGA design was working
on the FPGA board.

## **My VGA Design Edit**
Introduce your own design idea. Consider how complex/achievabble this might be or otherwise. Reference any research you do online (use hyperlinks).
### **Code Adaptation**
Briefly show how you changed the template code to display a different image. Demonstrate your understanding. Guideline: 1-2 short paragraphs.
### **Simulation**
Show how you simulated your own design. Are there any things to note? Demonstrate your understanding. Add a screenshot. Guideline: 1-2 short paragraphs.
### **Synthesis**
Describe the synthesis & implementation outputs for your design, are there any differences to that of the original design? Guideline 1-2 short paragraphs.
### **Demonstration**
If you get your own design working on the Basys3 board, take a picture! Guideline: 1-2 sentences.

## **More Markdown Basics**
This is a paragraph. Add an empty line to start a new paragraph.

Font can be emphasised as *Italic* or **Bold**.

Code can be highlighted by using `backticks`.

Hyperlinks look like this: [GitHub Help](https://help.github.com/).

A bullet list can be rendered as follows:
- vectors
- algorithms
- iterators

Images can be added by uploading them to the repository in a /docs/assets/images folder, and then rendering using HTML via githubusercontent.com as shown in the example below.

<img src="https://raw.githubusercontent.com/melgineer/fpga-vga-verilog/main/docs/assets/images/VGAPrjSrcs.png">
