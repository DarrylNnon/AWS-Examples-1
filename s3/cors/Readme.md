# Cross-Origin Resource Sharing (CORS)definition

Cross-Origin Resource Sharing is an http-header based mechanism that allows a server to indicate any origins (domain, scheme, or port) than its own from which a browser should permit loading of resources.

# Create Website 1

## Create a bucket

```sh
aws s3 mb s3://cors-fun-fd
```

## Change block public access

```sh
aws s3api put-public-access-block \
--bucket cors-fun-fd \
--public-access-block-configuration "BlockPublicAcls=true,IgnorePublicAcls=true,BlockPublicPolicy=false,RestrictPublicBuckets=false"
```

## Create a bucket policy

```sh
aws s3api put-bucket-policy --bucket cors-fun-fd --policy file://bucket-policy.json
```

## Turn on static website hosting

```sh
aws s3api put-bucket-website --bucket cors-fun-fd --website-configuration file://website.json
```

## Upload our index.html file and include a resource that would be cross-origin

aws s3 cp index.html s3://cors-fun-fd

## Get the website enpoint for s3

aws s3api get-bucket-website --bucket cors-fun-fd

## View the website and see if the index.html is there.


It this for us-east-1
http://cors-fun-fd.s3-website.us-east-1.amazonaws.com

Other regions might use a hyphen instead
http://cors-fun-fd.s3-website-ca-central-1.amazonaws.com


# Create Website 2

```sh
aws s3 mb s3://cors-fun2-fd
```

## Change block public access

```sh
aws s3api put-public-access-block \
--bucket cors-fun2-fd \
--public-access-block-configuration "BlockPublicAcls=true,IgnorePublicAcls=true,BlockPublicPolicy=false,RestrictPublicBuckets=false"
```

## Create a bucket policy

```sh
aws s3api put-bucket-policy --bucket cors-fun2-fd --policy file://bucket-policy2.json
```

## Turn on static website hosting

```sh
aws s3api put-bucket-website --bucket cors-fun2-fd --website-configuration file://website.json
```

## Upload our javascript file

aws s3 cp hello.js s3://cors-fun2-fd

## Create API Gateway with mock response and then test the endpoint

curl -X POST -H "Content-Type: application/json" https://dee9zs9cn4.execute-api.us-east-1.amazonaws.com/prod/hello

#curl -X POST -H "Content-Type: application/json" https://1kccnjkm43.execute-api.#ca-central-1.amazonaws.com/prod/hello


## Set CORS on our bucket

aws s3api put-bucket-cors --bucket cors-fun-fd --cors-configuration file://cors.json