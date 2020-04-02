# MasterPageLayoutCreation
Steps to create a master page layout in SharePoint using Designer

A master page layout is a frame like structure which contain web controls shared by different pages. For example, the top navigation bar, logos, or the left navigation bar, search bar etc construct a frame that is shared by many pages in the application. So, we can create a master page layout to store all the web controls and can be easily shared among different pages.

To create a master page, first create a folder and place all the html,css, images and any other files that belong to the master page layout in it.

Then, create a site collection in https://<tenant name>-admin.sharepoint.com/_layouts/15/online/SiteCollections.aspx
  Example : https://intern2k20-admin.sharepoint.com/_layouts/15/online/SiteCollections.aspx
  
 In the site collection page, click on new and select Private or Public site collection.
 Then, in the pop up fill the fields like Title, Administrator and select it as Publishing Portal under the Publishing tab. Click Ok, it creates a new Master Page with the title specified.
 
 Right click on the newly created master page, copy the site url and paste it in a new tab. The master page gets opened.
 
Go to Site Contents, in Site Settings>>Site Collection Administration>>site collection features>>Activate SharePoint Server Publishing Infrastructure. This will enable Design Manager feature for this site. Design manager is a feature in SharePoint 2013 that makes it easier to create a fully customized, pixel-perfect design by using a web design tool or HTML editor.
 
Open the site in SharePoint Designer by pasting the site url in Designer. Now open All Files >> _catalogs >> masterpage.

Copy paste the initially created folder contents into it(folder containing html,css, images etc.). 

Go back to browser >> Site Contents >> Site Settings >> Look and Feel >> Design Manager.

In Design Manager, click 4. Edit Master Pages >> Convert an HTML file to a SharePoint Master Page.
Now, select the html page that contains the overall content of the master page that you have added in Designer and click Insert.

If the master page html code contains the content inside the master page like the page that will be displayed on clicking any web control on navigation bar etc., then remove the code from it.

The code can be removed as follows : 
>> GoTo Designer >> MasterPages Folder. You will find two files like if your html file name is myHTMLFile.html, you will find myHTMLFile.html and myHTMLFile.master. Open myHTMLFile.html and remove the entire code. Open the page in browser and refresh it. Now you can find only the master page.

Once the editing is completed, we have to publish the site. Go to the Design Manager inside the Look and Feel and click on the ... beside the master page, click ... inside it, go to advanced and then click publish a major version.
