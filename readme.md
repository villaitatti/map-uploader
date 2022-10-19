# Map Uploader

## Researchspace compatibiliy

This app works with this [RS version](https://github.com/researchspace/researchspace/tree/FolderUploader)

## About the app
This app will be an important module of the Metapolis project. It allows **authenticated** users to upload on a RS storagee a map in mbtiles folder format. E.g., this example:

```
{map_name}/
  12/
    {X}/
      {Y}.png
  13/
    {X}/
      {Y}.png
  14/
  15/
``` 

## S3 Config

The app has been specifically created for an S3 storage. To install the component, first of all an **S3 storage** should be add.

```
"-Dconfig.storage.{S3-STORAGE-NAME}.type=s3",
"-Dconfig.storage.{S3-STORAGE-NAME}.mutable=true",
"-Dconfig.storage.{S3-STORAGE-NAME}.endpoint={ENDPOINT}",
"-Dconfig.storage.{S3-STORAGE-NAME}.region={REGION}",
"-Dconfig.storage.{S3-STORAGE-NAME}.bucket={NAME}",
"-Dconfig.storage.{S3-STORAGE-NAME}.access-key={ACCESS-KEY}",
"-Dconfig.storage.{S3-STORAGE-NAME}.secret-key={SECRET-KEY}",
```

Then, remember to update the storage from UI when uploading the folder. See the following image: 

<img width="1324" alt="directFolderUploader" src="https://user-images.githubusercontent.com/8267319/196654737-57d3b87c-ca59-4714-9477-8a3d94a71376.png">

## Missing features

We are still working on storing folder data during the uploading process.
