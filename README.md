![Gephi Logo][imglogo]


# Introduction
Gephi is a free and open-source platform for data visualization and exploration. It allows for interactions and analysis of graph data, and includes the enabling of various tools such as shaping, colouring and manipulation of structures so that one can easier see the patterns within. According to the developers, the platform can be used for: exploratory data analysis, link analysis, social network analysis, biological network analysis, and poster creation. 

The purpose of this tutorial is to teach you to be able to utilize Gephi to visualize various aspects of texts. This tutorial will be teaching you first to create a dataset, second to import it into Gephi, and finally, how to do some basic manipulations. The text used in the samples for the creation and importing of the dataset will be an ancient comedy by Terence called The Brothers, the translation used will be the one in Terence: The Comedies translated by Peter Brown.

Definitions:
Nodes: Vertices of a graph, these represent specific objects. Examples: events or characters.
Edges: Links in between nodes of a graph. Examples: character interactions, events, or themes. 



NOTE: There are several sample datasets on the Gephi wiki [here](https://github.com/gephi/gephi/wiki/Datasets).

### Step One: Detailing the Data
* Select the text that you will be creating data from.

* Decide what sort of data you want to create a visualization of. Do you want to just see basic character interactions? Do you want to see how many lines each character has? Do you want it to be directed, undirected, or mixed (i.e. both directed and undirected)? These are all questions that will affect how you go about creating your dataset(s).

* Open up a spreadsheet program such as Excel or Google Sheets. You will be creating two (or three) separate sheets, one for the Nodes, one for the character interactions that you will turn into one for the Edges.

![1][1]
 
Above is an example of a Nodes sheet. The only required column is the Id column, as it is used for the Edges sheet, but it is highly recommended if you are going to be creating texts about it to add more context through the Label column.

![2][2]
 
This is an example of the character interactions sheet before it is turned into the Edges sheet below.

![3][3]

* First off, create your Nodes sheet. Feel free to add more columns, such as a general description of the characters, or events, or whatever you decide to make your nodes. Once imported to Gephi, this will be used to create information in regards to the Nodes.

![4][4]

* Following that, save this sheet as a .csv file and give it a descriptive name such as Brothers_Nodes.

* Next, create a new sheet. This shall be your character interactions sheet. Go through the text you are converting and make sure to record the character interactions. The example that we are doing is only the basic character interactions, IE whether or not the characters interact. However, feel free to make notes on how many lines are said, what lines are said, so on and so forth.

* Next up is the Edges sheet. Copy and paste the character interactions into a blank sheet, where you will then convert the characters into their unique Ids from the Nodes sheet. You can do this through using the ‘Replace’ function from using the keys Ctrl + H. Next add two more columns and title them Type and Weight.

![5][5]
 
As we are only doing base character interactions, you can simply fill out Type with ‘undirected’ and Weight with ‘1’. However, if you wanted to go more in depth with whether or not a character is speaking to, or being spoken at, you can change around the Type to ‘directed’. Or if you wanted to, for example, include how many lines are spoken in the interaction, you can change the Weight (this will enable you to view how many lines are said in between two characters). When imported into Gephi, this sheet will be used to create connections between the Ids for the Nodes created via the Nodes .csv file.

* Finally, save your Edges sheet as a .csv file and make sure to give it a descriptive name.


### Importing the Data into Gephi
* Open up Gephi, and create a new project. Next, click on the button near the top that says “Data Laboratory and then click on “Import Spreadsheet” which is under the “Data Table” tab.

![6][6]

* We’re going to import the Nodes csv file first, so navigate to the appropriate folder and click the Nodes file when prompted. The next pop-up should look something like this:

![7][7]

Ascertain that the drop down tabs in your screen match the one above (especially the ‘Import as:’ one), and then click ‘Next’. In the next page, you may specify which columns you would like to import; the other setting ‘Time Representation’ will not be used in this tutorial. Click ‘Finish’ and then when prompted in the new window, have the Nodes imported to the existing workspace if your current workspace is empty (or a new workspace if your current workspace is not empty). This window will also tell you your number of Nodes/Edges, and you can specify whether or not you would like the graph type to be directed, undirected or mixed (a combination of directed and undirected) via a dropdown tab. Click ‘Ok’ once you have read over and made certain that the information is accurate and you will see a table of your Nodes.

* Next, we are going to be importing your Edges csv file. First click ‘Import Spreadsheet’ again, and then when prompted, select your Edges file. Now, go to your ‘Import as:’ drop down tab, and select the ‘Edges table’ option.

![8][8]

Click next, and select which columns you wish to import on the next page. The ‘Source’ and ‘Target’ columns are required, but aside from that, you can choose with other columns you wish to see. Click ‘Finish’ and you should be prompted to decide whether or not you want the Edges to be put in a new workspace, or the one that you just created for your Nodes. Select the ‘Append to existing workspace’ option, which will add the Edges sheet to the Nodes sheet.

* Now click on the ‘Overview’ tab at the top to view your rudimentary Gephi graph.


### Using Gephi
* Basics of using Gephi
- To zoom in and out, use your mouse wheel
- To pan throughout your graph, use right mouse click and drag to where you want to see

![9][9]

- The magnifier glass in the photo above will recenter the image on your graph, the grey box below the magnifier glass will reset the colours of the nodes and edges of the graph, the icon with an A above a red line will reset the graph’s text colours, and the A below that will reset whether or not the text is visible.
- From left to right of the bottom icons: the lightbulb will change the background colour and the camera will take a screenshot. The T will determine whether or not the nodes’ labels are shown, the first diagonal line will be to show or not to show the edges, the second diagonal line will be whether or not the edges will have the source node’s (IE the node that they originate from) colour, the white T will be to show the label of the edges and the first slider will be the proportionate size of the edges. The next two A’s are size mode and colour mode respectively, the next button determines the font and original size of the text, the second slider determines the proportionate size of the text, and the solid black button is the colour of the text.

![10][10]

- The photo above is the window that prompts upon clicking the clipboard button beside the text colour button. This allows you to decide which labels you would like the Graph to display from your spreadsheet that you had created earlier. This can be done for both nodes and edges.

* Back to the graph, it should be looking a little disorganized and hard to read. To fix this, we will apply a layout from the Layout tab on the bottom left (if you cannot find one, go to the top bar and click on the Window dropdown tab, and from there click on the Layout button [this can be applied to many tabs, in case you cannot find them]). Select the ‘Force Atlas’ selection from the dropdown tab and then click ‘Run’. Force Atlas will essentially pull together the nodes that are connected via edges and repel the nodes that are not connected. This should cluster your nodes and edges together, but make it hard to read because of how clustered they are. Change the ‘Repulsion strength’ selection from 200 to 10000 and edit it until you have found an acceptable looking graph. Click the ‘Run’ button again, although it will now be changed to a ‘Stop’ button.

**NOTE: You can click and drag Nodes to various places on your graph.**

* Another tab that you’re likely going to want to see is your Data Table. This will allow you to see a smaller version of the Data Laboratory, which keeps all of the data (including some that you will be finding yourself during this tutorial) that the program has on your nodes and edges.

* Now we are going to start making it pretty using the Appearance tab (pictured below).

![11][11]

The appearance of both nodes and edges can be changed with this tab. We’re going to be making the colour of the nodes change based on the degree of the nodes (or how many nodes one is connected to). Click the ‘Ranking’ tab, which will bring up a dropdown tab that will allow you to choose what you want to change the colour based on (you can also change the size of the nodes, colour of the text and size of the text by choosing between the images in the same row as the ‘Nodes’ and ‘Edges’ tabs). Choose the ‘Degree’ option from the ‘---Choose an attribute’ tab. This should change the ‘Ranking’ tab to show a colour slider. The slider goes from left to right, least to greatest amount. You may choose preset colour palettes from the little icon beside the slider, or you can add colours (click on an empty space on the slider) and alter colours (double click on the little arrows on the slider) yourself. Once you have decided on your colour palette, click ‘Apply’ to see the colours change to reflect their degrees.

**NOTE: If you wish to see the degrees in the Data Table, go to the Statistics window (it should be on the right side of the screen) and Run the ‘Average Degree’ program. This should give you a window that will provide you with details regarding the Degree Distribution and place the ‘Degree’ column on your Data Table, where you may view the statistics at your leisure.**

* Another thing that we can do with Gephi is use the Statistics panel to do calculations for us regarding the graph. For example, under the ‘Edge Overview’, you can find the ‘Average Path Length’ calculation. This will tell you information about how central a node (in this case, a character) is. Click ‘Run’ to view the average number of edges between Nodes. This will create a window that lets you decide if you want the calculator to run it as if it’s an undirected graph, or a directed graph (only available if the graph was defined as mixed or directed when created). Choose which type of path length you would like, and then press ‘Ok’. Next, you should see a ‘Graph Distance Report’, where all of the statistics generated will be. You can view this at any point by pressing the little question mark icon beside the ‘Run’ button in the ‘Average Path Length’ row. Now we have three new calculations added to the Data Table and Data Laboratory. To view them at work (and see how often a node will appear on paths between nodes), let’s try colouring the nodes based on their Betweenness Centrality. To do this, head back over to the Appearance tab and select ‘Betweenness Centrality’ from the dropdown menu in the Rankings. Press ‘Apply’ to view the new information on the graph.

* Now let’s change the size of Nodes based on their degree. Press the icon with multiple circles of different sizes in the ‘Nodes’ and ‘Edges’ row, this will allow you to change the sizes of nodes based on calculations.

![12][12]

Select ‘Degree’ from the dropdown menu, decide the minimum and maximum sizes of the nodes, and then press ‘Apply’ for your Nodes to be resized.

**NOTE: If there are overlapping nodes, you may go back to the Layout tab and select ‘Adjust by Sizes’ to remove the overlapping.**

* Now, we are going to be viewing communities of nodes. This means that we will be colorizing clusters of nodes based on which other nodes they interact with. Going back to the Statistics panel, under the ‘Network Overview’ section, run the ‘Modularity’ calculation. Now go back to the Appearance panel, and select the ‘Partition’ tab. Select ‘Modularity Class’ from the dropdown menu. The following chart will allow you to view the number of communities and how large they are. You can also generate a Palette through the ‘Palette’ link. Select ‘Apply’ when you wish to view the new version of the graph.

* You can also filter out various attributes, objects, edges, etc. To filter out nodes for example, go to the Filters panel that should be beside the Statistics one. Select Filters to view it. Say that we would like to filter out nodes that only have one edge connected to them. We would go to ‘Topology’ and drag ‘Degree Range’ from the list down to ‘Drag filter here’, which is under ‘Queries’.

![13][13]

From there, you can use the slider at the bottom of the panel to adjust the amount of nodes viewed based on their edges.

* We are done with the manipulation for now, so let’s go over to Preview Panel, which would be up at the top.

![14][14]

To view the graph’s most recent manipulations, select the ‘Refresh’ button down at the bottom.

![15][15]

‘Preview ratio’ allows you to view a partial graph.

* From here, you can make the graph look even prettier and presentable. Play around with the settings to make it look the way that you would like.

**NOTE: Curved edges do not show arrows to display direction of graph. To turn these off, go down to the ‘Edges’ selection under Settings, and turn off the ‘Curved’ option.**

* To export, select the button down at the bottom, under ‘Preview ratio’ and beside ‘Refresh’. This will allow you to export it to a SVG, PDF, or PNG file.

**NOTE: SVG files can be edited further in programs such as Inkscape and Adobe Illustrator.**

Make sure to save your project, and thank you for reading!

 
 
![DSL Logo][dsllogo]  
  
**This tutorial is brought to you by the Brock University Digital Scholarship Lab.  For more information on the DSL check out our website at [www.brocku.ca/library/dsl/](https://brocku.ca/library/dsl/) or you can e-mail us at dsl@brocku.ca.**  
  
You can also find us on:  
[Facebook](https://www.facebook.com/Brock-University-Digital-Scholarship-Lab-349407235866792/)  
[Twitter](https://twitter.com/brock_dsl)  
[Instagram](https://www.instagram.com/brock_dsl/?hl=en)  
[YouTube](https://www.youtube.com/channel/UC2eEqPkDo-1N3qilxv-N_1g/featured?view_as=subscriber)










<!--- Please use reference style images so that it is easier to update pictures later --->

[dsllogo]: dsl_logo.png
[imglogo]: Gephi_Logo.png
[1]: s_1.png
[2]: s_2.png
[3]: s_3.png
[4]: s_4.png
[5]: s_5.png
[6]: s_6.jpg
[7]: s_7.jpg
[8]: s_8.jpg
[9]: s_9.png
[10]: s_10.png
[11]: s_11.png
[12]: s_12.png
[13]: s_13.png
[14]: s_14.png
[15]: s_15.png
