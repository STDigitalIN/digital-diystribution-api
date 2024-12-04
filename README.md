# Prerequisites
Before a content supplier can use the ST Digital Distribution API, they must obtain access to ST Digital's AWS S3 bucket to upload their content.


# Folder Structore / Order of placement
- Batch Folder (YYYYMMDDHHmmsssnnn)
  1. Audio File (.wav)
  2. Cover Photo (.jpg)
  3. Metadata File (manifest.json)

*The `manifest.json` file should be placed at the end of the upload process, as it serves as the trigger to initiate content ingestion into our system.*
  
![alt text](https://kb.ddex.net/images/a749ea36830b7bd07b6add0590c0ba83.png)


# Metadata File Structure
``` json
{
  "name":"Ajay"
}
```

## Points to remember
- Each release must have a unique batch folder.
- If a release contains multiple tracks, upload all tracks within the same batch folder.
- The metadata file should contain accurate and up-to-date information.
- The metadata file must include the absolute path for all media files (Audio and Cover Photo), formatted as `bucket-name/your-folder/batch-folder/filename.extension`.
