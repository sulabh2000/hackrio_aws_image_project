# hackrio_aws_image_project

Compress image Using s3 and lambda.

I have used aws cli and git bash on my windows 10.

Aws Bucket:-
1. I have created two buckets, one for image upload and second for resized image.

Execution role:-
1. I have provided an execution role role to lambda function.

Lambda service:-
aws lambda create-function --function-name CreateThumbnail \
--zip-file fileb://function.zip --handler index.handler --runtime nodejs12.x \
--timeout 10 --memory-size 1024 \
--role arn:aws:iam::123456789012:role/lambda-s3-role


aws lambda invoke --function-name CreateThumbnail --invocation-type Event \
--payload file://inputFile.txt outputfile.txt


making use of these two commands


