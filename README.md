# beneficiaries-integration-app

- [x] Deploy Project PI to IIB Integration Node 

<img width="1372" alt="1" src="https://github.com/user-attachments/assets/a63f188c-3162-4692-8ebd-442de1564e24">
<br/><br/>
  
- [x] Launch IIB Integration Console & run the command script - 01_StopAndBackupv10Node.cmd from its source directory
      

<img width="1131" alt="2" src="https://github.com/user-attachments/assets/7d5b1326-c9eb-4889-8466-793833c1aba5">
<br/><br/>

- [x] This will create a backup file of the node resources and configuration. The backup file is written to \myBackupsIIB\v10backup.zip
      

<img width="1126" alt="3" src="https://github.com/user-attachments/assets/45b60c9a-4c14-4369-aaa9-247420e4fe63">
<br/><br/>
      
- [x] Launch ACE Console and run the command script - 02_ExtractComponentsTO_node.cmd from its source directory
      

<img width="978" alt="4" src="https://github.com/user-attachments/assets/1a3e8d5a-cf65-4f00-a0d3-52ec74e16ed3">
<br/><br/>
    
- [x] This script will migrate the resources defined in v10backup.zip to a v12 Integration Node. The script will also start the migrated integration node
      

<img width="981" alt="5" src="https://github.com/user-attachments/assets/70b1280a-1133-465c-8016-6a265e0d0e18">   
<br/><br/>
 
- [x] Switch to the Integration Explorer View in the v12 App Connect Enterprise Toolkit to see the migrated resources
      
      
<img width="1126" alt="6" src="https://github.com/user-attachments/assets/8628fbc8-042d-4538-bf2d-bc00baf79394">
<br/><br/>
     
- [x] Run the command script - 03_ExtractComponentsTO_server.cmd to migrate resources backed up in the v10backup.zip file to an independent Integration Server
      

<img width="975" alt="7" src="https://github.com/user-attachments/assets/6c4d2d22-8275-4d87-aa8d-c5dd86b05af1">
<br/><br/>

- [x] Connect to Integration Sever using the Admin port shown in the console
      

<img width="983" alt="8" src="https://github.com/user-attachments/assets/07ba99ce-fb36-41e7-a8d5-12b7e87dcb1d">
<br/><br/> 

- [x] Use ‘Retrieve and import resources’ to import the resources into your workspace
   

<img width="600" alt="10" src="https://github.com/user-attachments/assets/edca2b10-5871-42f3-8615-97049fc26b19">
<br/><br/> 

- [x] Recreate the CommonLib reference and Clean all projects. Clean should remove all ‘import path’ errors


<img width="1486" alt="11" src="https://github.com/user-attachments/assets/ec136807-ec70-4709-b5d2-8991f985950e">
<br/><br/> 
 
- [x] Redo the ‘Promoted to flow’ properties & verify the ‘User Defined Properties’. This should resolve all errors
- [x] Update the HTTP endpoints in the list sub-flows to call Stub APIs endpoints
- [x] Redeploy to Integration Server and run a test to retrieve records. Deploy the same BAR file into CP4I - Integration Server. 
- [x] Obtain the API Endpoint in CP4I and run a test to retrieve the records successfully.
- [x] When testing with Newman you can run the provided collection using the command newman run -k test.json -e test-env.json
