# GCP Migration
Migración de una VM a la nube de google usando los comandos del SDK de Google

## 1- Download the Google Cloud SDK
- https://cloud.google.com/sdk/docs/downloads-interactive?hl=es-419
- Choose your OS and click the "Cloud SDK Installer" link
- Open the setup, select "Single User (YOUR_USER)" and leave the rest otions by default
- "Would you  like to log in (Y/n)?" Type "Y"
- Open the link and sing in with your GCP account, once you have sing clik on the "Allow" button of the next page
- "Pick cloud project to use:" and select the project in which you have your credits (the project that you want to use for the migration --> IF YOU HAVE ONE ALREADY)
- "Do you want to configure a default Compute Region and Zone? (Y/n)?" Type "Y" and choose the number of your region or the region in wich you want to create the project

## 2- Export your on-Premise or Virtualized VM OVA to a GCP bucket
- Start a export job and get the .ova file of your VM (In VMware: File --> export to OVF... --> Change the extension to .ova)
- In the GCP console go to: Cloud Storage > Buckets > Create Bucket
- Name: Select the name of your bucket | Location type: Region | Location: choose the region you previously specified
- Leave the rest otions by default and click "CREATE"
- Back to your SDK console and use this command for copy your OVA in the bucket: 
```cmd
gsutil cp "YOUR_OVA_PATH.ova" gs://YOUR_BUCKET_NAME
```

## 3- Import the OVA to a new instance
- Write the next command:
```cmd
gcloud compute instances import gcpinstanename --os=[YOUR_VM_OS] --source-uri="gs://[YOUR_BUCKET_NAME]/[YOUR_OVA_NAME].ova"
```
