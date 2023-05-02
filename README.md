Download Link: https://assignmentchef.com/product/solved-comp1210-project-5-dodecahedron-list-app
<br>
<h1>Deliverables</h1>

Your project files should be submitted to Web-CAT by the due date and time specified.  You may submit your files to the <u>skeleton code</u> assignment until the project due date but should try to do this by Friday (there is no late penalty since the skeleton code assignment is ungraded for this project).  The files you submit to skeleton code assignment may be incomplete in the sense that method bodies have at least a return statement if applicable or they may be essentially completed files.  In order to avoid a late penalty for the project, you must submit your <u>completed code</u> files to Web-CAT no later than 11:59 PM on the due date for the completed code.  You may submit your <u>completed code</u> up to 24 hours after the due date, but there is a late penalty of 15 points.  No projects will be accepted after the one-day late period.  If you are unable to submit via Web-CAT, you should e-mail your project Java files in a zip file to your TA before the deadline.




Files to submit to Web-CAT (all three files must be submitted together):

<ul>

 <li>java</li>

 <li>java</li>

 <li>java</li>

</ul>




<h1>Specifications</h1>

<strong>Overview: </strong>You will write a program this week that is composed of three classes: the first class defines Dodecahedron objects, the second class defines DodecahedronList objects, and the third, DodecahedronListApp, reads in a file name entered by the user then reads the list name and Dodecahedron data from the file, creates Dodecahedron objects and stores them in an ArrayList, creates a DodecahedronList object with the list name and ArrayList, prints the DodecahedronList object, and then prints summary information about the DodecahedronList object.




<table width="586">

 <tbody>

  <tr>

   <td colspan="3" width="586">A dodecahedron has 12 equal pentagonal faces, 20 vertices, and 30 edges as depicted below. The formulas are provided to assist you in computing return values for the respective Dodecahedron methods described in this project.</td>

  </tr>

  <tr>

   <td width="198"> </td>

   <td width="184"> Surface Area (A) Volume (V) Edge length (a) Surface/Volume ratio (A/V)</td>

   <td width="204">    </td>

  </tr>

  <tr>

   <td colspan="3" width="586"> </td>

  </tr>

 </tbody>

</table>




<ul>

 <li><strong>Dodecahedron.java (<u>assuming that you successfully created this class in Project 4, just copy</u> <u>the file to your new Project 5 folder and go on to DodecahedronList.java on page 4.</u> <u>Otherwise, you will need to create Dodecahedron.java as part of this project</u>.) </strong></li>

</ul>

<strong> </strong>

<strong>Requirements</strong>: Create a Dodecahedron class that stores the label, color, and edge (i.e., length of an edge, which must be greater than zero).  The Dodecahedron class also includes methods to set and get each of these fields, as well as methods to calculate the surface area, volume, and surface

to volume ratio of a Dodecahedron object, and a method to provide a String value of a Dodecahedron object (i.e., a class instance).







<strong>Design</strong>:  The Dodecahedron class has fields, a constructor, and methods as outlined below.




<ul>

 <li><strong>Fields</strong> (instance variables): label of type String, color of type String, and edge of type double. Initialize the Strings to “” and the double to 0 in their respective declarations. These instance variables should be private so that they are not directly accessible from outside of the Dodecahedron class, and <u>these should be the only instance variables in the class</u>.</li>

</ul>




<ul>

 <li><strong>Constructor</strong>: Your Dodecahedron class must contain a public constructor that accepts three parameters (see types of above) representing the label, color, and edge. Instead of assigning the parameters directly to the fields, the respective set method for each field (described below) should be called. For example, instead of the statement label = labelIn; use the statement setLabel(labelIn); Below are examples of how the constructor could be used to create Dodecahedron objects.  Note that although String and numeric literals are used for the actual parameters (or arguments) in these examples, variables of the required type could have been used instead of the literals.</li>

</ul>




Dodecahedron example1 = new Dodecahedron(“Small Example”, “blue”, 0.25);




Dodecahedron example2 = new Dodecahedron(” Medium Example “, “orange”, 10.1);




Dodecahedron example3 = new Dodecahedron(“Large Example”, “silver  “, 200.5);




<ul>

 <li><strong>Methods</strong>: Usually a class provides methods to access and modify each of its instance variables (known as get and set methods) along with any other required methods. The methods for Dodecahedron, which should each be public, are described below.  See formulas in Code and Test below. o getLabel:  Accepts no parameters and returns a String representing the label field.

  <ul>

   <li>setLabel: Takes a String parameter and returns a boolean. If the string parameter is not null, then the “trimmed” String is set to the label field and the method returns true. Otherwise, the method returns false and the label is not set.</li>

   <li>getColor: Accepts no parameters and returns a String representing the color field.</li>

   <li>setColor: Takes a String parameter and returns a boolean. If the string parameter is not null, then the “trimmed” String is set to the color field and the method returns true. Otherwise, the method returns false and the label is not set.</li>

   <li>getEdge: Accepts no parameters and returns a double representing the edge field.</li>

   <li>setEdge: Accepts a double parameter and returns a boolean as follows. If the edge is greater than zero, sets the edge field to the double passed in and returns true.  Otherwise, the method returns false and the edge is not set.</li>

   <li>surfaceArea: Accepts no parameters and returns the double value for the total surface area calculated using the value for edge.</li>

   <li>volume: Accepts no parameters and returns the double value for the volume calculated using the value for edge.</li>

   <li>surfaceToVolumeRatio: Accepts no parameters and returns the double value calculated by dividing the total surface area by the volume.</li>

   <li>toString: Returns a String (does<u> not </u>begin with 
) containing the information about the Dodecahedron object formatted as shown below, including decimal formatting (“#,##0.0##”) for the double values.  Newline and tab escape sequences should be used to achieve the proper layout.  In addition to the field values (or corresponding “get” methods), the following methods should be used to compute appropriate values in the toString method: surfaceArea(), volume(), and surfaceToVolumeRatio().  Each line should have no trailing spaces (e.g., there should be no spaces before a newline (
) character).  The toString value for example1, example2, and example3 respectively are shown below (the blank lines are not part of the toString values).</li>

  </ul></li>

</ul>




Dodecahedron “Small Example” is “blue” with 30 edges of length 0.25 units.

surface area = 1.29 square units    volume = 0.12 cubic units    surface/volume ratio = 10.777




Dodecahedron “Medium Example” is “orange” with 30 edges of length 10.1 units.    surface area = 2,106.071 square units    volume = 7,895.319 cubic units    surface/volume ratio = 0.267




Dodecahedron “Large Example” is “silver” with 30 edges of length 200.5 units.

surface area = 829,963.459 square units    volume = 61,765,889.248 cubic units    surface/volume ratio = 0.013




<strong>Code and Test</strong>: As you implement your Dodecahedron class, you should compile it and then test it using interactions.  For example, as soon you have implemented and successfully compiled the constructor, you should create instances of Dodecahedron in interactions (e.g., copy/paste the examples above).  Remember that when you have an instance on the workbench, you can unfold it to see its values.  You can also open a viewer canvas window and drag the instance from the Workbench tab to the canvas window.  After you have implemented and compiled one or more methods, create a Dodecahedron object in interactions and invoke each of your methods on the object to make sure the methods are working as intended.  You may find it useful to create a separate class with a main method that creates an instance of Dodecahedron then prints it out.







<ul>

 <li><strong>java</strong></li>

</ul>




<strong>Requirements</strong>: Create a DodecahedronList class that stores the name of the list and an ArrayList of Dodecahedron objects.  It also includes methods that return the name of the list, number of Dodecahedron objects in the DodecahedronList, total surface area, total volume, average surface area, average volume, and average surface to volume ratio for all Dodecahedron objects in the DodecahedronList.  The toString method returns a String containing the name of the list followed

by each Dodecahedron in the ArrayList, and a summaryInfo method returns summary information about the list (see below).




<strong>Design</strong>:  The DodecahedronList class has two fields, a constructor, and methods as outlined below.




<ul>

 <li><strong>Fields</strong> (or instance variables): (1) a String representing the name of the list and (2) an ArrayList of Dodecahedron objects. These are the only fields (or instance variables) that this class should have.</li>

 <li><strong>Constructor</strong>: Your DodecahedronList class must contain a constructor that accepts a parameter of type String representing the name of the list and a parameter of type ArrayList&lt; Dodecahedron&gt; representing the list of Dodecahedron objects. These parameters should be used to assign the fields described above (i.e., the instance variables).</li>

</ul>

<strong> </strong>

<ul>

 <li><strong>Methods</strong>: The methods for DodecahedronList are described below.

  <ul>

   <li>getName: Returns a String representing the name of the list.</li>

   <li>numberOfDodecahedrons: Returns an int representing the number of</li>

  </ul></li>

</ul>

Dodecahedron objects in the DodecahedronList.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong>

<ul>

 <li>totalSurfaceArea: Returns a double representing the total surface areas for all Dodecahedron objects in the list.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>totalVolume: Returns a double representing the total volumes for all Dodecahedron objects in the list.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>averageSurfaceArea: Returns a double representing the average surface area for all Dodecahedron objects in the list.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>averageVolume: Returns a double representing the average volume for all</li>

</ul>

Dodecahedron objects in the list.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong>

<ul>

 <li>averageSurfaceToVolumeRatio: Returns a double representing the average surface to volume ratio for all Dodecahedron objects in the list.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>toString: Returns a String (does <u>not</u> begin with 
) containing the name of the list followed by each Dodecahedron in the ArrayList.  In the process of creating the return result, this toString() method should include a while loop that calls the toString() method</li>

</ul>

for each Dodecahedron object in the list (adding a 
 before and after each).  Be sure to include appropriate newline escape sequences.  For an example, see <u>lines 2 through 19</u> in the output below from DodecahedronListApp for the <em>Dodecahedron_data_1.txt</em> input file. [Note that t<u>he toString result should <strong>not</strong> include the summary items in lines 20</u> <u>through 26 of the example.  These lines represent the return value of the summaryInfo</u> <u>method below.</u>]

<ul>

 <li>summaryInfo: Returns a String (does<u> not </u>begin with 
) containing the name of the list (which can change depending of the value read from the file) followed by various summary items:  number of Dodecahedrons, total surface area, total volume, average surface area, average volume, and average surface to volume ratio.  Use “#,##0.0##” as the pattern to format the double values.  For an example, see <u>lines 20 through 26</u> in the output below from DodecahedronListApp for the <em>txt</em> input file.  The second example below shows the output from DodecahedronListApp for the <em>Dodecahedron_data_0.txt</em> input file which contains a list name but no Dodecahedron data. <strong> </strong></li>

</ul>

<strong>Code and Test</strong>: Remember to import java.util.ArrayList.  Each of the methods above requires that you use a loop (i.e., a while loop) to retrieve each object in the ArrayList.  As you implement your DodecahedronList class, you can compile it and then test it using interactions.

Alternatively, you can create a class with a simple main method that creates a DodecahedronList object and calls its methods.




<ul>

 <li><strong>java </strong></li>

</ul>

<strong> </strong>

<strong>Requirements</strong>: Create a DodecahedronListApp class with a main method that reads in the name of the data file entered by the user and then reads list name and Dodecahedron data from the file, creates Dodecahedron objects, stores them in a local ArrayList of Dodecahedron objects, creates a DodecahedronList object with the name of the list and the <u>ArrayList of Dodecahedron objects</u>, and then prints the DodecahedronList object followed summary information about the DodecahedronList object. <strong> <u>All input and output for this project should be done in the main</u> <u>method</u></strong>.




<ul>

 <li><strong>Design</strong>: The main method should prompt the user to enter a file name, and then it should read in the data file.  The first record (or line) in the file contains the name of the list.  This is followed by the data for the Dodecahedron objects.  After each set of Dodecahedron data is read in, a Dodecahedron object should be created and stored in the local ArrayList of Dodecahedron objects.  After the file has been read in and the ArrayList has been populated, the main method should create a DodecahedronList object with the name of the list and the ArrayList of</li>

</ul>

Dodecahedron objects as parameters in the constructor.  It should then print the

DodecahedronList object, then print the <u>summary</u> information about the DodecahedronList (i.e., print the value returned by the summaryInfo method for the DodecahedronList).  The output from two runs of the main method in DodecahedronListApp is shown below.  The first is produced after reading in the <em>dodecahedron_data_1.txt </em>file, and the second is produced after reading in the <em>dodecahedron_data_0.txt </em>file.  Your program output should be formatted exactly as shown.










<table width="631">

 <tbody>

  <tr>

   <td width="42">Line #</td>

   <td width="589">Program output</td>

  </tr>

  <tr>

   <td width="42"> 12345678910111213141516171819202122232425262728 </td>

   <td width="589"> —-jGRASP exec: java DodecahedronListAppEnter file name: dodecahedron_data_1.txt Dodecahedron Test List Dodecahedron “Small Example” is “blue” with 30 edges of length 0.25 units.    surface area = 1.29 square units    volume = 0.12 cubic units    surface/volume ratio = 10.777 Dodecahedron “Medium Example” is “orange” with 30 edges of length 10.1 units.    surface area = 2,106.071 square units    volume = 7,895.319 cubic units    surface/volume ratio = 0.267 Dodecahedron “Large Example” is “silver” with 30 edges of length 200.5 units.    surface area = 829,963.459 square units    volume = 61,765,889.248 cubic units    surface/volume ratio = 0.013  —– Summary for Dodecahedron Test List —–Number of Dodecahedrons: 3Total Surface Area: 832,070.821Total Volume: 61,773,784.687Average Surface Area: 277,356.94Average Volume: 20,591,261.562Average Surface/Volume Ratio: 3.686 —-jGRASP: operation complete. </td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<table width="612">

 <tbody>

  <tr>

   <td width="42">Line #</td>

   <td width="570">Program output</td>

  </tr>

  <tr>

   <td width="42"> 12345678910111213 </td>

   <td width="570"> —-jGRASP exec: java DodecahedronListAppEnter file name: dodecahedron_data_0.txt Dodecahedron Empty Test List  —– Summary for Dodecahedron Empty Test List —–Number of Dodecahedrons: 0Total Surface Area: 0.0Total Volume: 0.0Average Surface Area: 0.0Average Volume: 0.0Average Surface/Volume Ratio: 0.0 —-jGRASP: operation complete. </td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong>Code</strong>:  Remember to import java.util.ArrayList, java.util.Scanner, and java.io.File, and java.io.IOException prior to the class declaration.  Your main method declaration should indicate that main throws IOException. After your program reads in the file name from the keyboard, it should read in the data file using a Scanner object that was created on a file using the file name entered by the user.

<h2>           … = <strong>new</strong> Scanner(<strong>new</strong> File(fileName));</h2>

You can assume that the first line in the data file is the name of the list, and then each set of three lines contains the data from which a Dodecahedron object can be created.  After the name of the list has been read and assigned to a local variable, a while loop should be used to read in the

Dodecahedron data.  The boolean expression for the while loop should be

(_________.hasNext()) where the blank is the name of the Scanner you created on the file.  Each iteration through the loop reads three lines.  As each of the lines is read from the file, the respective local variables for the Dodecahedron data items (label, color, and edge) should be assigned, after which the Dodecahedron object should be created and added to a local ArrayList of Dodecahedron objects.  The next iteration of the loop should then read the next set of three lines then create the next Dodecahedron object and add it to the local ArrayList of Dodecahedron objects, and so on.  After the file has been processed (i.e., when the loop terminates after the hasNext method returns false), name of the list and the ArrayList of Dodecahedron objects should be used to create a DodecahedronList object.  The list should be printed by printing a leading 
 and the DodecahedronList object.  Finally, the summary information is printed by printing a leading 
 and the value returned by the summaryInfo method invoked on the DodecahedronList object.




<strong>Test</strong>:  You should test your program minimally (1) by reading in the <em>dodecahedron_data_1.txt</em> input file, which should produce the first output above, and (2) by reading in the <em>dodecahedron_data_0.txt</em> input file, which should produce the second output above.  Although your program may not use all of the methods in DodecahedronList and Dodecahedron, you should ensure that all of your methods work according to the specification.  You can either user interactions in jGRASP or you can write another class and main method to exercise the methods.  Web-CAT will test all methods to determine your project grade.




<h3>General Notes</h3>

<ol>

 <li>All input from the keyboard and all output to the screen should done in the main method. Only one Scanner object on System.in should be created and this should be done in the main method. All printing (i.e., using the System.out.print and System.out.println methods) should be in the main method. Hence, none of your methods in the Dodecahedron class should do any input/output (I/O).</li>

</ol>




<ol start="2">

 <li>Be sure to download the test data files (<em>txt</em> and <em>dodecahedron_data_0.txt</em>) and store them in same folder as your source files. It may be useful examine the contents of the data files. Find the data files in the jGRASP Browse tab and then open each data file in jGRASP to see the items that your program will be reading from the file.  Be sure to close the data files without changing them.</li>

</ol>





