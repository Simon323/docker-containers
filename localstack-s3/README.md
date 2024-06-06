## Health
  - http://localhost:4566/health

## Profile
```
[your_profile]
aws_access_key_id = foobar
aws_secret_access_key = foobar
region = us-east-1
```


## Run container
```bash
$ docker-compose up
```

## Create bucket
```bash
$ aws --endpoint-url=http://localhost:4566 s3 mb s3://yourbucket --profile your_profile
$ aws --endpoint-url=http://localhost:4566 s3 mb s3://yourbucket --no-sign-request
```

## Upload file
```bash
$ aws --endpoint-url=http://localhost:4566 s3 cp lorem.txt s3://yourbucket --profile your_profile
$ aws --endpoint-url=http://localhost:4566 s3 cp lorem.txt s3://yourbucket --no-sign-request
```

## List file
```bash
$ aws --endpoint-url=http://localhost:4566 s3 ls s3://yourbucket --profile your_profile
$ aws --endpoint-url=http://localhost:4566 s3 ls s3://yourbucket --no-sign-request
$ aws --endpoint-url=http://localhost:4566 s3 ls s3://yourbucket --recursive --no-sign-request
```

## Count objects
```bash
$ aws --endpoint-url=http://localhost:4566 s3 ls s3://yourbucket --recursive --summarize --profile your_profile
$ aws --endpoint-url=http://localhost:4566 s3 ls s3://yourbucket --recursive --summarize --no-sign-request
```

## List buckets
```bash
$ aws --endpoint-url=http://localhost:4566 s3api list-buckets --profile your_profile
$ aws --endpoint-url=http://localhost:4566 s3api list-buckets --no-sign-request
```

## Sync files
```bash
$ aws --endpoint-url=http://localhost:4566 s3 sync local_folder s3://yourbucket --profile your_profile
$ aws --endpoint-url=http://localhost:4566 s3 sync local_folder s3://yourbucket ---no-sign-request
```