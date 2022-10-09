# nest-lambda-docker-container-surpport

This project show you how to deploy the Nestjs Backend app to Lambda the fastest using docker image.

---

## following steps

Before we start, we need docker and aws cli.
If it's not installed, please refer to the link below.

#### Ensure Docker CLI is installed: https://docs.docker.com/get-docker/

#### Ensure AWS CLI is installed: https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html

If the installation is complete, let's get started.

- `npm install serverless -g`
- insert command
  ```
  serverless config credentials \
    --provider aws \
    --key <INSERT YOUR ACCESS KEY> \
    --secret <INSERT YOUR SECRET KEY> \
    --profile lambda-docker
  ```
- pull "lambda nodejs:14" docker image
  ```
  docker pull public.ecr.aws/lambda/nodejs:14
  ```
- Come back to the nest-lambda-docker-container-surport project then add modules
  ```
  yarn add
  ```
- This is all!! Now Let's deploy!!
  ```
  sls deploy
  ```
- Wait a minute then you will Success deploy
  [Click Me!](https://vdgluh9uh8.execute-api.ap-northeast-2.amazonaws.com/dev/hello)

We deployed the Nestjs backend app using Lambda's newly added [Lambda docker container support](https://aws.amazon.com/ko/blogs/korea/new-for-aws-lambda-container-image-support/). This means that Nestjsapp can be operated in a **Serverless environment**, not in a Provisioning environment, a service such as AWS EC2. It also means that it can be distributed up to 10GB of capacity, which can **escape from the capacity limitations** of the existing ZIP method.

If you want more info please [vist my blog](https://velog.io/@ghdmsrkd/NestJS-App-deploy-with-lambda-docker-container-support-and-Serverless-Framwork)
