Editing the DarlBot Tree
================
The heart of DarlBot is represented as a tree. The tree contains nodes each representing a word to be found in the incoming text, a variable to be captured, or other symbols that can match multiple words by meaning.
To Edit the tree is to edit the selected version of the bot, which may not be the one presented to users.

# Panels

## Left Panel
On the left is a tree representation of the knowledge of the bot.

### Selection
if you select a particular node, any associated rules and implications are shown in the right panel.

### Icons
Tree and leaf symbols are used to represent internal and terminal nodes respectively. Terminal nodes more often have rules associated with them.

### Editing
Right button clicking on a node will bring up a menu permitting creation of a new node, deletion of a node, copying and pasting of nodes.

### Search
Typing in a sequence of words in the search box will cause the tree to show just those nodes that match the words.

### Node text
The text holds the element to be matched. this can be:

#### Literal word
In this case only this word exactly as written will be matched, case insensitive
#### Value
Any value that matches the type described  will be captured, potentially for use in logical processing.
#### Default
At any point on the tree, including the root, default values can be set. Defaults are always leaf nodes. Defaults are executed when no better match exists. So a default at the root represents the response if no other match acn be found in the entire tree, whereas a default in another part of the tree represents a response to be given when the parent nodes have been matched.
#### Thesaurus match
Copying a thesaurus index from the thesaurus tree into the node text will result in a match with any word that matches that thesaurus entry and any below that entry in the thesaurus tree. 

### Cutting, copying and pasting
Nodes can be cut, copied and pasted onto other sections of the tree. In both cases the selected node and all children will be copied over. 

### Deleting
Selecting a node and deleting it with a right button selection will also delete all sub nodes.

### Node creation
Creating a node with a right button click and selection will create a new node with the text "New node".

### Rename
Nodes can be renamed with literal text, or text copied from the Thesaurus tree.

##Right Panel
The right panel contains details of the selected node.
The top line contains the path of the selected node.
###Darl editor
Next down is the interactive DARL editor that permits editing of the rule fragments associated with that node.
DARL has the characteristic that rules may be freely mixed in any order. When a terminal node is reached during parsing of an incoming text, the set of rules from all the parent nodes are assembled and executed along with the current nodes rules.
###implications
Implications are thesaurus indexes that serve as inference aides for resolving results. For instance a node containing "who" might have the thesaurus index for "person" associated, because the response must involve a person. 
### Add symbols
This brings up the Thesaurus pop-up which enables the users to add symbols to the tree or implications.
### Save attributes
This saves the current edit of the attributes to the model. Note that the model must be saved to the store for this change to become permanent.

## Thesaurus pop-up
This shows the set of possible thesaurus entries arranged as a heirarchy.
### Search box
Restricts the tree to thesaurus indexes matching the given word.
### +
Adds the selected index at the selection point in the main tree. Closes the pop-up.
### v 
Replaces the main tree's selected node's text with the selected thesaurus index.Closes the pop-up.
### x
Closes the pop-up.
