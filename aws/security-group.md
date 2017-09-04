---
title: Security Group naming conventions
---

## Risk level

Low (generally tolerable level of risk)

Ensure that all your EC2 security groups are using appropriate naming conventions for tagging in order to manage them more efficiently and adhere to AWS tagging best practices. A naming convention is a well-defined set of rules useful for choosing the name of an AWS resource. Cloud Conformity strongly recommends using the following pattern (default) for naming your security groups:
`^security-group-(ue1|uw1|uw2|ew1|ec1|an1|an2|as1|as2|se1)-(d|t|s|p)-([a-z0-9\-]+)$`. However, in case you need to create your custom naming pattern, the default one can be easily replaced within the rule settings available on Cloud Conformity console.

### Default Pattern Format

```
security-group-RegionCode-EnvironmentCode-ApplicationCode
```

### Default Pattern Components

#### RegionCode

```
(ue1|uw1|uw2|ew1|ec1|an1|an2|as1|as2|se1) for us-east-1, us-west-1, us-west-2, eu-west-1, eu-central-1, ap-northeast-1, ap-northeast-2, ap-southeast-1, ap-southeast-2, sa-east-1.
```

#### EnvironmentCode

```
(d|t|s|p) for development, test, staging, production.
```

#### ApplicationCode

```
([a-z0-9\-]+) for applications (e.g. nodejs, mongo) running on the instances associated with the selected security groups.
```

### Default Pattern Examples

```
security-group-us-east-1-p-mongo-elsticsearch
security-group-ap-northeast-1-p-tomcat
```

## Links

[security-group-naming-conventions](https://www.cloudconformity.com/conformity-rules/EC2/security-group-naming-conventions.html);