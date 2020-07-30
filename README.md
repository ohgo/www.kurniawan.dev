# www.kurniawan.dev

Source for my personal homepage [kurniawan.dev](https://kurniawan.dev).

Deploy
```shell script
aws cloudformation deploy \
  --stack-name "ku-www" \
  --template-file "site.yml" \
  --parameter-overrides $(cat "site.params" | tr '\n' ' ') \
  --capabilities CAPABILITY_NAMED_IAM \
  --no-fail-on-empty-changeset
```

Upload
```shell script
aws s3 sync ../src s3://kurniawan.dev
```