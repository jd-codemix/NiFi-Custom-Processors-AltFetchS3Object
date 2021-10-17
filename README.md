# NiFi-Custom-Processors-AltFetchS3Object
Retrieves the contents of an S3 Object,  only if the S3 Object exist, and writes it to the content of a FlowFile. 
Several custom S3 attributes are set. Three new custom properties such as (bulletin, penalize and include-content) are available to set.


New Custom Attributes: 
s3.exist: Boolean (true/false) value of S3 key existance
s3.message: Exception reason
s3.messagetype: Exception type
s3.statuscode: HTTP status code

New Custom Properties:
bullentin: only except True/False value. True will involk a bullentin if the file does not exist. False will not involk a bullentin. The custom attribute 's3.exist' will be set to true or false.
penalize: only except True/False value. True will involk a penalization if the file does not exist. False will not involk a penalization.
include-content: only except True/False value. If True, fetch file content if file exist. If False, will not fetch file content. Mainly used in conjunction with Attribute 's3.exist' to check if a file exist but don't need the content.
