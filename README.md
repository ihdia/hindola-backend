# hindola-backend
This is the repository for the component which serves the front-end web-based annotation interface and manages the back-end DB in our HInDoLA system. 

The first step is to setup the backend database. 
Download MYSQL from https://www.mysql.com/downloads/
Set up with a Username and Password and use the same credentials in the app.py file in the Annotation_App folder.
Create a database using the MYSQL command line and also set it as the database name in the app.py.

### Database Handling
1. If you have the .sql file containing all the information then use the following command to connect to your database:

 mysql -u localusername -p local databasename < yourfilename.sql

2. If there is another database serving a remote website the nuse the following commands:

 mysqldump -u remoteusername -p -h your.site.com localdatabasename > dump.sql
 mysql -u localusername -p local databasename < dump.sql
### To setup the backend server on local system
1. Download the repository and install the prerequisites mentioned in Annotation_App/requirements.txt
2. Go to the Annotation_App folder and locate app.py
3. Run ```python3 app.py ```

The Annotation App is to manage the manuscripts annotations through an interactive GUI. Implemented in Flask, the App has useful features to annotate images from large manuscripts libraries.

### Annotations
1. Open the page at the started local server
2. Sign-up and login
3. Request image through "Request" Button
4. Annotate with the regions provided - Freehand (single click to start and double click to finish), Polygon(Single click     to start, each click adds new vertex and double click to finish)
5. "Done" button to save the annotations, "Skip" button to skip the image 
