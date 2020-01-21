![](uwazi.png)
# HURIDOCS-User-Manuals
Uwazi Guide Manual information
Uwazi User Guide 2.0

# Introduction to Uwazi
To manage records and documents, most organizations today use folders or categories on platforms like DropBox, One Drive and Google Drive so that staff can access them later.  Although safe and effective, these platforms simply provide a safe space for these documents and provide no connections or analysis.

What if organising documents could make their contents come alive? Uwazi goes beyond tags and filenames to organise your documents. Each document can be critical is telling a story: an email that asks for a favor from a politician, a testimony from a witness of police violence, the ruling of a court on a human rights case. When these stories are connected by the platform, the bigger picture of patterns and systems becomes clearer: ongoing corruption, systematic police violence, legal human rights precedence and abuse of power.

Uwazi is built to do exactly this – highlight and organise the important information in each document, and create relationships between documents. Uwazi illuminates the bigger picture that human rights document collections uncover.
# Table of Content

# Installation Guide

 
## Usage
### Edit account information

To edit account information like:
1. Email address
2. Password
3. Log-out

Click on settings
Click on Account 


### Enable two-factor authentication

### Add new users
If you work in collaboration with other people, Uwazi allows you to create users with specific permissions to help you update your collection of documents.

As you can notice, you do not need to create visitors. This is the basic role when anyone visits your collection!
But if you want to allow some people to perform specific actions into your collection, you can create Users that will allow them login the same way you login into your admin account.
To create a new user, you need to go to Settings and click on the Users section. It will appear a list with all current users inside your collection. You will be able to create new ones, edit or delete them if necessary.
A user has three fields to be completed:
* Username
* E-Mail
* (Editor or Admin).
We will send an email to that person with a link to set the user's password.
Note: If you are hosting your own Uwazi or if you are accessing the instance as localhost, e.g. http://localhost:3000/settings to send the invitation, the email will be sent to the  address of the instance URL.
If you have a proper domain, create the account from that url, for instance: http://yourdoumain.com/settings. This will send a 'yourdomain.com' URL.
If you are using a local IP, then use something like http://192.168.xx.yy/settings for it to send with that address.
### Manage user permissions 
* Any visitor to an Uwazi instance is able to:
* View all the documents, entities, properties, connections, etc in Uwazi (but cannot edit, create, or delete anything)
* User the search and filter functionalities
### A user with the role of editor is able to:
* Do all the things that a visitor can do
* Upload documents and create entities
* Delete documents and entities
* Organize the collection, including: apply properties, create connections and references, create a table of contents
* Add/edit translations
### A user with the role of administrator is able to:
* Do all the things that an editor can do
* Manage settings
* Configure the information architecture, including: create document and entity types/templates, create dictionaries, name connections
* Configure filters
* Add and delete users
* Edit your site information
* Change the name of your collection
Click on “settings”
Click on “collection”
Change the name of your collection
Save



### Make your collection private

If you are handling sensitive information or you just want your collection to be accessible only via login, you can configure Uwazi to do so. 
Click on “settings”
Click on “collection”
Click the checkbox to make the instance private


By activating this option, your information will not be crawled by search engines, and users will be prompted with a login screen when trying to access your documents or entities.
Set your landing page
The landing page is the first thing users will see when visiting your Uwazi instance. By default, your landing page is the Library, without any filter applied and a list with all documents and entities.
However you can use any page from your Uwazi instance as a landing page, just copying and pasting the URL on the text box below the custom page.
These are some examples:
A static page: /page/dicxg0oagy3xgr7ixef80k9
A library query: /library/?searchTerm=test
A document or entity: /document/4y9i99fadjp833di /entity/9htbkgpkyy7j5rk9
Always use URLs relative to your site, starting with / and skipping the https://yoursite.com.
Track web analytics
Uwazi supports both Google Analytics and Matomo so that you can track your collection visits. (If you are hosting your Uwazi with HURIDOCS, we provide Matomo as part of the hosting. Please contact us in order to activate your account.)

Find your unique ID (for example, if you want to use Google Analytics ID to track website visits).
Add your to Uwazi under Settings > then click Collection.


### Mailer configuration
This is a JSON configuration object that should match the options values required by Nodemailer, as explained here.
This setting takes precedence over all other mailer configuration. If left blank, then the configuration file in /api/config/mailer.js will be used.
Public form configuration

### Allow cookies on your site
 

##Build Your Information Architecture
###Create templates
Templates are the foundation of your Uwazi platform as they allow you to attribute consistent, structured metadata to your documents and entities. Within each template, you can assign a variety of properties like:
* Text
* Numerics
* Select (needs thesaurus)
* Multi-select (needs thesaurus)
* Date, date range, multi date, multi date range
* Rich text
* Geo-location
* External links
* Media (for video and audio embedding or self hosting)
* Relationship - allow you to use items from another template as thesaurus items

To create a template:
Click on “settings”
Click on Templates in the Metadata section
Click “add templates”

There will be two default properties: Title and Date Added. 

Add new properties by dragging and dropping them into the designated area.
Give the template a name.
Click Save.

Note:
In case the instance is planned to be in Arabic by default, the template and properties should be created in latin characters then translated into Arabic, otherwise it is going to trigger a bug. Developers are working to fix it.
When you add a select or multi-select property to a type, you will see a field titled Thesauri in which you can select a Thesaurus or a Template that you have already created. See the section on create thesauri for more information on how to create these thesauri.





### Create thesauri
A thesaurus in Uwazi is a list of terms that you have referenced as properties when creating your entity types. 
E.g: You may want to create a thesaurus for countries so you can refer to this list when you add the country property to your document template.  Using thesauri will make data entry and retrieval more precise, coherent and easy. 
You can use the same thesauri across the templates by calling a thesaurus from a property, thus creating connections between different types of information by a common property. 
To create a thesaurus;
Click on “settings”
Click on “thesauri” under the Metadata section

click on “add thesaurus
write the name of the thesaurus; e.g. Type of testimony
 Add some items to this thesauri like “testimony of victims” “testimony of family” etc. 
click ‘save’ when finished. 

 
### Nested options in thesauri
For big thesauri, grouping values in groups makes information more accessible. In the thesauri creation interface, there is a "Create group" at the bottom action buttons and some controls to move items around:

 
Which gets render as a filter:


### Importing new thesauri from CSV files
This feature allows you to import terminology lists in different languages from a CSV file into an Uwazi thesaurus. You can import data into a new or existing thesaurus.
 

### Preparing the CSV file
The CSV file should have a separate column for each language you want to import, the language should be used as the name of the column. Each row contains a term and its translations in different languages.
Here's a sample CSV file viewed as plain text:
Here's a sample CSV file viewed as plain text:
English,French,German
Man,Homme,Mann
Woman,Femme,Frau
Child,Enfant,Kind
 
Here's the same file viewed in a spreadsheet program:

### Importing data into an existing thesaurus
To import data from a thesaurus you have already created, first;
go to " settings"
click "thesauri"
Select the thesaurus you want to add data to.
At the bottom, you will see an import button
When you click the button, you'll be prompted to select the csv button to import.
 
 
 
 
 
 
 
 


### Create relationship types
Connections in Uwazi link two pieces of information in your collection. It could link a paragraph in one document to a separate document or a word to an entity. 

To name your connections; 
Click “settings”
Click on “relationship types” 
Add the type of connections. Once you have named them, you can begin to create connections.

Connect properties in two different templates
Uwazi uses a relationship field in templates. This has some clear advantages like
The allowed targeted entities can be used to ensure only connections to one type of template can be made
For example: We have a type “country” and we want to add that property to another type- a person. By specifying the select list “Country”, your users will only be able to use country for this field. 
A relationship type can be defined as well now. 


Relationship fields will now behave as a regular multiselect while at the same time, create particular relationships that will be displayed like this:

 

You can configure your relationship fields for existing sets of connections to be displayed as a multiselect field like this;
 these connections were added as they were signatories of a document.

## Contributing

## Credits

## License
