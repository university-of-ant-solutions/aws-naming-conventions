---
title: Virtual Private Cloud naming conventions
---

## Risk level

Low (generally tolerable level of risk)

Ensure that your AWS Virtual Private Clouds (VPCs) are using appropriate naming conventions for tagging in order to manage them more efficiently and adhere to AWS resource tagging best practices. A naming convention is a well-defined set of rules useful for choosing the name of an AWS resource. Cloud Conformity strongly recommends using the following pattern (default pattern) for naming your AWS VPCs: `^vpc-(ue1|uw1|uw2|ew1|ec1|an1|an2|as1|as2|se1)-(d|t|s|p)-([a-z0-9\-]+)$`. In case you need to create your custom naming pattern, the default one can be easily replaced within the rule configuration settings available on Cloud Conformity console.

Naming (tagging) your AWS VPCs consistently has several advantages such as providing additional information about the VPC location and usage, promoting consistency within the selected AWS region, distinguishing fast similar resource stacks from one another, avoiding naming collisions, improving clarity in cases of potential ambiguity and enhancing the aesthetic and professional appearance.

### Default Pattern Format

```
vpc-RegionCode-EnvironmentCode-ApplicationStackCode
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
([a-z0-9\-]+) for the application stack that runs within the VPC (e.g. bid-data-app-stack).
```

### Default Pattern Examples

```
vpc-us-east-1-p-bid-data-app-stack
vpc-us-west-2-p-web-app-stack
```

## Links

[vpc-naming-conventions](https://www.cloudconformity.com/conformity-rules/VPC/vpc-naming-conventions.html);