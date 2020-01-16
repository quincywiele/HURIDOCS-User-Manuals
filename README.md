# HURIDOCS-User-Manuals
Uwazi Guide Manual information
Uwazi User Guide 2.0
##Introduction to Uwazi
To manage records and documents, most organizations today use folders or categories on platforms like DropBox, One Drive and Google Drive so that staff can access them later.  Although safe and effective, these platforms simply provide a safe space for these documents and provide no connections or analysis.
What if organising documents could make their contents come alive? Uwazi goes beyond tags and filenames to organise your documents. Each document can be critical is telling a story: an email that asks for a favor from a politician, a testimony from a witness of police violence, the ruling of a court on a human rights case. When these stories are connected by the platform, the bigger picture of patterns and systems becomes clearer: ongoing corruption, systematic police violence, legal human rights precedence and abuse of power.
Uwazi is built to do exactly this – highlight and organise the important information in each document, and create relationships between documents. Uwazi illuminates the bigger picture that human rights document collections uncover.
##What problems does Uwazi solve?
Most document management systems organise contents based on a document’s metadata such as author, department, person, event, or year.
However, for human rights organisations, a document is often much more than these basic descriptors assigned to it . The content within the document also provides important insight.
Uwazi addresses these problems by putting content and connections at the heart of the platform. Within each document there is important information to highlight, tag, organise, reference, and connect to other documents. In Uwazi, one paragraph referencing a military commander responsible for a human rights violation can be connected to another paragraph in another document that provides more biographical information about the same person.
##Who is it for?
Uwazi was designed to address the needs of human rights organisations. Human rights NGOs, National Human Rights Institutions, Universities, Journalists, Courts, and others working with large document collections can also benefit from Uwazi’s user friendly features.
More information: https://www.uwazi.io/
##History of Uwazi
In 2010, HURIDOCS partnered with the Institute for Human Rights and Development in Africa (IHRDA) to develop the African Case Law Analyser. This website greatly improves access to human rights case law of African human rights regional bodies. The African Case Law Analyser addressed an enormous problem that we see in many regions – that access to human rights jurisprudence is almost impossible to obtain, hindering the work of human rights defenders, journalists and lawyers. In 2017, HURIDOCS and the Center for Justice and International Law (CEJIL)  launched SUMMA - a Case Law Analyser for the Americas, to provide access to the Inter-American Court and Commission cases.
After building two Case Law Analysers, HURIDOCS decided to invest in building an open source platform to allow any human rights project to organise and publish its own document collections. Through consultations with human rights organisations, we learned that document collections are not helpful unless they can be connected to a bigger narrative: case documents need to be connected to judgement documents, judgement documents needs to be connected to judges, and so on. All of this information needs to be organised, in order to be understood. HURIDOCS built Uwazi to address these needs.
We continue to develop new features in response to feedback from our users. Currently, we are working to support human rights investigations managing large amounts of source documents and media to advance transitional justice efforts and evidence-based advocacy, all while meeting the pressing security needs of human rights organisations.
Significant funding for Uwazi development has been provided by the MacArthur Foundation and the Center for Justice and International Law (CEJIL).
##Glossary of terms
Document - in a Uwazi, a document is a PDF with properties, is filterable and able to have connections
Entity - something that has properties, is filterable and able to have connections, but is not a PDF (for example, a court, case, person, or event)
Thesauri - a list of items that you want to refer to throughout the platform (in a property)
Properties - descriptive attributes that are assigned to documents or entities
Connections - a simple field that connects documents or entities to each other with a label
Reference - a bookmark that connects selected content in the same document, other selected content in another document , an entire document or an entity
Build Your Information Architecture
Create templates
Templates are the foundation of your Uwazi platform as they allow you to attribute consistent, structured metadata to your documents and entities. Within each template, you can assign a variety of properties like:

 -Text

 -Numerics

 -Select (needs thesaurus)

 -Multi-select (needs thesaurus)

 -Date, date range, multi date, multi date range

 -Rich text

 -Geo-location

 -External links

 -Media (for video and audio embedding or self hosting)

 -Relationship - allow you to use items from another template as thesaurus items

##To create a template:

1.Click on “settings”
2.Click on Templates in the Metadata section
3.Click “add templates”
.
4.There will be two default properties: Title and Date Added.
.
5.Add new properties by dragging and dropping them into the designated area.
6.Give the template a name.
7.Click Save.
Note:
In case the instance is planned to be in Arabic by default, the template and properties should be created in latin characters then translated into Arabic, otherwise it is going to trigger a bug. Developers are working to fix it.
When you add a select or multi-select property to a type, you will see a field titled Thesauri in which you can select a Thesaurus or a Template that you have already created. See the section on create thesauri for more information on how to create these thesauri.

##Create thesauri
A thesaurus in Uwazi is a list of terms that you have referenced as properties when creating your entity types.
E.g: You may want to create a thesaurus for countries so you can refer to this list when you add the country property to your document template.  Using thesauri will make data entry and retrieval more precise, coherent and easy.
You can use the same thesauri across the templates by calling a thesaurus from a property, thus creating connections between different types of information by a common property.
###To create a thesaurus;
1.Click on “settings”
2.click on “thesauri” under the Metadata section
3.click on “add thesaurus
4.write the name of the thesaurus; e.g. Type of testimony
5.Add some items to this thesauri like “testimony of victims” “testimony of family” etc.
6.click ‘save’ when finished.
###Nested options in thesauri
For big thesauri, grouping values in groups makes information more accessible. In the thesauri creation interface, there is a "Create group" at the bottom action buttons and some controls to move items around:
Which gets render as a filter:
##Name connections
Connections in Uwazi link two pieces of information in your collection. It could link a paragraph in one document to a separate document or a word to an entity.
To name your connections;
1.Click “settings”
2.Click on “relationship types”
3.Name connections here. Once you have named them,you can begin to create connections
**Create an entity **
Now you’re ready to start configuring Uwazi to organise your information!
The first thing to do is create an entity template. Templates serve as “containers” for your information and they are based on your data model.
** To create a template**;
click on settings
Click on ‘templates’ under the Metadata section
click on “add template”
Each template needs “properties.” These properties represent a type of metadata that you want to capture and potentially analyse.
There are 15 different properties for you to select from.
To see more information on creating a template, please visit: https://github.com/huridocs/uwazi/wiki/Create-templates
Importing thesauri to Uwazi from CSV files
This feature allows you to import terminology lists in different languages from a CSV file into an Uwazi thesaurus. You can import data into a new or existing thesaurus.
Preparing the CSV file
The CSV file should have a separate column for each language you want to import, the language should be used as the name of the column. Each row contains a term and its translations in different languages.
Here's a sample CSV file viewed as plain text:
English,French,German
Man,Homme,Mann
Woman,Femme,Frau
Child,Enfant,Kind
Here's the same file viewed in a spreadsheet program:
| man | homme |Mann
| ------ | ------ |
| Woman | Femme |Frau
| Child | Enfant |Kind
Importing data into an existing thesaurus
To import data from a thesaurus you have already created, first;
go to " settings"
click "thesauri"
Select the thesaurus you want to add data to.
At the bottom, you will see an import button
When you click the button, you'll be prompted to select the csv button to import.
Linking pieces of Information in Uwazi
Connections link two bits of information in your collection together. The link could be a paragraph to a document or a word to an entity. To create these connections, follow these steps:
click on settings
Click on "relationship types"
Name your connections here. Now you can create connections within your document collection.
