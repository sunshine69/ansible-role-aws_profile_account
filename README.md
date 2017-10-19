# aws_profile_account

aws_profile_account allows an AWS instance_profile that has already used STS to assume
one role to assume an entirely different role

This allows a CI user that might be assuming a role in one AWS account to perform an operation
in another AWS account.

## Variables

### Input
* `aws_profile_account_role_arn` - ARN of role to assume
* `aws_profile_account_role_session_name` - temporary session name to distinguish role usage
* `aws_profile_account_region` - region of the role

### Output
* `aws_profile_account_sts_credentials` - contains an `sts_creds` dict with `access_key`, `secret_key`
  and `security_token`
