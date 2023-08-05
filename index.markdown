---
layout: default
---

## Design Framework

Our design framework represents the three main components of generation pipelines---<b>input, model, outputs</b>---into three iteractive objects---<b style="color:{{site.syscolor}}">cells, generators, and lenses</b>. By modularizing the components into these objects, writing interfaces can enable end-users to <b>(1)</b> maintain multiple <b>versions</b> of the generation components, <b>(2)</b> use each object as a <b>testing</b> sandbox for different sub-configurations, and <b>(3)</b> <b>compose</b> these objects into new and parallel configurations.

{: .sys-img}
![The teaser figure for the framework. Three headers are shown: Input, Model, and Output. Underneath each header there are diagrams depicting the Cells, Generators, and Lenses, respectively. Underneath Cells, dots that represent cells are shown. These dots are linked and one path of dots is highlighted with text for that path also displayed underneath the path. Underneath Model, rectangles that represent generators are displayed and these generators are connected with lines to the dots. One generator is highlighted with information about the model underneath it (i.e., GPT-4 model and its parameters). Underneath Lenses, three summarized representations of lenses are displayed: a list lens that shows generations as a list of text, a ratings lens that show ratings in bars, and a space lens that shows the generations as dots in a 2D space. These lenses are linked to the generators with lines.](/assets/img/teaser.png)

### Cells

{: .img-left}
![Abstract representation of cell objects and their interactions. An abstract representation of a text editor is shown where the last part of the text is highlighted. This highlighted part is connected to a tree of dots, where each dot represents a cell and they are connected with lines to show their ordering. One branch out of the tree is labelled with "create" to show how cells can be created. Also, a branch that is connected coming out of the tree is shown with an arrow labeled "assemble" to show how cells can be assembled together into bigger ensembles. There is an arrow going between the two bottom branches of the tree it is labelled "copy" to show that cells can be copied. Next to the tree another abstract representation of the highlighted text is shown where parts are now highlighted in a different color and it is labelled "modify".](/assets/img/cells.png)

{: .text-right}
<b style="color: {{site.syscolor}}">Cells</b> are object representations of discrete input units. For example, a line of a prompt, an example in a prompt, a sentence of a story, a keyword, etc. An interface that supports cells can enable end-users to <b>create</b> multiple cells to maintian multiple input variatiosn to test, and <b>assemble</b> cells into comprehensive inputs for an LLM.

### Generators

{: .img-left}
![Image shows several tree of cells or dots that represent different ensembles of cells. There are lines connecting the trees to three rectangles that are labelled "Generators". One of these lines is labelled with an arrow that says "link". The top rectangle is connected to another rectangle that shows a slider labelled "parameter" and an arrow going left-to-right labelled "modify". The middle rectangle is connected to another rectangle that contains a row with "parameter" and an arrow going up, a row labelled "generations" and showing three abstract representations of text, and another row labelled "parameter" with an arrow going down. There is an arrow going down next to this rectangle that says "track".The bottom rectangles is more transparent and is labelled with "create".](/assets/img/generators.png)

{: .text-right}
<b style="color: {{site.syscolor}}">Generators</b> are object representations of model settings (i.e., type of LLM and parameter values). By supporting generators, interfaces can allow end-users to <b>maintain</b> multiple parameter settings, and flexibly <b>link</b> these with different inputs according to their present needs.

### Lenses

{: .img-left}
![Image displays three rectangles (the middle one in a different color) that represent generators and are connected to two containers that are labelled "lens". There is an arrow between the middle generator and the top lens that is labelled "link". The top container shows dots spread out in two different colors that represent the top generator and middle generator. The bottom generator is connected to the bottom container which shows two boxes positioned vertically with abstract representations of text. This bottom container is linked to another container that contains rating bars and there is an arrow between these two that is labelled "assemble".](/assets/img/lenses.png)

{: .text-right}
<b style="color: {{site.syscolor}}">Lenses</b> are object representations of spaces that represent and visualize the generations produced. For example, these can include a list, a gallery, or a real-time confidence visualization. An interface can provide end-users with diverse lenses to support <b>navigation</b> of generated outputs based on personal, changing needs and goals.

------

## Example Interfaces

With this framework, we designed and developed three interfaces to demonstrate how the proposed interactive objects can support writing with LLMs.

### Copywriting Interface

![The copywriting interface which is partitioned in four components. The top-left components shows text boxes aligned according to lines, where the are multiple text boxes per line and only one in each line is highlighted.. The bottom-left component shows four buttons that represent generators where each generator shows the four parameters but with different values. There is also a button below these generators with a "+" mark. The bottom-right component shows two containers: one contains a list of text, and the other contains radial rating indicators. The top-right component shows a text editor. Next to the screenshot of the copywriting interface, we can see multiple sub-components. The first sub-component shows a generators where the temperature parameter has been clicked to reveal a control panel that shows the current temperature value and a slider to change the value. The second sub-component shows a generator where its history of changes is displayed. The history shows previous temperature changes and outputs that the generators has produced. The final sub-component shows the space and rating lens.](/assets/img/copywriting.png)

In our <b>copywriting interface</b>, end-users can create and maintain alternative specifications for their desired advertisement as cells, and then assemble these into new combinations. The interface allows end-users to create multiple generators to test diverse parameter settings and to use various lenses to explore generated advertisements based on their content, similarity, sentiment and/or emotion.

### Email Composing Interface

![The email composing interface, which is split into two parts. On the left, there is a text editor that shows one portion of text highlighted in blue (the selected text) and the following portion of the text in blue (the generated text). Hovering over the text editor, there is a square container that shows a graph with two axes, anger and sadness, and dots. On the right of the interface, there is two pipeline buttons that are labelled "C" and "A". The settings for the "C" button are open which shows four text containers: (1) "Change sentences to be more polite and friendly", (2) "Whole email: [Whole text]", (3) "Original sentence: [Selection]", and (4) "Changed sentence: [Output]". Next to this input, there is the Model container that contains two generators with different colors. Next to that, there is the output container that presents three buttons represented by icons for the list lens, axis lens, and space lens. Under these buttons, there are two dropdown menus for the horizontal and vertical axis settings.](/assets/img/email.png)

Our <b>email composing</b> interface packages cells, generators, and lenses into <b>"brushes"</b> that allow end-users to select text and perform their own desired generative functions on the selected text. For each brush, the end-users can assemble cells to specifcy the brush's purpose, set multiple generators to perform the function with various parameter settings, and explore outputs in their preferred way by choosing a lens for the brush. 

### Storywriting Interface

![The story writing interface which is split into four parts. The left-most part is a text editor. The second left-most part shows a tree representation where each node is represented as a block where each block contains a keyword. Also, there are lines connecting these dots. Only one path in this tree is selected (all the dots are filled with color) while the other dots are unfilled. The second right-most column shows several generators that are connected to different lenses in the right-most column. In the right-most column there are three lenses: a list lens that shows a list of text, a space lens that shows three dots in a 2D space, and finally a peek lens which shows a piece of text where certain sentences are invisible or more transparent.](/assets/img/storywriting.png)

Our <b>story writing interface</b> partitions the end-user's story into cells and arranges them into a tree, which enable writers to assemble cells into <b>branching and parallel plotlines</b> for their story. In this interface, end-users can experiment with and compare configurations by linking cells to multiple generators and linking multiple generators to the same lens.

------

## Bibtex
<pre>
@inproceedings{kim2023cells,
  author = {Kim, Tae Soo and Lee, Yoonjoo and Chang, Minsuk and Kim, Juho},
  title = {Cells, Generators, and Lenses: Design Framework for Object-Oriented Interaction with Large Language Models},
  year = {2023},
  isbn = {9798400701320},
  publisher = {Association for Computing Machinery},
  address = {New York, NY, USA},
  url = {https://doi.org/10.1145/3586183.3606833},
  doi = {979-8-4007-0132-0/23/10},
  booktitle = {The 36th Annual ACM Symposium on User Interface Software and Technology (UIST '23), October 29-November 1, 2023, San Francisco, CA, USA},
  numpages = {18},
  location = {San Francisco, CA, USA},
  series = {UIST '23}
}
</pre>

------

{: .logos}
[![Logo of KIXLAB](/assets/img/kixlab_logo.png)](https://kixlab.org)
[![Logo of KAIST](/assets/img/kaist_logo.png)](https://kaist.ac.kr)

{: .center .acknowledgement}
This research was supported by the **KAIST-NAVER Hypercreative AI Center**.


[1]:{{site.code}}
[2]:{{site.paper}}
