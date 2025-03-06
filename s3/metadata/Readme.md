## Create a bucket

aws s3 mb s3://metadata-fun-fd

### Create a new file

echo "Hello Francklin" > hello.txt

## Upload file with metadata

aws s3api put-object --bucket  metadata-fun-fd --key hello.txt --body
hello.txt --metadata Name=Francklin

## Get Metadata through head object

aws s3api head-object --bucket  metadata-fun-fd --key hello.txt 

## Cleanup

aws s3 rm  s3://metadata-fun-fd/hello.txt
aws s3 rb  s3://metadata-fun-fd