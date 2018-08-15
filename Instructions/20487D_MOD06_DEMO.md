# Module 2: Querying and Manipulating Data Using Entity Framework

 Wherever you see a path to file starting at [repository root], replace it with the absolute path to the directory in which the 20487 repository resides. 
 e.g. - you cloned or extracted the 20487 repository to C:\Users\John Doe\Downloads\20487, then the following path: [repository root]\AllFiles\20487D\Mod01 will become C:\Users\John Doe\Downloads\20487\AllFiles\20487D\Mod01

# Lesson 1: Web Deployment with Visual Studio

### Demonstration: Deploying a web application with Visual Studio

#### Demonstration Steps

1.  Click **Start**, type **Visual Studio**. From the search results, right-click **Visual Studio 2017**, and then select **Run as administrator**, In User **Control dialog** box  click **Yes**.
2.  On the **File** menu, point to **New**, and then click **Project**.
3.  In the **New Project** dialog box, on the navigation pane, expand the  **Installed** node, expand the **Visual C\#** node, click the **Web** node, and then in the list of templates, click **ASP.NET Core Web Application**.
4.  In the **Name** text box, type **MyWebSite**.
5.  In the **Location** text box, type **[repository root]\Allfiles\20487C\Mod06\DemoFiles\DeployWebApp**.
6.  Clear the **Create directory for solution** check box, and then click **OK**.
7.  In the **New ASP.NET Web Application** dialog box, select **API**, and then click **OK**.
8.	Open **Microsoft Edge** and go to **https://portal.azure.com**.
9.	If a page appears asking for your email address, enter your email address, and then click **Next**. Wait for the sign in page to appear, enter your email address and password, and then click **Sign In**.

	>**Note :** If during sign in, a page appears asking you to choose from a list of previously used accounts, select the account you previously used, and then enter your credentials.

10.	In the left menu of the portal, click **App Services**.
11. In the action bar, click **Add**, select **Web App**, and then at the bottom of the third screen, click **Create** .
12.	In the **App name** box, type the name **mod6demo1***YourInitials* (YourInitials contains your initials). This is a unique value, which when combined with the **.azurewebsites.net** suffix is used as the URL to your web app.
13. In the **Resource Group** section, select **Create new**, and then change the name of the Resource Group to **BlueYonder.Demo.06**.
12.	Click **App Service Plan/Location** and then click **Create new**.
13. In the **App Service Plan** box, type **BlueYonderDemo06**.
14.	In the **Location** drop-down list, select the region closest to your location.
15. In the **Pricing tier** section, select **D1 Shared**, and then click **OK**.
16. Click **Create** . The site is added to the Web Apps table and its status is set to **Creating**. 
17.	After the status changes to **Running**, in Visual Studio, on the **View** menu, click **Server Explorer**.
18.	In **Server Explorer**, right-click the **Azure** pane, and then click **Connect To Microsoft Azure Subscription**.
19.	On the login screen, if a page appears asking you to choose from a list of previously used accounts, select the account you previously used, enter your credentials, and then click **Sign in**.

    >**NOTE :**	Wait until the login process completes.
        You only need to perform this step once, to import your Microsoft Azure account settings to Visual Studio.
        Now **Visual Studio 2017** can display the list of Web Apps and Cloud Services to which you can deploy applications.

20.	In Visual Studio, in **Solution Explorer**, right-click **MyWebSite** project, and then click **Publish**.
21.	In the **Pick a publish target** dialog box, choose **App Service**, then in the **Azure App Service** view, select the **Select Existing** option, and then click **Create Profile**.
22.	In the **App Service** dialog box, expand **BlueYonder.Demo.06** folder, select **mod6demo1[YourInitials]**, and then click **OK**.
23. Click **Publish**.
    >**Note:** Visual Studio publishes the application according to the settings that are provided in the profile file. After deployment finishes, Visual Studio opens Internet Explorer and displays the web app. The deployment process is quick, because the process only copies the content of the application to an existing virtual machine and does not need to wait for a new virtual machine to be created.
24. In the browser navigate to the following **URL**:
    ```url
    http://mod6demo1[YourInitials].azurewebsites.net/api/values
    ```
25. Verify that the response is: **["value1","value2"]**.
26. Close all open windows.

# Lesson 3: Continuous Delivery with Visual Studio Team Services

### Demonstration: Continuous delivery to websites with Git and VSTS

#### Preparation Steps
  
To present this demonstration, you must have a **Microsoft account**. If you have not created a Microsoft account before, create one before you start the demonstration.

> **Important!** Make sure you are connected to your Microsoft account in Visual Studio 2017 before starting this demonstration!

#### Demonstration Steps

1. Open **Microsoft Edge** browser.
2. Navigate to **https://portal.azure.com**.
3. If a page appears asking for your email address, enter your email address, and then click **Next** and enter your password, and then click **Sign In**.
4. If the **Stay signed in?** dialog appears, click **Yes**.
   >**Note**: During the sign-in process, if a page appears prompting you to choose from a list of previously used accounts, select the account that you previously used, and then continue to provide your credentials.
5. Click **App Services** on the left menu panel, to display all the **App Services**.
    - Click on **Add** in the **App Services** blade, letting you select app service template.
    - Click on **Web App** in the **Web** blade, overview of the template will be shown.
    - Click on **Create** button in the **Web App** blade.
6. To create the **Web App** fill-in the following fields:
    - In the **App Name** text box, type the following web app name: **mod6demo3**{YourInitials}.
        >**Note:** The **App Name** will be part of the URL.
    - In the **Resource Group**  select **Create new**, and type in the text box below **mod6demo3**.
    - Click on **App Service plan/Location** and then click on **Create new**, then open **New App Service Plan** blade, fill-in the following information:
        - In the **App Service plan** text box type: **Mod6Demo3ServicePlan**.
        - Click on **OK**.
    - Click on **Create** and wait that **App Services** is created.
7. Open new tab in the browser and navigate to **https://www.visualstudio.com/team-services/** and click **Get started for free**.
8. On the **Sign in** page, enter your **Microsoft account** email address,and then click **Next**.
    >**Note:** If instead of a **Sign in** page, you see a **Pick an account** page, pick your account and click **Next**.
    - On the **Enter password** page, enter your password, and then click **Sign in**.
    >**Note:** If this is the first time you logged in with your account to VSTS, follow the next steps, else skip to step 14.
9.  In the **Host my projects at** page, enter a unique name. (We will relate to that unique name as _youraccount_ from now on.)
10. Under **Manage code using**, select **Team Foundation Version Control** then click on **Continue**.
    >**Note:** Wait until the account creation is done and you will redirect to the **MyFirstProject** page.
12. If you already have projects in your account, click **New Project**, else skip to the next step.
13. In the **Create new project** page, enter the following details:
    - Project name: **MyApp**
    - Version control: **Git**
    - Click on **Create**. 
    > **Note:** Wait for the project to be created.
14. In **MyApp** page, click on **Generate Git credentials** and enter the following details:
    - Alias: **mod6demo3**
    - Password: **Password123**
    - Confirm Password: **Password123**
    - Click on **Save Git Credentials**
15. Click on **Build and release** on the top blade.
16. Click on **New pipeline**.
17. In **Select a source** choose **VSTS Git**, then click on **Continue**.
18. Select **Azure Web App for ASP.NET**, then click on **Apply**.
19. In **Azure subscription**, enter the following details:
    - Select your azure subscription.
    - Click on **Authorize**.
    - In the popup window login with your azure credentials.
20. In **App service name** select **mod6demo3**{YourInitials}.
21. Click on **Triggers** tab, then click on **Add** under **Branch filters**.
22. Click on **Save $ queue** tab and select **Save**, then click **Save** again in the popup window. 
23. Open **Command Line**.
24. Run the following command to Switch directory:
    ```bash
    cd [Repository Root]\Allfiles\Mod06\Demofiles
    ```
25. Run the following command to clone repository to local repository:
    ```bash
    git clone  https://_youraccount_.visualstudio.com/MyApp/_git/MyApp
    ```
    > **Note:** Replace **_youraccount_** with the name that was provided in point 5.
    - Enter UserName: **mod6demo3**
    - Enter Password: **Password123**
26. Run the following command to switch directory to **MyApp**:
    ```bash
    cd [Repository Root]\Allfiles\Mod06\Demofiles\MyApp
    ```
27. Run the following command to create a new **WeaApi** project:
    ```bash
    dotnet new webapi -n MyProject
    ```
28. Run the following command to create a new **Solution**:
    ```bash
    dotnet new sln -n Mod6Demo3
    ```
29. Run the following command to add **MyApp** project to **Mod6Demo3** solution:
    ```bash
    dotnet sln Mod6Demo3 add MyApp\MyApp.csproj
    ```
30. Run the following command to add the new files for the next commit:
    ```bash
    git add .
    ``` 
31. Run the following command to **commit** the changes:
    ```bash
    git commit -m "my first commit"
    ```
32. Run the following command to **push** the changes to our repository:
    ```bash
    git push
    ```
33. Return to **Visual studio team services** and click on **Build and Release**, 
34. Locate the pipeline that was created and then click on the **build id** (starts with hash tag).
    > **Note:** Wait until the build is finished. 
35. Navigate to the **Web App** url that was created in azure:
    ```url
    https://Mod6Demo3{YourInitials}.azurewebsites.net/api/values
    ```
36. The response shoulde be a **JSON** with the following values:
    ```json
    ["value1", "value2"]
    ```
37. Close all windows.


# Lesson 4: Deploying to Staging and Production Environments 

### Demonstration: Using deployment slots with Azure Web Apps

#### Demonstration Steps

1. Open **Microsoft Edge** browser.
2. Navigate to **https://portal.azure.com**.
3. If a page appears asking for your email address, enter your email address, and then click **Next** and enter your password, and then click **Sign In**.
4. If the **Stay signed in?** dialog appears, click **Yes**.
   >**Note**: During the sign-in process, if a page appears prompting you to choose from a list of previously used accounts, select the account that you previously used, and then continue to provide your credentials.
5. Click **App Services** on the left menu panel, to display all the **App Services**.
    - Click on **Add** in the **App Services** blade, letting you select app service template.
    - Click on **Web App** in the **Web** blade, overview of the template will be shown.
    - Click on **Create** button in the **Web App** blade.
6. To create the **Web App** fill-in the following fields:
    - In the **App Name** text box, type the following web app name: **mod6demo4**{YourInitials}.
        >**Note:** The **App Name** will be part of the URL.
    - In the **Resource Group**  select **Create new**, and type in the text box below **mod6demo4**.
    - Click on **App Service plan/Location** and then click on **Create new**, then open **New App Service Plan** blade, fill-in the following information:
        - In the **App Service plan** text box type: **Mod6Demo4ServicePlan**.
        - Click on **Pricing tier**.
            - Select **Production** tab.
            - In **Recommended pricing tiers** select **S1**.
            - Click on **Apply**. 
        - Click on **OK**.
    - Click on **Create** and wait that **App Services** is created.
7. Click on **App Services** on the left menu panel, to display all the **App Services**.
8. Click on **mod6demo4**{YourInitials} app service. 
9. Click on **Deployment credentials** under **DEPLOYMENT** section, to add credentials to our app service, and fill-in the following information:
    - In the **FTP/deployment username** type **FTPMod6Demo4**{YourInitials}.
    - In the **Password** and **Confirm password** text box type: **Password99**.
    - Click on **Save**.
10. Click on **Deployment slots** on the left blade menu under **DEPLOYMENT** section.
    - Click on **Add Slot**:
        - In **Name** type **Staging**
        - In **Configuration Source** select **mod6demo4**{YourInitials}.
        - Click on **OK**.
11. Open **Command Line**.
12. Change directory to the starter project, run the following command in the **Command Line**:
    ```bash
    cd [Repository Root]\Allfiles\Mod06\Demofiles\SimpleServiceForDeploymentSlots
    ```
13. Open the project in **VSCode** and paste the following command and press enter:
    ```bash
    code .
    ```
14. Expand **Properties** folder then **PublishProfiles** folder and double-click on **Azure.pubxml**.
15. Replace {YourInitials} with your initials from the **Azure web App**.
16. In **PublishProfiles** double-click on **Staging.pubxml**.
17. Replace {YourInitials} with your initials from the **Azure web App**.
18. Switch to **Command Line**, and paste the following command:
    ```bash
    dotnet publish /p:PublishProfile=Azure /p:Configuration=Release
    ```
    > **Note :** If the there was an error in the publish process, restart the **mod6demo4**{YourInitials} app services.
19. Open **Microsoft Edge** browser. 
20. Navigate to the following url:
    ```url
    https://Mod6Demo4{YourInitials}.azurewebsites.net/api/values
    ```
21. The response shoulde be a **JSON** with the following values:
    ```json
    ["value1", "value2"]
    ```
22. Switch to **VSCode**.
23. Expand **Controllers** and double click on **ValuesController**.
24. Locate **Get** method and add to the array **value3**.
25. Switch to **Command Line**.
26. Paste the following command to publish in the staging slot:
    ```bash
    dotnet publish /p:PublishProfile=Staging /p:Configuration=Release
    ```
    > **Note :** If the there was an error in the publish process, restart the  Mod6Demo4-{YourInitials}-staging app services.
27. Open new **Microsoft Edge**  browser. 
28. Navigate to the following url:
    ```url
    https://mod6demo4-{YourInitials}-staging.azurewebsites.net/api/values
    ```
29. The response shoulde be a **JSON** with the following values:
    ```json
    ["value1", "value2", "value3"]
    ```
30. Switch to **Azure Portal**.
31. Click on **App Services** on the left menu panel, to display all the **App Services**.
32. Click on **mod6demo4**{YourInitials} app service.
33. In **Overview** blade click on **Swap** on the top bar.
34. In **Swap** blade added the following steps:
    - In **Swap type** select **Swap**.
    - In **Source** select **production**.
    - In **Destination** select **Staging**.
    - Click **OK**. 
35. Switch to **Microsoft Edge** browser with the production url.
36. Refresh the page (prass **F5**).
37. The response shoulde be a **JSON** with the following values:
    ```json
    ["value1", "value2", "value3"]
    ```

©2018 Microsoft Corporation. All rights reserved.

The text in this document is available under the [Creative Commons Attribution 3.0 License](https://creativecommons.org/licenses/by/3.0/legalcode), additional terms may apply. All other content contained in this document (including, without limitation, trademarks, logos, images, etc.) are **not** included within the Creative Commons license grant. This document does not provide you with any legal rights to any intellectual property in any Microsoft product. You may copy and use this document for your internal, reference purposes.

This document is provided &quot;as-is.&quot; Information and views expressed in this document, including URL and other Internet Web site references, may change without notice. You bear the risk of using it. Some examples are for illustration only and are fictitious. No real association is intended or inferred. Microsoft makes no warranties, express or implied, with respect to the information provided here.