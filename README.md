Download Link: https://assignmentchef.com/product/solved-csc60-lab-5-functions-make
<br>
<strong><u> PROBLEM   </u></strong><u>:</u>

<ul>

 <li>Write a <strong>function</strong> named <em>compute </em>that finds both the area and the circumference of a circle. Your function must use <strong>pointer notation </strong>(the address operator “&amp;” and the indirection operator “*”), and will be a <em>separate </em>file (compute.c) from the other code (lab5.c).</li>

 <li>You are required to create a working makefile.</li>

 <li>You must edit <strong>c </strong>to add your name at the top, and add you name at about line 35 fprintf(data_out, “
<strong>Your name here. </strong>Lab 5. 

”);</li>

</ul>

<strong>The function prototype is</strong>:

/* Function to compute the area and the circumference  */

/* of a circle   */

<h1>void compute(double radius, double *area, double *cir);</h1>

You will need the file <strong>lab5.c</strong> as your main/driver program for the function.  This main program will set things up, read the values from the file, and print the output sentences.  You will also need <strong>lab5.h </strong>and <strong>lab5.dat</strong>.

<strong><u>THE FORMULAS</u></strong> (in <strong><em><u>algebraic</u></em></strong> notation)(must be translated to C notation):

<ul>

 <li>area of a circle (2) circumference of a circle a = PI * radius<sup>2    </sup>c = 2 * PI * radius</li>

</ul>

<strong><u>TO GET THE FILES YOU NEED</u>:</strong>

First move to your class folder by typing:  <strong>cd csc60</strong>

The following command will create a directory named <strong>lab5</strong> and put all the needed files into it below your csc60 directory.

Type:  <strong>cp  -R  /gaia/home/faculty/bielr/files_csc60/lab5  .</strong>

Spaces needed:  (1) After the <strong>cp                                            <em>↑</em></strong><em> Don’t miss the space &amp; dot.</em>

<ul>

 <li>After the <strong>-R</strong></li>

 <li>After the directory name at the end &amp; before the dot.</li>

</ul>

After the files are in your account and you are still in <strong>csc60</strong>, you need to type: <strong>chmod 755 lab5 </strong>This will give permissions to the directory.

Next move into lab5 directory (cd lab5), and type: <strong>chmod  644  lab5* </strong>This will give permissions to the files.

Your new lab5 directory should now contain: lab5.c, lab5.h, lab5.dat

<strong><u>INPUT/OUTPUT DESCRIPTION</u></strong>:

The <strong>input</strong> is a list of varying length of type double values in the file <strong>lab5.dat</strong>.    Each record (or line) will have one value for the radius.

The <strong>output</strong> is a chart showing the radius, area, and circumference of a circle.

<strong><u>DEFINED OUTPUT APPEARANCE</u></strong>:

Print statements are included in the main program, and require no changes, except your name.

Your name here.  Lab 5.

Radius     Area     Circumference  ——–  ——–  —————

3.70     43.01        23.25

6.80    145.27        42.73

<strong><em>ONLY the first two lines are shown here</em></strong>.  You should validate the correctness of the other lines.

<strong><u>ALGORITHM DEVELOPMENT – Pseudo code</u></strong>:

/*————————————————————————-*/ main                                 /* main is given to you as <strong><em>lab5.c  </em></strong> */     Open the data file and check for error on open.

Open the output file and check for error on open.

Print headers.     while ( good data reading(fscanf) a radius )

Call compute

Print the radius, area, and circumference.    Close the files.

/*————————————————————————-*/

/* This code, <strong>compute.c,</strong> will reside in a <em>separate</em> <em>file </em>       */

/* <em>from the main function </em>                                                       */

/* Function to compute the area and the circumference  */

/* of a circle                                                                                */

/* Remember: #include “lab5.h”                                            */

<h1>void compute(double radius, double *area, double *cir)</h1>

Calculate the area

Calculate the circumference

Return

/*————————————————————————-*/

<strong><u>REMINDERS</u></strong>:

<ul>

 <li>Remember to put your name and Lab 5 in the comment header and in the output.</li>

 <li>Remember the operator for multiplication is the asterisk (*).</li>

 <li>Since we are already including math.h, use <strong>M_PI</strong> for the value of PI.</li>

 <li>You should examine the data file and confirm the correctness of the answer produced by your program.</li>

 <li>Changes: <strong>c</strong> to add your name; create <strong>compute.c</strong> in separate file; create a <strong>makefile </strong> You will also need to add <strong>-lm</strong> on the line that does the <strong>gcc</strong> in the makefile.</li>

 <li>The Output is going to the file <strong>out</strong></li>

</ul>

<strong><u>CREATING A MAKE FILE: </u></strong> Use the slides 13-15 of 5-UNIX as a reference. Also pasted here.

The Dependency Chart of Lab5 program:

lab5.c       lab5.h              compute.c                  lab5.h

The first line should be a comment with your name.

Next: use a name like <em>lab5</em>, followed by the *.o files and the *.h file

Next:  one or two tabs followed by the *.o files and the rename of the executable You will need to add <strong>-lm</strong> on the line that does the <strong>gcc</strong> in the makefile.

Next: the *.o file name, followed by a colon, followed by the *.c file and the *.h name Next: compile without linking the .c file Separate your Rules with empty lines.

<strong><u>PREPARE YOUR FILE FOR GRADING:</u></strong>

When all is well and correct,

Type:  <strong>script StudentName_lab5.txt  </strong>[Script will keep a log of your session.]

Type:  <strong>touch lab5.h     </strong>to force a recompilation

Type:  <strong>make                 </strong>to compile the code

Type:  <strong>lab5       </strong>to run the program to show the output of the program

(or <u>whatever name</u> you used for the executable)

Type:  <strong>cat lab5.out     </strong>to see the output of your program Type:  <strong>exit </strong>to leave the script session

<strong><u>Turn in your completed session:</u></strong>

Go to Canvas and turn in (no zip files):

<ol>

 <li>c</li>

 <li>makefile</li>

 <li>c</li>

 <li>your script session (StudentName_lab5.txt)</li>

</ol>

 more on next page  




CSC60.  Lab 5.  Functions &amp; make                                                                        Page 4 of 5.

CSC60.  Lab 5.  Functions &amp; make                                                                        Page 5 of 5.

<strong><u>Helpful slides:</u></strong>

<strong><u>Slide 13:</u></strong>

<em>/*   Second pass at a makefile:      */</em>

<em>/*  Look at its contents. We have no p2.h but it is included in light italics       to show where it would be placed.              */</em>

<em> </em>

&gt;cat makefile # Your name

power2: power2.o compute.o  <em>p2.h </em>        gcc power2.o compute.o  -o power2 -lm

power2.o: power2.c  <em>p2.h </em>        gcc -c power2.c

<table>

 <tbody>

  <tr>

   <td width="87"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

compute.o: compute.c  <em>p2.h </em>        gcc -c compute.c

<strong><u>Slide 15: </u></strong>

<strong><em>/*   Helpful Comments */</em></strong>

When you enter <strong>vim</strong>, while in Command Mode, type: <strong>  :set list</strong>

This will show the non-printable characters:

^I = tab

$ = end of line

To create a tab on athena, you may have to hit the tab key <strong>twice</strong> in a row. You will know you have a correct tab when you see the ^I.

(To reverse the action of <strong>:set list</strong>, retype it and add an exclamation point to the end of the   line.    Ex:  <strong>:set list!</strong> )