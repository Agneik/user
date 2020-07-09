# UPAXER SLS COGNITO SECURITY

Repositorio que incluye los servicios para la implementación de cognito.

## Prerequisitos

Instalar **Flask, Oracle y Boto3**

```bash
pip install Flask flask_cors
pip install cx_Oracle
pip install boto3
```

Para hacer deploy en AWS, mediante el framework [serverless](https://serverless.com/)

```bash
npm install -g serverless
```

Configura credenciales de AWS

```bash
serverless config credentials --provider aws --key YOUR_KEY_ID --secret YOUR_SECRET_KEY --profile PROFILE
```

Instala plugins de serverless

```bash
sls plugin install -n serverless-wsgi --env ENTORNO --domain DOMINIO

sls plugin install -n serverless-python-requirements --env ENTORNO --domain DOMINIO

npm i serverless-deployment-bucket

npm i serverless-domain-manager
```

## Deploy

#### Local Deployment
```bash
sls wsgi serve
```

#### AWS Deployment
```bash
sls deploy --aws-profile YOUR_PROFILE --env ENTORNO --domain DOMINIO
```

Sintáxis en archivo **serverless.yml**

**service**: upx-sls-servicename

**deploymentBucket** name: upax-serverless-api

**apiName**: upx-sls-servicename-API

**stackName**: upx-sls-servicename-cloudformation  
