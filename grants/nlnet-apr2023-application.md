<!--
# (0) Context

 [ ] Situation of diagram for visual impairments
 [ ] Needs of diagram navigator
 [ ] Value of UML in Computing

Diagrams are graphic representations which can appear in all sorts of shapes and sizes. There are organisational charts, time-schedule analyses, decision trees, diagrammatic representations showing the working of the heart, or the chemical interaction between the various components of aspirin, or the influence of the money market on the stock exchange, or the structure of a computer programme – and so on. It is therefore not easy to give a comprehensive summary of the characteristics of a diagram. They have been very useful for express concepts and relationships between concepts, but the visual representation left blind people out of its scope and benefit.

On October 1st 2001 begun the Technical Drawings Understanding for the Blind (TeDUB) project ([https://web.archive.org/web/20051225200631/https://projects.fnb.nl/tedub/](https://web.archive.org/web/20051225200631/https://projects.fnb.nl/tedub/)), developing a system that will automatically generate descriptions of certain classes of graphics (electronic circuit diagrams, UML diagrams and architectural plans) and allow blind people to explore them independently. This system would have great potential in work, education and leisure domains to open up independent access to graphic material for blind people.

Despite the project it failed to deliver anything on this front, it defined a guideline ([https://web.archive.org/web/20051225200631/https://projects.fnb.nl/tedub/guidelines.zip](https://web.archive.org/web/20051225200631/https://projects.fnb.nl/tedub/guidelines.zip)) and did produce *Accessible UML*, a tool for helping blind people read software engineering UML diagrams.

*Accessible UML* is a tool to allow blind software engineers, students and screen-reader users to access UML diagrams produced by common UML tools ([https://www.alasdairking.me.uk/tedub/index.htm](https://www.alasdairking.me.uk/tedub/index.htm)). It supports UML Class diagrams, Use case diagrams, Sequence diagrams and State Chart diagrams exported from any tool producing XML XMI format ([https://en.wikipedia.org/wiki/XML\_Metadata\_Interchange](https://en.wikipedia.org/wiki/XML_Metadata_Interchange)), a format for UML diagram files that can be exported by tools like Rational Rose and Poseidon UML.
-->

# (1) Abstract
<!-- Can you explain the whole project and its expected outcome(s)-->
**TopoUML** is an HTML-generator porting of the former desktop software **Accessible UML**, conceived as a producer of a navigable web-based format of a UML diagram.

*Accessible UML* is a tool developed in the scope of the Technical Drawings Understanding for the Blind (TeDUB) project ([https://www.alasdairking.me.uk/tedub/index.htm](https://www.alasdairking.me.uk/tedub/index.htm)), to allow blind software engineers, students and screen-reader users to access UML diagrams produced by common UML tools. It supports UML Class diagrams, Use case diagrams, Sequence diagrams and State Chart diagrams exported from any tool producing XML XMI format ([https://en.wikipedia.org/wiki/XML\_Metadata\_Interchange](https://en.wikipedia.org/wiki/XML_Metadata_Interchange)).

**TopoMUL** is a software parser that uses an XMI file as input to produce a complete and accessible web representation of the UML diagram as an HTML file with javascript code and CSS rules included, allowing to recreate in a browser the main user experience that Accessible UML provides in a desktop environment.

Obs: I have the consent of the author of the Accessible UML tool (Mr. Alasdair King) to perform the porting and his statement that no patents were involved in its development.

# (2) Involvement
<!-- Have you been involved with projects or organisations relevant to this project before? And if so, can you tell us a bit about your contributions? -->

I have been involved in the design and development of accessibility improvements to the web interface of the Gitea software forge ([https://github.com/fsologureng?org=go-gitea&year\_list=1](https://github.com/fsologureng?org=go-gitea&year_list=1)) for the last few months, helping to prioritise Accessibility as a general concern in the design of the framework's web interface and as an important aspect to take into account at the time of coding. I have also contributed to improving the structure of the platform widgets and the semantic structure of the html layout, adding landmarks and other components to reduce the accessible barriers into the user interface ([https://blog.gitea.io/2023/03/gitea-1.19.0-is-released/#thank-you](https://blog.gitea.io/2023/03/gitea-1.19.0-is-released/#thank-you), [https://blog.gitea.io/2023/03/gitea-1.19.0-is-released/#-honorable-mentions-substantial-improvements](https://blog.gitea.io/2023/03/gitea-1.19.0-is-released/#-honorable-mentions-substantial-improvements)). 

I have extensive experience in web development and project management in my previous job ([https://web.archive.org/web/20190411152137/http://www.newtenberg.com:80/Acerca-de-NTG/91254:Felipe-Sologuren-Gutierrez](https://web.archive.org/web/20190411152137/http://www.newtenberg.com:80/Acerca-de-NTG/91254:Felipe-Sologuren-Gutierrez)), and in particular with Carola Ureta Marín's self-managed multimedia project ([https://www.carolaumarin.com/about](https://www.carolaumarin.com/about)) "La Ciudad Como Texto" (The City As Text) which she has carried out in collaboration with me as integral developer of the web medium [https://www.laciudadcomotexto.cl](https://www.laciudadcomotexto.cl).

# (3) Costs

<!--
Explain what the requested budget will be used for?
Does the project have other funding sources, both past and present?
(If you want, you can in addition attach a budget at the bottom of the form)

Explain costs for hardware, human labor (including rates used), travel cost to technical meetings, etc.
-->

The budget requested of 6,000 euros will be used exclusively in working hours for the time spent on the project. There are no other costs. The project has no other sources of funding and has not had them before because it is at an early stage.

This is my first application, so I am estimating 50€ per hour rate for 120 hours of work. The main plan is to port the user experience design from the Accessible UML tool to a standalone web application builder within the scope of the grant, including reverse engineering efforts, creating the test suite and deploying the test environment, with an estimated time of 100 hours. Next, the task is to produce integrations in software forges to improve the inclusion of diagrams in markdown texts with an accessible representation, with 20 hours of work estimated.
 
# (4) Compare

<!-- 
 Compare your own project with existing or historical efforts.

(e.g. what is new, more thorough or otherwise different)
-->
There are many serious initiatives intended to offer accessibility of UML diagrams, beginning with the Technical Drawings Understanding for the Blind (TeDUB) project ([https://web.archive.org/web/20051225200631/https://projects.fnb.nl/tedub/](https://web.archive.org/web/20051225200631/https://projects.fnb.nl/tedub/)). However, since then there is no Web App implemented with that goal in mind. The original tool developed under TeDUB, Accessible UML, was made for a Windows 2000+ environment, which leave people with devices made by Apple, \*nix based systems and handheld devices out of scope.

More recently, have appeared integrations for the Eclipse IDE as the TextUML Toolkit ([http://abstratt.github.io/textuml/](http://abstratt.github.io/textuml/)) which also can works as an IDE by itself, and the Cooperate Project ([https://www.cooperate-project.de/index.php/en/](https://www.cooperate-project.de/index.php/en/)) intended as a suite of UML tools and a text notation aiming to enhance the cooperation inside IT teams with visual impaired people. The main barrier in these solutions is the conception of a workflow environment based in the mentioned IDE, not opened to Internet as available software forge platforms for distributed development, and without ease to work in multidisciplinary teams or in educational contexts.

On the other hand, software forge platforms have an implicit solution under the assumption that the text notation of the UML diagrams are accessible files available in the code repository. This way, collaboration with visual impaired people is possible through the VCS or trough downloading from web directories of the code repository. In this context, tools as PlantUML has been integrated in Gitea ([https://docs.gitea.io/en-us/customizing-gitea/#example-plantuml](https://docs.gitea.io/en-us/customizing-gitea/#example-plantuml)), GitLab ([https://docs.gitlab.com/ee/administration/integration/plantuml.html](https://docs.gitlab.com/ee/administration/integration/plantuml.html)) and Github ([https://github.com/marketplace/actions/generate-plantuml](https://github.com/marketplace/actions/generate-plantuml)) in order to provide images from such text notations as part of the generated output from the Markdown format sources, whether as part of documentation or as elements to the technical discussion in issues or pull request trackers. Unfortunately, the output provided is not accessible for web visitors, leaving visual impaired people and the own blind collaborators without access to those outputs. PlantUML also provides a HTML output format in multiple files, but limited to UML class diagrams.

Doxygen ([https://www.doxygen.nl/manual/diagrams.html](https://www.doxygen.nl/manual/diagrams.html)) also provides a way to obtain web diagrams built from the code structure, but the HTML resultant is totally inaccessible.

Draw.io ([https://github.com/jgraph/drawio](https://github.com/jgraph/drawio)), which is a Web App, doesn’t provide accessibility in its web interface, despite its powerful diagram editor.

With better accessibility features, MermaidJS ([https://mermaid.js.org/config/accessibility.html](https://mermaid.js.org/config/accessibility.html)) integrates well with the most known software forge platforms ([https://mermaid.js.org/ecosystem/integrations.html](https://mermaid.js.org/ecosystem/integrations.html)). However, the ARIA attributes available are not intended to provide an automatic textual notation of the source diagram as an alternative text, leaving the accessibility of the output as an editorial concern, which is not optimal.

TopoUML, as a portation of Accessible UML, will provide a self-contained Web App using ARIA best practices with a broader range of uses, allowing multidisciplinary cooperation and better automatic-generated accessible documentation outputs. This will improve accessibility for this type of content in software forge platforms, but also in web sites with UML content as Wikipedia, if would be adopted.

Educational environments, both technical and regular, also would be beneficiaries of TopoUML because the approach produce independence of the operating system and the screen reader used.

# (5) Challenges
<!--
What are significant technical challenges you expect to solve during the project, if any?)
-->
The main technical challenge of TopoUML is to replicate the user experience of exploring a UML diagram as Accessible UML does in an accessible Web App environment.
     * Support UML Class Diagrams, Use Case Diagrams, Sequence Diagrams and State Diagrams formatted as an XMI file.
     * Reproduce the 6 levels of navigation through the fields provided by Accessible UML, which will give information about the current node, connections, annotations, node information, connection information and connected nodes that can be browsed and switched between the different fields by pressing a set of keys.
     * Make the web interface WCGA 2.1 level AAA compliant.
     * Provide a test suite with samples obtained with PlantUML's XMI export functionality or through the collection of openly licensed content on the Internet.
* Develop a set of integration code to software forging platforms to provide an alternative experience to the embedded UML diagrams included as UML textual notation in Markdown sources.
   Joystick and "Save As" functionality will not be ported. Bookmark nodes will not be implemented in this phase.

On the other hand, the main social challenge is to achieve a reasonable amount of adoption of TopoUml. However, in the ecosystem of software forging platforms there is a growing interest in providing better accessibility to the tools associated with the development workflow. Furthermore, TopoUML does not need to be a replacement, but a complement to an existing functionality, which should facilitate its adoption.

# (6) Ecosystem
<!--
Describe the ecosystem of the project, and how you will engage with relevant actors and promote the outcomes?
(E.g. which actors will you involve? Who should run or deploy your solution to make it a success?)
-->
Many software forges have solutions to render diagrams as part of the parsing process of plain text UML notation included in markdown files for the web user view. PlantUML or MermaidJS have integrations as extensions or plugins to this platforms. **TopoUML** could be easily integrated in the same way to this platforms in order to enhance inclusion for blind contributors and general readers. Starting with Gitea and taking advantage of the gained confidence with their developers, the integration will be well promoted to administrators of those instances. Integration in Github and GitLab should be straightforward with the success of this first experience, but taking contact with their accessibility teams has been considered.

Another good space to provide inclusion of this new form of diagram representation is in the MediaWiki ecosystem as a complement of an existent diagram extension ([https://www.mediawiki.org/wiki/Extension:Diagrams](https://www.mediawiki.org/wiki/Extension:Diagrams)). With a simple solution like this complementing the visual representations of UML diagrams based on PlantUML notation, including an alternative file to the output, the potential of enhanced access of visual impaired readers and future engagement with the solution is envisioned.

Additionally, I know particular blind persons whom can be contacted in a feedback phase of the project. One of them is a software engineer. This kind of engagement will be explored and extended to produce improvement and diffusion of the tool.
