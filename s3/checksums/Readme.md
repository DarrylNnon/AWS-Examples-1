## Create a new s3 bucket

```md
aws s3 mb s3://checksums-examples-fd
```

## Create a file that will we do a checksum on

```
echo "Hello Francklin" > myfile.txt
```

## Get a checksum of a file for md5

```md
md5sum myfile.txt 
# b3d3da281f89554bfc9a2a29dc90e4aa myfile.txt
```

## Upload our file and look at its etag

```
aws s3 cp myfile.txt s3://checksums-examples-fd
aws s3api head-object --bucket checksums-examples-fd --key myfile.txt
```

## Lets upload a file with a different kind of checsum


```sh
bundle init # to initialize ruby and create a gemgile we add zlib into gem
bundle install to install ruby
bundle exec ruby crc.rb
```
```sh
sudo apt install rhash -y
rhash --crc32 --simple myfile.txt
```

Using a script
```sh
bundle exec ruby crc.rb
```

using a library
```sh
sha1sum myfile.txt 
```

```sh
aws s3api put-object \
--bucket="checksums-examples-fd" \
--key="myfilesha1.txt" \
--body="myfile.txt" \
--checksum-algorithm="SHA1" \
--checksum-sha1="OTNmOTYwMTgyZTg1YjlmNmIyMjBiMThlNzNlNGI1Y2ZmYzhiYzgzMw=="
```