#### 1. Export WCM Data
1. Login to the server via RDP. Open Command Prompt and type the following commands one by one, 2 and 3.  
2. `cd C:\IBM\WebSphere\wp_profile\ConfigEngine`  
3. `ConfigEngine.bat export-wcm-data -Dexport.allLibraries=true -Dexport.directory=C:/Users/Administrator/Desktop/wcm -Dexport.singledirectory=true -DWasPassword=upperstorey -DportalAdminPwd=upperstorey`  
4. Compress it in a zip archive. Files are located in `C:/Users/Administrator/Desktop/wcm`.
5. Download the archive to your local machine from the server (check Side Note below).   
**Note**: If the build failed for some reasons, try to run it again. Sometime it will throw login error.

#### 2. Export WCM Pages: 
1. Login to WP, and go to Administrator section. Click on Manage Pages under Portal User Interface.  
2. Click on Content Root. Pages list will appear, click on Export icon for Navy in the list. It will export all the pages as xml format.  

#### 3. Theme Ear File (check ref 2 and 5 below for more details):
1. Open Eclipse, create workspace if not created yet. Create new project as `Dynamic Web Project`(refer to ref 5 below). If `Web` is not available to choose, refer to ref 6 for installing(Go to the link, drag and drop the install link to eclipse. It will open eclipse market place to start installation). Name it as Navy_Theme.  
3. If it is not already selected, select 2.4 for the Dynamic Web Module version while creating the project. Image below.
4. Select Add project to an EAR. Click Next and Next.  Image below.
  ![Selection_001](/uploads/e9e73d83e7e11f0a341a21fff9c6d11a/Selection_001.png)
5. Change Context Root to `Navy_Theme`.
6. Add the custom static files(theme folder, Navy17) to WebContent folder. The rest are fine. Eclipse will be used to package the files later. Use file explorer for copying.
7. After copying make sure to refresh the project in eclipse by right click and choose refresh.  
8. Now in Eclipse right click on the project Navy_Theme and mouse over Export. Choose Export, select Java EE and choose EAR file and click next. Name should be Navy_Theme, Destination should be different than workspace. Browse for location to save the EAR file. Click finish. Congratulations, you have done it.  
**Note**: WebDAV is used for static contents push to the server via file store.  

#### 4. Theme Ear File Dynamic Contents (JSP etc) (check ref 2 below for more details):  
1. This may not be necessary to do almost at all as dynamic JSP's are configured already. In rare cases it may happen when there is a need to add/configure/update the backened for frontend. Filename is Navy_Theme_Dc.  
2. Copy over the contents from `PortalServer\theme\wp.theme.themes\simple\installed Apps\SimpleTheme.ear\SimpleTheme.war\themes` in file explorer. Eclipse will be used to package the files later. Use file explorer for copying.  
3. Use the same method from step 3 to package the file as EAR. Filename must be Navy_Theme_Dc.  
**Note**: Files/JSP or any other file(s) has to be directly modified on the server 1st.  

#### Side Note:
I am using shared drive to copy over the files from the server to my local machine. You can see that on the server as Shared-from-server in explorer. It will be only accessible on my Linux machine as i configured RDP for it.  

#### Extra (only for info purpose):
Theme Artifacts:  
cd C:\IBM\Ear  
C:\IBM\WebSphere\AppServer\bin\ws_ant.bat -f assembleArtefacts.xml  

#### References
1. https://www.ibm.com/support/knowledgecenter/en/SSYJ99_8.5.0/wcm/wcm_config_wcmlibrary_export.html  
2. https://www.ibm.com/support/knowledgecenter/SSHRKX_8.5.0/mp/dev-theme/themeopt_themedev_manual_warbased_copy.html  
3. https://developer.ibm.com/answers/questions/219725/how-do-i-create-a-copy-of-the-websphere-portal-85.html  
4. https://www.ibm.com/support/knowledgecenter/SSHRKX_8.5.0/mp/dev-theme/themeopt_themedev_manual_warbased.html  
5. https://help.eclipse.org/kepler/index.jsp?topic=%2Forg.eclipse.stardust.docs.wst%2Fhtml%2Fwst-integration%2Fdynamic-web-proj.html
6. https://marketplace.eclipse.org/content/eclipse-java-ee-developer-tools-0