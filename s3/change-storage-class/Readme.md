## Create a bucket

aws s3 mb s3://class-fun-fd

## Create a file

echo "Hello Francklin" > hello.txt
aws s3 cp hello.txt s3://class-fun-fd --storage-class STANDARD_IA

## Cleanup

aws s3 rm s3://class-fun-fd/hello.txt
aws s3 rb s3://class-fun-fd