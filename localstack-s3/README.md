## Health
  - http://localhost:4566/health

## Profile
```
[your_profile]
aws_access_key_id = foobar
aws_secret_access_key = foobar
region = eu-west-1
```


## Run container
```bash
$ docker-compose up
```

## Create bucket
```bash
$ aws --endpoint-url=http://localhost:4566 s3 mb s3://yourbucket --profile your_profile
```

## Upload file
```bash
$ aws --endpoint-url=http://localhost:4566 s3 cp lorem.txt s3://yourbucket --profile your_profile
```

## List file
```bash
$ aws --endpoint-url=http://localhost:4566 s3 ls s3://yourbucket --profile your_profile
```

## Count objects
```bash
$ aws --endpoint-url=http://localhost:4566 s3 ls s3://yourbucket --recursive --summarize --profile your_profile
```

## List buckets
```bash
$ aws --endpoint-url=http://localhost:4566 s3api list-buckets --profile your_profile
```