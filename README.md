Download Link: https://assignmentchef.com/product/solved-ence361-week-4-laboratory-adc
<br>
This is the last of the formal laboratories for the course.  From now on, you will use the lab sessions to work on the project.  The first priority is <strong><em>Milestone 1 in Week 5</em></strong>.

<ol>

 <li><strong><em>Outcomes: </em></strong></li>

</ol>

<ul>

 <li>To learn how to use the ADC peripheral on the Tiva microcontroller.</li>

 <li>To explore the use of interrupts and ISRs.</li>

 <li>To explore the sampling theorem for analogue-to-digital conversion.</li>

 <li>To explore the use of data buffering in signal acquisition.</li>

 <li>To use a serial link between the Tiva microcontroller and host PC to display status information. Ø To make progress towards Milestone 1 for the project (refer to the Milestone 1 specification).</li>

</ul>

<ol start="2">

 <li><strong><em>Source files: </em></strong></li>

</ol>

You have been supplied with four new source files for this laboratory:   <strong>ADCdemo1.c</strong>, <strong>circBufT.c</strong>, <strong>circBufT.h</strong> and <strong>uartDemo.c</strong>. You will also need <strong>buttons4.h</strong> and <strong>buttons4.c</strong> from last week’s lab.

The source files can be found on Learn:  <strong>Projects and Laboratories | Laboratory source code | Week-4 </strong>

The Milestone 1 specification can also be found on Learn: <strong>Projects and Laboratories | Project Specifications – Milestone 1</strong>.

<ol start="3">

 <li><strong><em>Specification for Week 4:</em></strong></li>

</ol>

<ul>

 <li><strong>Set up a new project for the Week-4 Lab (call it “Week-4Lab”). </strong></li>

</ul>

While this is not strictly necessary, it will help to keep your work in sections.  Follow a similar procedure to that you used last week (see CCS 9_2_0 Tutorial.pdf and the Week-3 lab sheet, if you need to).  Copy the source files from Learn into your new project directory.  Remember that you will need to set up the project properties as you did in Week 3 so that links are established to the OrbitOLED and ustdlib modules.

<strong><em>Note: It is also possible to copy an existing project in such a way that the project properties are maintained. </em></strong>

Remember that you should only compile the .c files that are part of each program – use right click and “Exclude from Build” as required.

<ul>

 <li><strong>Compile, link and load ADCdemo1.c </strong>(needs access to circBufT.c and circBufT.h)</li>

</ul>

Run the program and operate the potentiometer on the Orbit board to alter the analogue input voltage between 0 and 3 V.  Observe the 12-bit integer that results.  Study the source code for ADCdemo1 in detail to understand how it works.

<ul>

 <li><strong>Prepare a new version of the program</strong> (say, c  or  miles1_v1.c) to change to the analogue input AIN9, PE4 (J1-05).  Set up the bench power supply to provide a voltage between 0 and +3 V and set the current limit to 0.01 A.  Use two banana-to-alligator cables and two of the mini cables that came with your Tiva to connect the input voltage and ground to the board.   <strong>Take care to check the voltage &amp; polarity of the applied voltage  BEFORE  you turn on the supply output. </strong></li>

</ul>

Check the operation of the program.  The relationship between the displayed value and the voltage should be perfectly linear.

<ul>

 <li><strong>Work out</strong> a suitable size for the circular buffer for two different applications:

  <ul>

   <li>For reading the position of the potentiometer if it is to be used as an input to the fitness monitor UI.</li>

   <li>For sampling data from the accelerometer, which will respond to the wearer’s footsteps. Also work out suitable sampling rates for both peripherals (refer to the Milestone 1 and 2 specifications for the project). Present a case in your lab book for the values you determine.  It is reasonable to assume that the motion of a person running is limited to &lt; 3 Hz.  Test your sampling/buffering/averaging system by means of the function generator.</li>

  </ul></li>

</ul>

<strong>Again, check the voltage of the function generator output with the scope  BEFORE  you connect to the ADC input. </strong>

<ul>

 <li>Use code from <strong>c</strong> to send the same data that is on the OLED display to the Tiva board’s host PC. Rather than sending every ADC reading, data should only be sent at predefined intervals of about 2 Hz. To view the serial data in CCS you will need to create a new terminal connection:

  <ul>

   <li>First, open the Terminal pane by clicking View &gt; Terminal. (You may prefer to use a separate application, TeraTerm for this.)</li>

   <li>With the Terminal pane open, click the “Open a Terminal” button , or Ctrl+Alt+Shift+T.</li>

   <li>In the window that opens choose Serial Terminal, with 9600 baud, 8 data bits, 0 parity bits, 1 stop bit, no flow control and 5 seconds’ timeout.</li>

   <li>The Port will vary from USB port to USB port and PC to PC. Open the Windows Control Panel, select Device Manager and expand the Ports (COM &amp; LPT) group. The name in brackets next to the entry Stellaris Virtual Serial Port is the name that should be used for the serial terminal port.</li>

  </ul></li>

</ul>

NB: The topic of serial communication will be covered in lectures in Week 7.

<ul>

 <li><strong>Carefully read the Milestone spec</strong> and make sure you understand exactly what is required. Carry on developing your code.  Remember that the compliance of your program for Milestone 1 will be checked during your lab session in Week 5.  <strong>Don’t leave your preparation to the last minute</strong></li>

</ul>




<ol start="4">

 <li><strong><em>Guidance: </em></strong></li>

</ol>

<ul>

 <li>Prepare the new programs one step-at-a-time.</li>

</ul>




<ul>

 <li>Make new code as modular as possible, using appropriately designed and named functions. This will pay off when you come to build a much bigger program to drive your fitness monitor.</li>

</ul>




<ul>

 <li>Test, test, and test once more. Make sure your tests cover the specification fully.  A lot of problems with software occur because the developer has not been thorough in testing their code.  Record how you have tested your code and save any special programs you may have used for testing.</li>

</ul>




—-:—-