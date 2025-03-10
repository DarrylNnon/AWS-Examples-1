## Create a bucket

aws s3 mb s3://encrypt-client-fun-fd


## create a file

echo "Hello Francklin!" > hello.txt

### Run our our SDK ruby script

bundle init # to intialize
bundle install
bundle exec ruby encrypt.rb


# Cleanup 

aws s3 rm s3://encrypt-client-fun-fd/hello.txt
aws s3 rb s3://encrypt-client-fun-fd
