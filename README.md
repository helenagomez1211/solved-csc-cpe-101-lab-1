Download Link: https://assignmentchef.com/product/solved-csc-cpe-101-lab-1
<br>
<ol>

 <li>Login to Linux environment: login: &lt;enter username&gt; Password: &lt;enter password&gt;</li>

 <li>Open a terminal window. To do so, from the system menu on the desktop toolbar, select <strong>Applications</strong> → <strong>System Tools</strong> → <strong>Terminal</strong>. The Terminal program will present a window with a command-line prompt. At this prompt you can type Linux commands to list files, move files, create directories, etc. For this lab you will use only a few commands. Additional commands can be found from a link on the course website.</li>

 <li>In the terminal, type <strong>ls</strong> at the prompt and hit &lt;Enter&gt;. This command will list the files in the current directory. (In some environments, e.g., Windows, a directory is commonly referred to as a folder.)</li>

 <li>If you type <strong>pwd</strong>, the current directory will be printed (it is often helpful to type <strong>pwd</strong> while you are navigating directories). If you type <strong>tree</strong>, then you will see a tree-like listing of the directory structure rooted at the current directory.</li>

 <li>Create a new directory for your coursework by typing <strong>mkdir CPE101</strong>. Use <strong>ls</strong> again to see that the new directory has been created.</li>

 <li>Change into this new directory with <strong>cd</strong> by typing <strong>cd CPE101</strong>. To move back “up” one directory, type <strong>cd ..</strong>.</li>

</ol>

To summarize:

cd ~

mkdir CPE101

chmod go-rx CPE101    cd CPE101




<ol start="7">

 <li>Create a directory as LAB1</li>

</ol>

mkdir LAB1     cd LAB1

<strong>Editor: </strong>

There are many options for editing a Python program. On the department machines, you will find vi, vim, emacs/xemacs, nano, gedit, and some others. The editor that one uses is often a matter of taste. You are not required to use a specific editor, but we will offer some advice (and we will try to help with whichever one you choose). An editor is a personal choice – ask your friends which one(s) they use!

If you decide to connect to the department machines from home, then you’ll want an editor that can work via a remote connection without much effort (i.e., without installing and running additional software). This makes gedit a less than desirable candidate (unless you want to learn two editors). The others will work fine, though you’ll see some differences between xemacs and emacs (which is what you’d use remotely).

vi and emacs are powerful editors once you have learned how to use them. But they require some initial effort to learn their command sequences. Knowledge of one of these will, however, serve you well for quite some time.

nano (or pico, when nano isn’t available) is very simple. It will feel, in some respects, like using Notepad. It is quick to learn and easy to use. Some people will mock others for using nano (some people are elitist dorks). You might choose to start with nano and then switch to one of the other editors as you “outgrow” nano (the others provide features that can aid you when programming).

<strong>A note concerning tabs:</strong> Whichever editor you choose, you should lookup how to convert tabs to spaces so that your Python source files do not contain a mix of tabs and spaces. <strong>DO NOT use tab characters in your files.</strong>

In general, whichever editor you choose, you should invest some time early to learn how to navigate quickly within a file. More specifically, you will want to learn how to jump to a specific line, to search within the file, and copy/paste lines.

If you cannot decide, then use nano. You always have the option of switching at a later time.

<ol start="8">

 <li>You will start the editor by typing the name at the prompt followed by the name of the file that you wish to edit. For instance, <strong>nano -Ec lab1.py</strong> (note the <strong>-Ec</strong> is useful to 1) convert tabs to spaces (E) and 2) direct nano to display the line number for the cursor’s current position(c)).</li>

 <li>A Python program is written in a plain text file. The program can be run by using a Python interpreter.</li>

 <li>Save this file as lab1.py</li>

 <li>Note: the files are accessible through PolyLearn.</li>

 <li>To execute the program, type <strong>python lab1.py</strong> at the command-line prompt.</li>

 <li>Using your editor of choice, modify <em>py</em> to replace <strong>World</strong> with your name and fill out the header comment at the beginning of the file. Execute the program to see the effect of this change.</li>

 <li>The Python interpreter can be used in an interactive mode. In this mode, you will be able to type a statement and immediately see the result of its execution. Interactive mode is very useful for experimenting with the language and for testing small pieces of code.

  <ol>

   <li>Type python and press enter the &gt;&gt;&gt; prompt will appear in your screen.</li>

  </ol></li>

</ol>

$ python

&gt;&gt;&gt;

<ol>

 <li>Now try some arithmetic statements and see the results</li>

 <li>Type each of the following (hit enter after each one) to see the result. When you are finished, you can exit the interpreter by typing ctrl-D (i.e., hold the control key and hit d).</li>

</ol>

<a href="#_Toc5479">  0 +                                                                                                                   1 </a>

<a href="#_Toc5480">  2 *                                                                                                                   2 </a>

<a href="#_Toc5481">  19 //                                                                                                                 3 </a>

<a href="#_Toc5482">  19 /                                                                                                                  3 </a>

<a href="#_Toc5483">  19 / 3.0   19.0 / 3.0   4 * 2 + 27 // 3 +                                                            4 </a>

<a href="#_Toc5484">  4 * (2 + 27) // 3 +                                                                                             4 </a>







<ol>

 <li>Type python3 and press enter the &gt;&gt;&gt; prompt will appear in your screen.</li>

</ol>

$ python3

&gt;&gt;&gt;

<ol start="3">

 <li>Try 19//3, 19/3, and 19/3.0 and check the difference with previous results.</li>

 <li>What is different between / and // operator?</li>

</ol>

Many people tend to focus on writing code as the singular activity of a programmer, but testing is one of the most important tasks that one can perform while programming. Proper testing provides a degree of confidence in your solution. During testing you will likely discover and then fix bugs (i.e., debug). Writing high quality test cases can greatly simplify the tasks of both finding and fixing bugs and, as such, will actually save you time during development.

For this part of the lab you will practice writing some simple test cases to gain experience with the unittest framework. Using your editor of choice, open the <em>lab1_test_cases.py</em> file. This file defines, using code that we will treat as a boilerplate for now, a testing class with a single testing function.

In the <em>test_expressions</em> function you will see a single test case already provided. You must add additional test cases to verify that the following expressions (exactly as written) produce the values that you expect. Note that you will want to use assertAlmostEqual instead of assertEqual to check computations that are expected to result in a floating point value.

<h1><a name="_Toc5479"></a>             0 + 1</h1>

<h1><a name="_Toc5480"></a>             2 * 2</h1>

<h1><a name="_Toc5481"></a>             19 // 3</h1>

<h1><a name="_Toc5482"></a>             19 / 3</h1>

    19 / 3.0

<h1><a name="_Toc5483"></a>             19.0 / 3.0</h1>

    4 * 2 + 27 // 3 + 4

<h1><a name="_Toc5484"></a>             4 * (2 + 27) // 3 + 4</h1>

Remember: use <strong>assertAlmostEqual</strong> when comparing floats, use <strong>assertEqual</strong> when comparing integers.

<ol>

 <li>Save the following program as <strong>python file lab1_test_cases.py</strong> Note: the files are accessible through PolyLearn.</li>

</ol>

or you can copy and paste the code in your editor and save as <strong>lab1_test_cases.py</strong> # Test cases example for lab 1.

import unittest<strong><em>      </em></strong># import the module that supports writing unit tests # Define a class that will be used for these test cases.

# This class will include testing functions.

# Much of this code should be viewed as boilerplate for now.

# class TestsLab1(unittest.TestCase)<strong><em>:    </em></strong>def test_expressions(self)<strong><em>:         </em></strong># Defines one testing function.

<strong><em>      </em></strong>self.assertEqual(0 + 1<strong><em>, </em></strong>1)

<strong><em>      </em></strong># Add code here (like the line above) for the additional test cases. <strong><em>      </em></strong>self.assertEqual(2 * 2<strong><em>, </em></strong>4)

<strong><em>      </em></strong>self.assertAlmostEqual(19/3.0<strong><em>, </em></strong>6.333333333333333)

# Run the unit tests.

if __name__ == <strong>‘__main__’</strong><strong><em>:    </em></strong>unittest.main()




Run the program by typing <strong>python3 lab1_test_cases.py</strong>. You should now see a report of any tests that did not succeed.

<ol start="2">

 <li>Raise your hand as soon as you finished the program</li>

 <li>Submit your work in PolyLearn</li>

 <li>If you have time do more practice on Linux commands:

  <ol>

   <li>l shows list of files</li>

   <li>ls –directory listing ls [-l] [-s] [-a] [dir or file names…]</li>

  </ol></li>

</ol>

-l long listing

-s include file sizes

-a all files

<ol>

 <li>Copy a file cp –copying files cp &lt;original file&gt; &lt;new file&gt; Example:</li>

</ol>

$ cp file1 file2

<ol>

 <li>Rename a file mv –rename files</li>

</ol>

mv &lt;original filename&gt; &lt;new filename&gt;

<ol>

 <li>Delete a file rm –remove files rm &lt;option&gt; &lt;file&gt;</li>

</ol>

-f force

-i interactive (ask before removing)

-r recursive

<ol>

 <li>Search grep –searching files grep &lt;string&gt; &lt;filename&gt;</li>

</ol>

Example: File homework1.txt contains: This is line1.

This is line2 for CSC101.

This is line3.

grep cs390 homework1.txt Result:

This is line2 for CSC101.




More Linux command can be found in Linux documents and online resources.











