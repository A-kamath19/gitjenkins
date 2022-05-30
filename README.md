# gitjenkins
## Steps to integrate Jenkins with GitHub
1. Ensure that Git plugin is installed in Manage Jenkins section
![image](https://user-images.githubusercontent.com/74644342/171019973-5b262c3e-4094-417e-aec3-87060d613b4f.png)

2. Create a New Job 
- Click on New Item on Dashboard
- Write the item name
- Select Freestyle project
- ![image](https://user-images.githubusercontent.com/74644342/171020123-201a0302-f436-4fdb-85dc-3398201b295d.png)
- Click on OK

3. Configure project
- In Source code management section, click on Git radio-button
- Enter the Git repository URL
- ![image](https://user-images.githubusercontent.com/74644342/171021715-a0f949cd-9f61-478b-8b46-c7a830fefa73.png)
- In the Branches to build section leave Branch specifier with '*'
- ![image](https://user-images.githubusercontent.com/74644342/171025490-685d6faf-f3b2-49ff-9339-c427a15bb1fb.png)
- In the Build Triggers section, click on 'GitHub hook trigger for GITScm polling' or any trigger of your choice
- ![image](https://user-images.githubusercontent.com/74644342/171021904-09c29c4d-7c3d-4df4-8df4-6339059a058f.png)
- In Build section, do the following
- ![image](https://user-images.githubusercontent.com/74644342/171022412-9a40d06b-89e9-4314-b9df-5144e3a527b6.png)
- click on Apply

4. Configure GitHub
- Go to Settings
- Click on Webhooks and then click on Add webhook.
- In the Payload URL field, paste your Jenkins URL. At the end of the URL append /github-webhook/. 
- In the Content type select: ‘application/json’.
- ![image](https://user-images.githubusercontent.com/74644342/171023480-468b3769-5cd5-4fe4-a671-bef454b15069.png)
- In 'Which events would you like to trigger this webhook?' section click on 'Let me select individual events.' and select 'Pull Requests’ and ‘Pushes’. 
- At the end of this option, select the ‘Active’ option and click on ‘Add webhook’.
- ![image](https://user-images.githubusercontent.com/74644342/171023592-27e0ed8c-76ca-487f-b297-fcd2632b0264.png)

5. Let's check the output
- Make some changes in your java file and commit the changes
- Go to jenkins and click on Build Now
- Once the build is completed click on console output
- ![image](https://user-images.githubusercontent.com/74644342/171025362-315575f8-ed5d-4f4b-85b2-6c17af8a6629.png)

 
