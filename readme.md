# db_test

This directory contains files you will need to test connectivity to two different databases: one remote and the other local.

### Files included:

- db_test.jar:  This the Mule Application that needs to be opened in Anypoint Studio 7.3.2 (you can download it from https://www.mulesoft.com/ty/dl/studio Note that to run Studio, you will need JDK 1.8)

- mulesoft-training-services-1.6.2.jar:  This runs a local Derby database. To run the local server, use a terminal and issue command `java -jar mulesoft-training-services-1.6.2.jar`


### To test connectivity with **REMOTE MySQL database**:

1. Use Anypoint Studio to import db_test.jar Mule application

	- Open Studio, use menu "File > Import"

	- Expand folder "Anypoint Studio" and select "Packaged mule application (.jar)"

	- Point to the `db_test.jar` to import it

2.  Once the project is loaded,

	- Expand `src/main/mule` folder and open `db_test.xml`.  This should open db_test in a tab.

	- Click on "Global Elements" tab

	- Double-click "Database_Config".  Database details are already configured

	- Click on "Test Connection" button to verify connectivity to MySQL database.

	- If the connection fails (indicates either you are behind a proxy or using VPN). In such a case, try the following "LOCAL" option


### To test connectivity with **LOCAL Derby database**:

1.  Start the local server using `mulesoft-training-services-1.6.2.jar` as directed above

2.  After importing the `db_test` Mule app into Studio (see steps above), use the "Global Elements" tab, and open "Global Property".  Replace the value `REMOTE` with `LOCAL`.  Close the dialog box.

3.  From "Global Elements", double-click "Database_Config" to open it.

4.  Click on "Test Connection" button to verify connectivity to Derby database.