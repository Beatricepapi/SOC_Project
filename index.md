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

<img width="450" alt="VGA Colour Stripes" src="docs/assets/images/VGA_Stripes.jpeg">

*Figure 1: Original VGA Colour Stripes design displayed on the monitor using the Basys3 FPGA board.*

### Vivado Project Summary

![Vivado Project Summary](docs/assets/images/Project_Summary.png)

*Figure 2: Vivado project setup showing the Basys3 FPGA device and design sources.*

### Behavioral Simulation

![Behavioral Simulation](docs/assets/images/Simulation.png)

*Figure 3: Behavioral simulation showing VGA timing signals and RGB colour outputs.*

### Implementation Results

![Implementation Results](docs/assets/images/Implementation.png)

*Figure 4: Implemented FPGA design and timing summary in Vivado.*

### Next Week

Next week, I plan to start modifying the original design to display my own image. I have chosen a simple Kawaii Kitty design with a pink background and a white cat face.

## **Template VGA Design**
### **Project Set-Up**
Summarise the project set-up and design flow. Include a screenshot of your own set-up, for example see the image of my Project Summary window below. Guideline 1 short paragraph.

<img src="https://raw.githubusercontent.com/melgineer/fpga-vga-verilog/main/docs/assets/images/VGAPrjSum.png">
### **Template Code**
Outline the structure and design of the Verilog code templates you were given. What do they do? Include reference to how a VGA interface works. Guideline: 2/3 short paragraphs, consider including screenshot(s).
### **Simulation**
Explain the simulation process. Reference any important details, include a well-selected screenshot of the simulation. Guideline: 1/2 short paragraphs.
### **Synthesis**
Describe the synthesis and implementation processes. Consider including 1/2 useful screenshot(s). Guideline: 1/2 short paragraphs.
### **Demonstration**
Perhaps add a picture of your demo. Guideline: 1/2 sentences.

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
