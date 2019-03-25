# awsenv

Set AWS environment variables and execute.

## Usage


```
Run a command with my-profle:
  awsenv -p my-profile aws sts get-caller-identity

Run a command with my-profle no cache:
  awsenv -Cp my-profile aws sts get-caller-identity

Run a command with my-profle and token duration:
  awsenv -Cp my-profile -d 7200 aws sts get-caller-identity

Export credential environment variables with my-profile:
  eval $(awsenv -ep my-profile)

If you use the fish shell:
  awsenv -ep my-profile | source -
```


## Configuration

```
You can token_duration in ~/.aws/config as follows:

[profile my-profile]
token_duration=43200
```

## License

MIT
