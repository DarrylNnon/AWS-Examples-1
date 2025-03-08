## Create a new bucket

```sh
aws s3api create-bucket --bucket acl-example-fd --region us-east-1
```
 -[https://docs.aws.amazon.com/cli/](https://docs.aws.amazon.com/cli/latest/reference/s3api/create-bucket.html)

## Turn of Block Public Access for ACLs

```sh
aws s3api put-public-access-block \
--bucket acl-example-fd \
--public-access-block-configuration "BlockPublicAcls=false,IgnorePublicAcls=false,BlockPublicPolicy=true,RestrictPublicBuckets=true"
```
-[https://docs.aws.amazon.com/cli/](https://docs.aws.amazon.com/cli/latest/reference/s3api/put-public-access-block.html#examples)

```sh
aws s3api get-public-access-block --bucket acl-example-fd
```

## Change Bucket Ownership


```sh
aws s3api put-bucket-ownership-controls \
--bucket acl-example-fd \
--ownership-controls="Rules=[{ObjectOwnership=BucketOwnerPreferred}]"
```

## Change ACLs to allow for a user in another AWS Account

```sh
aws s3api put-bucket-acl \
--bucket acl-example-fd \
--access-control-policy file:///workspace/AWS-Examples/s3/acls/policy.json
```

## Access Bucket from other account

```sh
touch bootcamp.txt
aws s3 cp bootcamp.txt s3://acl-example-fd
aws s3 ls s3://acl-example-fd
```

## Cleanup

```sh
aws s3 rm s3://acl-example-fd/bootcamp.txt
aws s3 rb s3://acl-example-fd
```