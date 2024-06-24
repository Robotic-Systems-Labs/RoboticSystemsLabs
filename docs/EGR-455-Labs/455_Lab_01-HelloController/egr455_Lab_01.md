---
layout: default
title: Lab 1 -- Hello Controller
parent: EGR 455 Labs
nav_order: 2
---

{: .fs-2 }
This document was last modified: <scr id="demo">.

<script>
let text = document.lastModified;
document.getElementById("demo").innerHTML = text;
site.last_edit_timestamp= text;
</script>

# Lab 1: Hello Controller
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Lab Objectives

1.	Ensure that you are ready to use the Robotic System`s mock Controller unit, which uses PSoC 5LP
and an LCD Screen, for many of the lab assignments.
2.	Get you started with some coding on the PSoC controller.

## Deliverables

- [ ] <ins>In-class demonstration</ins>, using your completed "controller" indicated by writing your name on
    the back side of the PCB, display your name in the top left corner of the LCD screen
    and towards the bottom right corner of the LCD screen, you have “Count:” with values counting up by ones.

- [ ] <ins>In-class demonstration</ins> of the PSoC`s built-in LED blinking.  

- [ ] <ins>A Canvas submitted</ins> of the Lab`s PSoC Creator archived/zipped file for this lab.

{: .warning-title}
> Warning
>
> <Strong><ins>To be eligible</ins></strong> to receive credit for the code submission,
> you <strong><ins> must receive Demonstration credit.</ins></strong>


## General Steps for Completion of Lab

### Step 1 - Double Check Parts 
<details open markdown="block">
<summary>To Hide Details</summary>

The following table lists the parts, quantities, and PCB 
designators. <strong>Figure 1</strong> shows a view of most of the parts needed to build mock controller 
for the Robotic Systems courses.

| QTY  | Part Name                     |PCB designator(s) |
|:------|:-----------------------------|:-----------------|
| 1     | Custom PCB                   |                  |
| 2     | 40 pin Female Header         | U1               |
| 14    | 4 pole Screw Header          | J1 (6.5x), J2(2x),<br> J9 (5x), J8 (0.5x)              |
| 1     | DC Power Jack                | J6               |
| 1     | 16 pins IC Socket            | U2               |
| 2     | 6 pin Female Header          | J11, J12         |
| 1     | 0.1 uF Capacitor (104)       | C1               |
| 1     | 1 uF Capacitor (105)         | C2               |
| 2     | 4 pin Female Header          | J7, J10          |
| 1     | 16 pin Female Header         | U3               |
| 2.5   | 40 pin Male Header           |                  |
| 1     | PSoC 5LP Development Kit     |                  |
| 1     | Basic 16x2 Character LCD     |                  |
| 5     | Bumper Pads     |  ** To provide protection for accidental shorts and/or scratches from PCB   |
| 4     | Socket Head Screw<br> M2.5, 14 mm Long     | ** Use to attach LCD Screen to PCB if so desired. |
| 8     | M2.5 Nylon Hex Nut    | ** Use to attach LCD Screen to PCB if so desired.   |

<figure>
    <img src="imageParts.jpg"
         alt="Parts needed to build mock controller">
    <figcaption><strong>Figure 1:</strong> Parts needed to build mock controller.</figcaption>
</figure>  

</details>

### Step 2 - Solder Parts
<details open markdown="block">
<summary>To Hide Details</summary>

Solder the different parts on to build your "Controller," similar to what is shown in <strong>Figure 2.</strong> See below for more details and steps.

<figure>
    <img src="imageGoal.jpg"
         alt="Showing the completed mock controller">
    <figcaption><strong>Figure 2:</strong> Showing the completed mock controller.</figcaption>
</figure>

{: .new-title}
> TIPS
> <ul>
>   <li> When soldering through-hole parts, it is commonly recommended that solder 
>   parts be attached in order of smallest height to largest.</li>
>   <li> Place/work with parts to help keep the PCB “level” to help keep parts tight to the board.</li>
>   <li> Solder one (or two, if needed) to hold the part in place so you can inspect and
>   correct the positioning before soldering all the pins.</li>
>   <li> Both the pad and pin need to get hot so that the solder flows and bonds correctly.</li>
>   <li> Too much heat for the type of solder can ruin the solder joint(s).</li>
>   <li> When part alignment matters, place all the parts and then solder a few pins to hold the 
>   alignment. Then, if applicable, separate into a sub-group before finishing the soldering
>   of the remaining pins. Check and be careful not to mess up that alignment.</li>

Using the tip from above, it is recommended that you add parts in the following order:
1.	Capacitors. (<strong>Figure 3</strong> for refernce shown farther below)
2.	Dip socket. (<strong>Figure 4</strong>)
    * <strong> Make sure <ins>the notch</ins> on one of the short ends of the DIP socket is <ins>next to the U2 marking</ins>.</strong>
    This notch indicates how the IC chip get inserted in where both notches are together. This notch is clearer to see in
    in <strong>Figure 6.</strong>
3.	Female and male headers at U1 (PSoC). (<strong>Figure 5</strong>)
4.	Remaining female headers at J7, J10, J11, J12, and U2. (<strong>Figure 6</strong>)
5.	Screw headers, connected together at J1 and J9.
6.	Remaining screw headers.
7.	DC Power Plug.
8.	Male header to LCD screen.
9.	Bumpers on the back side of PCB.


{: .warning-title}
> Attention!
>
> Make sure the opening on the side of the screw terminals are
> facing out, away from PCB, to make it easy to secure wires later.
> (<strong>Figure 7</strong> for refernce shown farther below)


<figure>
    <img src="imageCap.png"
         alt="Showing the placement of capacitors">
    <figcaption><strong>Figure 3:</strong> Showing the placement of capacitors.</figcaption>
</figure>
<br>
<figure>
    <img src="imageDipClose.png"
         alt="Showing the placement of dip socket">
    <figcaption><strong>Figure 4:</strong> Showing the placement of dip socket.</figcaption>
</figure> 
<br>
<figure>
    <img src="imagePSoCwHeaders.png"
         alt="Showing male and female headers held in alignment with PSoC Dev board">
    <figcaption><strong>Figure 5:</strong> Showing male and female headers held in alignment with PSoC Dev board.</figcaption>
</figure>
<br>
<figure>
    <img src="imageRemainingHeaders.png"
         alt="Showing remaining female header">
    <figcaption><strong>Figure 6:</strong> Showing remaining female header.</figcaption>
</figure>
<br>
<figure>
    <img src="imageScrewsOpenOut.png"
         alt="Attempting to Show how the wire openings on the screw termials are facing out.">
    <figcaption><strong>Figure 7:</strong> Attempting to Show how the wire openings on the screw termials are facing out.</figcaption>
</figure>
<br>

</details>
### Step 3 - Inspection of Work
<details open markdown="block">
<summary>To Hide Details</summary>

If you haven`t been doing it already, now is the best time to inspect your work on
assembling your “Controller.” Things you are on the lookout for are:
<ul>
    <li> Missed parts. Look for parts you may have forgotten to either add or fully solder.
    The only opening that will not have something soldered to it are the non-plated mechanical
    holes for the screws to mount/secure the LCD screen.</li>

    <li> Quality of soldered joints. Look at all the points you soldered. (a) Do they have 
    the appearance of a slightly melted Hersey kiss? This means that the solder flows in a smooth
    cone-like shape. See <strong> Figure 8</strong> and look at the solder joint the Green arrows
    are pointing to for reference. Or look at the solder joints back in <strong>Figure 7. </strong>
    You <strong><ins>do not want balls</ins> of solder at the pins</strong> like the what the
    <strong> RED arrows</strong> are pointing to in <strong>Figure 8.</strong> </li>

    <li> Check continuity. While inspecting your solder joints, are there places you 
    are <strong> not certain</strong> they are either (a) making a connection or (b) could be 
    shorting? Now is the time to make sure you will not have problems later. </li>
</ul>

<figure>
    <img src="image033.png"
         alt="Attempting to show how to check solder joint quality.">
    <figcaption><strong>Figure 8:</strong> Attempting to show how to check solder joint quality where 
    the green arrows are what is desired.</figcaption>
</figure>


</details>
### Step 4 - Understanding Your Controller

#### Processor
{: .fs-4 .fw-500}
<details open markdown="block">
<summary>To Hide Details</summary>

Similar to an Industrial Controller Unit, your mock Robotic System's Controller
has a Processor which is the PSoC 5LP, which is within the Orange 
center box of <strong>Figure 9.</strong>  To protect our processor, the whole Dev board
is supported by header to help prevent the kit's programmer section from snapping/breaking 
off from the PSoC 5LP section. <strong>Figure 10</strong> shows those two sections and a pin overview of the PSoC 5LP. 

{: .warning-title}
> Warning!
>
> You can only program this Dev board on the one end with the male USB A 
> through the programmer section of the dev board.

<figure>
    <img src="ImageControlPSoC.jpg"
    width="200" height="200"
         alt="Highlighting the location of the processor with the orange box and the in/output connector with the two red boxes.">
    <figcaption><strong>Figure 9:</strong> Highlighting the location of the processor with the orange box 
    and the in/output connector with the two red boxes.</figcaption>
</figure>
<br>
<figure>
    <img src="imagePSoCoverview.png"
    width="300" height="300"
         alt="PSoC 5LP pin overview and section.">
    <figcaption><strong>Figure 10:</strong> PSoC 5LP pin overview and section.</figcaption>
</figure>
</details>

#### Inputs and Outputs
{: .fs-4 .fw-500}

<details open markdown="block">
<summary>To Hide Details</summary>
Again, like an Industrial Controller Module, the different
Input and Output that goes to the processor have a separate connection for
easy and secure points of connection. These are in located in the red boxes of 
<strong> Figure 9.</strong> The only I/O pins for the PSoC 5LP not on these screw terminal blocks 
are the ones going to the LCD screen.
</details>

#### Shared Processor Power Levels
{: .fs-4 .fw-500}

<details open markdown="block">
<summary>To Hide Details</summary>

For any of the devices that will be connected to the controller and will be using the same 5 volts, 1/2 
an amp power as the PSoC 5LP, there are the two, 5-pin headers indicated by the yellow box in 
<strong>Figure 11</strong> below. In addition to these headers, there are two set of locations within the screw 
terminal connectors. One set is at the end of screw terminal connectors opposite of the DC power jack and 
close to the LCD screen. The other set is diagonal to the first noted set, next to the 
V<sub>bus</sub> input power connection.

{: .new-title}
> Note
>
> All power sources have their grounds connected together via a Ground Plane within the PCB board to help you not experience that issue of things 
> not working because the grounds were not tied together. (You’re welcome. I hope because this a lesson <strong><ins>you must learn</ins></strong> and 
> most <ins><strong>ready learn </strong> it the hard way</ins>.)

<figure>
    <img src="ImageControlLowPower.jpg"
    width="200" height="200"
         alt="The yellow box indicates a point of connection for multiple 5 volts and ground connections.">
    <figcaption><strong>Figure 11:</strong> The yellow box indicates a point of connection for multiple 5 volts and ground connections.</figcaption>
</figure>

</details>

#### Motor Driver Unit
{: .fs-4 .fw-500}

<details open markdown="block">
<summary>To Hide Details</summary>

Just like an Industrial Controller, our Robotic System’s Controller processor cannot handle the 
higher voltage and amperage levels that the motor needs to have to operate without causing damage 
to the processor. To safely control the motor at a higher level than the processor, the processor 
communicates with some type of motor controller device. Your kit has been designed to do this with 
an H-Bridge IC chip. The H-Bridge chip sits in the dip socket and has the needed connections either 
directly handled with traces within the PCB or to the two headers on either side. We are using a 
dip socket connection instead of soldering the IC to the PCB for ease of possible repair. These headers 
and dip socket for our motor driver unit is indicated by the orange box in <strong>Figure 12.</strong>

<figure>
    <img src="ImageControlMotorDriver.jpg"
    width="200" height="200"
         alt="The orange box indicates the motor driver unit area.">
    <figcaption><strong>Figure 12:</strong> The orange box indicates the motor driver unit area.</figcaption>
</figure>

</details>

#### Motor Power
{: .fs-4 .fw-500}

<details open markdown="block">
<summary>To Hide Details</summary>

To provide a higher voltage and amperage level for the different motors that will be used in the course, 
there is the DC power jack along with 4 sets of screw connectors. These have been identified by the 
red “box” in <strong> Figure 13.</strong>

<figure>
    <img src="ImageControlHigherPower.jpg"
    width="200" height="200"
         alt="The red box area indicates where the higher motor power comes in and is accessed.">
    <figcaption><strong>Figure 13:</strong> The red box area indicates where the higher motor power comes in and is accessed.</figcaption>
</figure>

</details>

#### User Interface Screen
{: .fs-4 .fw-500}

<details open markdown="block">
<summary>To Hide Details</summary>

To handle the feedback, one may that a simple indicator light cannot do, a user interface screen is 
commonly employed. You have been provided with a 2-by-16-character LCD screen that the PCB has the 
different connection handled for you so that it is a simple process to connect the LCD screen when 
needed/desired whose location is indicated in <strong> Figure 14</strong> by a red box. While you 
will not be asked to use to in all the upcoming labs, you may find it a useful tool for debugging.

<figure>
    <img src="ImageControlScreen.jpg"
    width="200" height="200"
         alt="The red box area indicates where a display screen can be connected.">
    <figcaption><strong>Figure 14:</strong> The red box area indicates where a display screen can be connected.</figcaption>
</figure>

</details>


### Step 5 - First Code in PSoC

#### Create a Workspace and Start a Project
{: .fs-4 .fw-500}

<details open markdown="block">
<summary>To Hide Details</summary>

If you have not installed PSoC Creator as part of Lab 0, you will need to go back and do so 
before moving forward.

Open PSoC Creator. While opening the program, you might get a pop-up screen that ask to register 
or allow “cykeilic” app to make changes as shown in <Strong>Figure 15.</strong> You can just say 
no to this request if you so desire. When the program opens, your screen will look something like 
<strong>Figure 16.</strong>

<figure>
    <img src="cykeilicImage.jpg"
        alt="Showing the pop-up screen that asks to register or allow “cykeilic” app to make changes.">
    <figcaption><strong>Figure 15:</strong> Showing the pop-up screen that asks to register or allow “cykeilic” app to make changes.</figcaption>
</figure>
<br>
<figure>
    <img src="psocStartScreen.png"
        alt="Showing the home screen of PSoC Creator after launching it and without opening any project or workspace files.">
    <figcaption><strong>Figure 16:</strong> Showing the home screen of PSoC Creator after launching it and without opening any project or workspace files.</figcaption>
</figure>
<br>

Now to start the process of creating a new project in a new workspace, select 
<strong>File</strong> -> <strong>New</strong> -> <strong>Project</strong> as show in 
<strong>Figure 17</strong> from the pull-down menu. 

<figure>
    <img src="newProjectPSoCcreator.png"
        alt="Showing a visual reference to starting a new project.">
    <figcaption><strong>Figure 17:</strong> Showing a visual reference to starting a new project.</figcaption>
</figure>
<br>



</details>
#### PSoC Creator Code Setup for an Output Pin
{: .fs-4 .fw-500}

<details open markdown="block">
<summary>To Hide Details</summary>

Open PSoC Creator and create a new Project (select File -> New -> Project) (See Figure 8 toward the end for a visual reference)

</details>
#### Create Code an Output Pin
{: .fs-4 .fw-500}

<details open markdown="block">
<summary>To Hide Details</summary>

Open PSoC Creator and create a new Project (select File -> New -> Project) (See Figure 8 toward the end for a visual reference)

</details>

#### Create Program the PSoC 5LP
{: .fs-4 .fw-500}

<details open markdown="block">
<summary>To Hide Details</summary>

Open PSoC Creator and create a new Project (select File -> New -> Project) (See Figure 8 toward the end for a visual reference)

</details>

#### Create Modify Code
{: .fs-4 .fw-500}

<details open markdown="block">
<summary>To Hide Details</summary>

Open PSoC Creator and create a new Project (select File -> New -> Project) (See Figure 8 toward the end for a visual reference)

</details>

### Step 6 - Learning How to Work with the LCD Screen in PSoC Creator
<details open markdown="block">
<summary>To Hide Details</summary>

To make it easier to connect the motor and encoder wires to the controller, it is <strong>strongly suggested</strong> that you <ins>solder six
of your jumper wires</ins> to each of the wires of the motor wire harness, similar to w

#### Cfgjsgjnhmgshnode
{: .fs-4 .fw-500}

<details open markdown="block">
<summary>To Hide Details</summary>

Open PSoC Creator and create a new Project (select File -> New -> Project) (See Figure 8 toward the end for a visual reference)


</details>

### Step 7 - Test and Modify Code for LCD Screen
<details open markdown="block">
<summary>To Hide Details</summary>

To make it easier to connect the motor and encoder wires to the controller, it is <strong>strongly suggested</strong> that you <ins>solder six

</details>
