**Creating Static Content in WCM**  
1) Create Authoring template (AT)  
2) Create Presentation template (PT)  
3) Create Site area(if necessary) and contents  

**1) Create Authoring template (AT)**  
1.1 Check the html how to separate and which fields to be editable   
1.2 Go to the library(where we want to create static content) and click on Authoring template.  
1.3 Click on new and choose content template  
1.4 Fill a name, display title and description  
1.5 Click on Manage Elements to create Elements which we want to be able to edit from front end  
1.6 Save and close

**2) Create Presentation template (PT)**  
2.1 Go to the library and click on Presentation template  
2.2 Click on new and choose presentation template  
2.3 Give a name, display title and description.  
2.4 Add the html in the Presentation template options box.  
2.5 Link to the elements in the AT (click on Insert tag, choose Editable element in tag type, content in source item type, current in item context and choose the AT we created above and click Ok).
2.6 Save and close.  
**Once we created PT, Go to AT and link the newly created PT in Default presentation template.** 

**3) Create Site Area(if necessary) and contents**  
3.1 Go to the library and under content, click on new and site area , default site area template  
3.2 Fill a name, display title and description  
3.3 Click on properties tab, under profile, add a key(ibm.portal.toolbar.NewContent) to show up in front end to drag and drop if the site area is newly created and save   
3.4 Finally create contents under the site area. Click on new, content, choose the AT and fill the contents.  
3.5 Click properties tab, under workflow, choose the workflow, submit for approval.

**Once the content is created, go to the page in frond end. Turn on editable mode and drag and drop the content component.**
   

