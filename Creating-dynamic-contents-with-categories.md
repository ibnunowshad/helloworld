1) Create Authoring Template  
2) Create Presentation Template  
3) Create Site Area  
4) Create Categories  
5) Create List Presentation(LP) and menu  
6) Create Contents under site area

Steps 1 to 3 are same as [creating dynamic contents in wcm](https://github.com/habeebmaraikar/hello-world/wiki/Creating-dynamic-contents-in-wcm)

**4) Create Categories**

4.1 Go to under Categories(same library with authoring and presentation template)  
4.2 Click on New button, choose taxonomy and name it properly  
4.3 To create the categories, go to under the newly created taxonomy, click on New button and choose category and name it properly

**5)Create List Presentation and menu**  

5.1 Go to under components(same library with authoring and presentation template)  
5.2 Click on New button -> Current view and choose list presentation and fill the name, display title and description.  
5.3 Under List Paging Options, put 1000 in results per design  
5.4 Under List Presentation Markup, put the separated html in the boxes  
5.5 The opening and closing html, put in the header and footer and the main middle(dynamic) part, put in the Result design box1.  
5.6 To do the dynamic content, select the content(which we want to be dynamic) and link to the respective elements which we created in the authoring template.(click insert tag, select Element in the tag type, content in source item type, Autofill in item context and choose the authoring template we created above and finally choose the element)
5.7 Save and close.  
5.8 To create menu, repeat steps 5.1. In step 5.2, choose the menu instead of list presentation and give a name, display title and description.  
5.9 Under Menu Criteria, select the location and categories.   
5.10 Under Categories section, check Include descendants and choose the category(need to choose taxonomy)  
5.11 Under Location, select site area and check Include descendants.  
5.12 Under Menu Design properties, select 'Use a list presentation' and link to the LP(created above) and save and close.  
**Once we created LP and menu, go to presentation template and link to menu, not LP. Click on Insert Tag, select component in tag type and choose the menu we created**

Finally create the contents under site area.  
**6) Create Contents under site area**  

6.1 Go to under content and site area we created. Click on new button, content and choose the Authoring template we create above.  
6.2 Under Properties tab, go to profile section and choose the category which need to show under  
6.3 save and close.