# NiFi-Custom-Processors-AltFetchS3Object
Checks for the existence of an S3 file without erroring out if it does not exist. Existence status is returned in the attribute s3.exist.

Three new properties are available to set:
1.	Include-content
o	Retrieve file contents
o	Default is True
2.	Bulletin
o	Invoke a bulletin if file does not exist
o	Default is False
3.	Penalize
o	Penalize flow if file does not exist
o	Default is False


Five new S3 attributes are set during runtime: 
•	s3.key 		(key name)
•	s3.exist 		(Boolean value of key existence)
•	s3.message 		(success message or failure reason)
•	s3.messagetype 	(exception type if failure)
•	s3.statuscode 	(HTTP status code if failure)

