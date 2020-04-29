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

Above is an example of a Nodes sheet. The only required column is the Id column, as it is used for the Edges sheet, but it is highly recommended if you are going to be creating texts about it to add more context through the Label column.

This is an example of the character interactions sheet before it is turned into the Edges sheet below.

* First off, create your Nodes sheet. Feel free to add more columns, such as a general description of the characters, or events, or whatever you decide to make your nodes. Once imported to Gephi, this will be used to create information in regards to the Nodes.

* Following that, save this sheet as a .csv file and give it a descriptive name such as Brothers_Nodes.

* Next, create a new sheet. This shall be your character interactions sheet. Go through the text you are converting and make sure to record the character interactions. The example that we are doing is only the basic character interactions, IE whether or not the characters interact. However, feel free to make notes on how many lines are said, what lines are said, so on and so forth.

* Next up is the Edges sheet. Copy and paste the character interactions into a blank sheet, where you will then convert the characters into their unique Ids from the Nodes sheet. You can do this through using the ‘Replace’ function from using the keys Ctrl + H. Next add two more columns and title them Type and Weight. 

As we are only doing base character interactions, you can simply fill out Type with ‘undirected’ and Weight with ‘1’. However, if you wanted to go more in depth with whether or not a character is speaking to, or being spoken at, you can change around the Type to ‘directed’. Or if you wanted to, for example, include how many lines are spoken in the interaction, you can change the Weight (this will enable you to view how many lines are said in between two characters). When imported into Gephi, this sheet will be used to create connections between the Ids for the Nodes created via the Nodes .csv file.

* Finally, save your Edges sheet as a .csv file and make sure to give it a descriptive name.


### Second Header

Content

### Etc.
 
 
 
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
