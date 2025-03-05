# etags (entity tag)
it is way to look for changes into resources whitout the need to dowload

```sh
- create a main.tf
- create a file call myfile.txt
- terraform init # to initialize the configuration
- terraform plan to see the backend change
- terraform apply --auto-approve# to apply the changes
- aws s3api list-buckets --query BUCKETS --output table # to visualise the bucket in a table
- aws s3 ls s3://terraform-20250305093714187700000001 # to see the object files
- aws s3 cp s3://terraform-20250305093714187700000001/myfile.txt myfile.txt | cat # to dowload it.
- aws s3 cp s3://terraform-20250305093714187700000001/myfile.txt - && cat - # to see the object content.
```

