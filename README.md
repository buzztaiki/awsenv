# awsenv

Set AWS environment variables and execute.

## Usage


```
run command with my-profle:
  awsenv -p my-profile env | grep AWS_ACCESS_KEY_ID

run command with default profile (or AWS_PROFILE):
  awsenv env | grep AWS_ACCESS_KEY_ID

export AWS_PROFILE environment variable with my-profile
  eval $(awsenv -ep my-profile)

export credential  environment variables with my-profile
  eval $(awsenv -Ep my-profile)
```

## License

MIT
