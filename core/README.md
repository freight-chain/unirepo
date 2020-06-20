#
# api template refs


sequences:immutable;
class:str
class:bytes

sequences:mutable;
class:list
class:bytearray


[boxes] == class
{$} == api call 
refs/tags/{$}
[refs]/[heads]/{$}

# Git

## git file dir struct 

_corporate-entity_/-/repository/module/component/

-/repository/module/component/
-/repositorypackages/component/
-/repository/module/plugin/
repository/build
repository/registry
repository/lib
repository/schema
repository/core*reserved*
repository/scm [git sub modules]
repository/logic*reserved*
repository/kernel *reserved*
repository/interfaces *reserved*


entity/module-component

e.g.

freight-trust/docker-elk

## templating 

> Handlebar Templates

Template:

Shown.
{{#person}}
  Never shown!
{{/person}}
Hash:

{
  "person": false
}
Output:

Shown.


### templating spec

refs/heads/{branch-name}
pr-{pull-request}
refs/tags/{git-tag}
{git-tag}
{path}/Dockerfile


# RegEx 

arn:partition:service:region:account-id:resource-id
arn:partition:service:region:account-id:resource-type/resource-id
arn:partition:service:region:account-id:resource-type:resource-id

--->
~~~
^arn:(?P<Partition>[^:\n]*):(?P<Service>[^:\n]*):(?P<Region>[^:\n]*):(?P<AccountID>[^:\n]*):(?P<Ignore>(?P<ResourceType>[^:\/\n]*)[:\/])?(?P<Resource>.*)$
~~~
A pattern to parse Amazon Web Services ARNs into their varying components:

Partition
Service
Region
AccountID
ResourceType (optional - empty string is missing)
Resource
<----


` ^us-[a-z]*-[0-9]{1} `



## module-component structure 

- .ci-cd/actions
|
- src
- dist
- var
- tests
- docs
- schema
- lib
- etc



### Key:Value for Tags
[key:value]

entity:service
group:purpose
service:instance_purpose

corporate:graylog2
devops:logging
graylog2:webapp_logging

[module:core]
[toolchain:devops]

[module]
## Core
https://github.com/archimatetool/archi.git

[module]
### API
https://github.com/JustinFeng/fakeit.git


[module]
### Branding
https://github.com/rodi01/RenameIt.git
https://github.com/andrewfiorillo/sketch-palettes.git
https://github.com/mathieudutour/git-sketch-plugin.git
https://github.com/Ashung/Automate-Sketch.git

[module]
### Docker
<!-- https://github.com/Graylog2/graylog2-images.git --> 


## Toolchain
https://github.com/restyled-io/restyler.git

[toolchain:devops]
https://github.com/awslabs/aws-shell.git

<!-- ### toolchain:smithy 

https://github.com/awslabs/smithy-gradle-plugin.git
https://github.com/awslabs/smithy.git
--> 


## Corporate Services
https://github.com/awslabs/aws-iam-generator.git

https://github.com/all-contributors/all-contributors.git

Java
https://github.com/zulu-openjdk/zulu-openjdk.git


LDAP:
https://github.com/keycloak/keycloak-operator.git

Apposody:
https://github.com/appsody/appsody-operator.git

Postgres:
https://github.com/CrunchyData/postgres-operator.git

SysAdmin
https://github.com/duo-labs/cloudmapper.git

Performaant
https://github.com/HdrHistogram/HdrHistogram
https://github.com/LatencyUtils/LatencyUtils.git
https://github.com/giltene/jHiccup

Kube
https://github.com/kinvolk/lokomotive.git
https://github.com/kinvolk/inspektor-gadget.git
https://github.com/kinvolk/flatcar-linux-update-operator.git
https://github.com/kinvolk/headlamp.git
https://github.com/walmartlabs/kubeman

IAAS
https://github.com/poseidon/terraform-provider-ct.git [lokomotive, depen]

Prometheus
https://github.com/prometheus/node_exporter


### KPIs

producibility
provability
recoverability
relevance
reliability
repeatability
reproducibility
resilience
installability
integrity
interchangeability
distributability
durability
effectiveness
efficiency
evolvability
extensibility
failure transparency
fault-tolerance
fidelity
accessibility
accountability
accuracy
adaptability
administrability
affordability