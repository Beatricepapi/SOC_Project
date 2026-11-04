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
>

<p><i>Figure 5: First stage of my Kawaii Kitty design showing the pink background and white rectangle.</i></p>

<h3>Step 2 - Adding the Cat Ears</h3>

<p>
Next, I added two white ears using more if statements
with row and column coordinates. I generated a new
bitstream and tested the updated design on the
Basys3 FPGA board.
</p>

<img width="450" alt="White cat face with ears" src="https://github.com/user-attachments/assets/1e5887ff-d2e5-43a9-992a-14c88a88cc44">
">

<p><i>Figure 6: Second stage of my Kawaii Kitty design with two ears.</i></p>

### What I Learned This Week

This week, I learned how to change the original VGA design to display my own shapes instead of colour stripes. I used the row and column values to control where the shapes appeared on the screen.

I found it easier to build the design one step at a time. First, I tested the background and white rectangle, and then I added the ears. Testing each stage on the Basys3 board helped me check that my changes were working.

Next week, I plan to add the eyes, nose and mouth to complete the cat's face.

### Week 3 – Completing My Kawaii Kitty Design

This week, I will continue working on my Kawaii Kitty VGA design in Vivado 2025.1.

Last week, I successfully displayed the pink background, white face and two ears on the VGA monitor using the Basys3 FPGA board.

My goal for this week is to complete the cat's face by adding two dark eyes, a small pink nose and a simple mouth.

I plan to continue modifying `VGAColourStripes.v` using `if` statements with the `row` and `col` coordinates. I will use the same method as before to control the position, size and colour of each shape.

Once the changes are complete, I will run the Behavioral Simulation to check the RGB outputs. I will then run synthesis and implementation, generate a new bitstream and test the updated design on the VGA monitor.

I want to keep the design simple and make sure I understand how each part works before adding more features.

### Next Steps

After completing and testing the cat's face, I would like to add a switch to make the cat blink. My idea is to use one of the Basys3 switches to change the eyes between open and closed. I plan to work on this during Week 4.#

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
