## Micronaut 2.4.0-SNAPSHOT Documentation

- [User Guide](https://docs.micronaut.io/snapshot/guide/index.html)
- [API Reference](https://docs.micronaut.io/snapshot/api/index.html)
- [Configuration Reference](https://docs.micronaut.io/snapshot/guide/configurationreference.html)
- [Micronaut Guides](https://guides.micronaut.io/index.html)
---

## Handler

[AWS Lambda Handler](https://docs.aws.amazon.com/lambda/latest/dg/java-handler.html)

Handler: io.micronaut.function.aws.proxy.MicronautLambdaHandler

## AWS Lambda Workflow (CLI)

Workflow file: [`.github/workflows/aws-lambda-cli-java.yml`](.github/workflows/aws-lambda-cli-java.yml)

### Workflow description
For pushes to the `master` branch, the workflow will:
1. Setup the build environment with respect to the selected java/graalvm version.
3. Login to [AWS CLI](https://aws.amazon.com/cli/).
4. Build micronaut application.
5. Deploy to [AWS Lambda](https://aws.amazon.com/lambda/).

### Dependencies on other GitHub Actions
- [Setup GraalVM `DeLaGuardo/setup-graalvm`](https://github.com/DeLaGuardo/setup-graalvm)
- [Configure AWS Credentials `aws-actions/configure-aws-credentials`](https://github.com/aws-actions/configure-aws-credentials)

### Setup
Add the following GitHub secrets:

| Name | Description |
| ---- | ----------- |
| AWS_ACCESS_KEY_ID | AWS Access Key Id. |
| AWS_SECRET_ACCESS_KEY | AWS Secret Access Key. |
| AWS_ROLE_ARN | AWS Role ARN under which the Lambda function runs. |

The workflow file also contains additional configuration options that are now configured to:

| Name | Description | Default value |
| ---- | ----------- | ------------- |
| FUNCTION_TIMEOUT | The amount of time that Lambda allows a function to run before stopping it. | `30` |
| FUNCTION_MEMORY | The amount of memory available to the function at runtime. | `512` |
| AWS_REGION | The AWS Region where the function is created. | `eu-central-1` |


### Verification

## Feature aws-lambda documentation

- [Micronaut AWS Lambda Function documentation](https://micronaut-projects.github.io/micronaut-aws/latest/guide/index.html#lambda)

## Feature http-client documentation

- [Micronaut HTTP Client documentation](https://docs.micronaut.io/latest/guide/index.html#httpClient)

