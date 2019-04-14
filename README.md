# awsenv

Set AWS credential environment variables and execute.

## Requirements

- https://github.com/aws/aws-cli
- https://github.com/stedolan/jq


## Features

- Run command with specified profile's session credentials.
- Export credentials to environment variables.
- Assume role with MFA.
- Cache credentials.

## Usage


Run a command with my-profle:

```
% awsenv -p my-profile aws sts get-caller-identity
```

Run a command with my-profle no cache:

```
% awsenv -Cp my-profile aws sts get-caller-identity
```

Export credential environment variables with my-profile:

```
% eval $(awsenv -p my-profile)
```

If you use the fish shell:

```
% awsenv -p my-profile | source -
```

To see full options, run `awsenv -h`.


## Configuration

You can set token_duration per profile in ~/.aws/config as follows:

```
[profile my-profile]
token_duration=43200
```

## License

MIT
