# gpaws

AWS CLI wrapper using GPG encrypted credentials

## Usage

### Executing a single CLI command

It will look for `~/.aws/credentials.gpg` file and try to decrypt it. It should contain `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY` separated by a space.

Simply invoke `gpaws` instead `aws`.

Example:

```
gpaws s3 list-buckets 
```

### Storing decrypted credentials in environment variables

If you plan to execute multiple commands, it might be more comfortable to decrypt credentials and store them in environment variables.

Source _gpaws_ invoked without arguments.

```
source gpaws
```

Remember, that decrypted credentials will be available to any process from now on.