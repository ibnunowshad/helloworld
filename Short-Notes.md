**Static Contents:**

- Authoring template with manage elements.
- Presentation Template - copy the html code of the section and do the editable elements by using insert tag.
- Once again goto authoring template and In item properties, Look for : 
Default Presentation Template: link with the specified presentation template. 
- `Content - create site area and in properties-> profile add "ibm.portal.toolbar.NewContent" to show as a page component`
- Once again goto Content and add default contents..

**Dynamic contents:**

- Authoring Template: with manage elements
- Presentation Template - empty template
- Content - create site area (Default Site Area)  and add
Child Template Mappings of the PT and AT.
- Component - current view - create menu and LP. 
In LP, List Paging Option - Result per page - 10000000.
List Page Markup : Header , Result Design 1 and footer. Copy the required html codes in the respective fields.
 Once the List Page Markup is done, do the editable elements. Once the editable elements done. 
Goto to Menu.and look for Select the criteria to use when searching for content and check the location.

In location, select the site area, include descendants and then add the specified site area.
In Menu design properties,  look for formating - Use a list presentation.

- finally Goto presentation template again. and insert tag and choose component. then choose only that menu. no need to choose LP.
Now we can add the contents. Goto content, choose the specified "On deployment carousel - AT" and add all the dynamic content. 
Once all the contents are added. come to edit mode and add page component. In application look for web content viewer and drag it.


**Dynamic contents with category:**

- Authoring Template: with manage elements
- Presentation Template - empty template
- Content - create site area  and add
Child Template Mappings of the PT and AT.
- Category - create Taxonomy first and then create all the categories.
- Component - current view - create menu and LP.
 Once the LP is done, do the editable elements. Once the editable elements done. 
Goto to Menu.and look for Select the criteria to use when searching for content and check the location and category

In location, select the site area, include descendants and then add the specified site area.
In category, - check include descendants and then add the specified category.
In Menu design properties,  look for formating - Use a list presentation.

- finally Goto presentation template again. and insert tag and choose component. then choose only that menu. no need to choose LP.
Now we can add the contents. Goto content, choose the specified "On deployment carousel - AT" and add all the dynamic content. 
Once all the contents are added. come to edit mode and add page component. In application look for web content viewer and drag it.


**LINK ELEMENT AND IMAGE ELEMENT:**

```<a href='[Element key="Link" type="content" context="autofill" format="url"]'>
 <img  src='[Element key="Episode Image" type="content" context="autofill" rendition="auto" format="url"]' alt='[Element key="Episode Image" type="content" context="autofill" rendition="auto" format="alt"]'>   
</a>```


For categories, we need to use as below
`[Property field="categories" type="content" context="autofill"]`

Unique name in open page setting -> advanced
`com.navy.sg.about.org.structure.formations`