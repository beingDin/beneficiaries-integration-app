# beneficiaries-integration-app

- [x] Deploy Project PI to IIB Integration Node
   <img width="1372" alt="1" src="https://github.com/user-attachments/assets/a63f188c-3162-4692-8ebd-442de1564e24">
   
- [x] Launch IIB Integration Console & run the command script - 01_StopAndBackupv10Node.cmd from its source directory 
- [x] This will create a backup file of the node resources and configuration
- [x] The backup file is written to \myBackupsIIB\v10backup.zip
- [x] Launch ACE Console and run the command script - 02_ExtractComponentsTO_node.cmd from its source directory
- [x] This script will migrate the resources defined in v10backup.zip to a v12 Integration Node
- [x] Finally the script will start the migrated integration node
- [x] Switch to the Integration Explorer View in the v12 App Connect Enterprise Toolkit to see the migrated resources
- [x] Run the command script - 03_ExtractComponentsTO_server.cmd to migrate resources backed up in the v10backup.zip file to an independent Integration Server
- [x] Connect to Integration Sever and ‘Retrieve and import resources’ to import the resources into your workspace
- [x] Recreate the CommonLib reference and Clean all projects. Clean should remove all ‘import path’ errors
- [x] Redo the ‘Promoted to flow’ properties & verify the ‘User Defined Properties’. This should resolve all errors
- [x] Update the HTTP endpoints in the list sub-flows to call Stub APIs endpoints
- [x] Redeploy to Integration Server and run a test to retrieve records. Deploy the same BAR file into CP4I - Integration Server. 
- [x] Obtain the API Endpoint in CP4I and run a test to retrieve the records successfully.
- [x] When testing with Newman you can run the provided collection using the command newman run -k test.json -e test-env.json
