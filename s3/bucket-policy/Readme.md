## Create a bucket

aws s3 mb s3://bucket-policy-example-fd

## Create bucket policy

aws s3api put-bucket-policy --bucket bucket-policy-example-fd --policy file://policy.json

-[https://docs.aws.amazon.com/cli/latest/](https://docs.aws.amazon.com/cli/latest/reference/s3api/put-bucket-policy.html#examples)

# In the other account access the bucket

touch bootcamp.txt
aws s3 cp bootcamp.txt s3://bucket-policy-example-fd
aws s3 ls s3://bucket-policy-example-fd


## Cleanup

aws s3 rm s3://bucket-policy-example-fd/bootcamp.txt
aws s3 rb s3://bucket-policy-example-fd