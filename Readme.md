# Scope

We currently test the performance of the following requests:

```
read-resource-description(access-control=trim-descriptions, operations=true, recursive-depth=2)
```

(The requests are embedded within the test plan, base64 encoded.)

At the moment, three target resources are considered. 

- /subsystem=jgroups
- /susbystem=datasources
- /subsystem=jacorb

# Setup / Prerequisites

## JMeter

Get and install JMeter: http://jmeter.apache.org/download_jmeter.cgi

## Update the HTTP Auth Manager Settings

Open the RBAC.jmx test plan and update the AuthManager settings to reflect your server login.

## Start a server using the full-ha configuration

```
./bin/standalone.sh --server-config=standalone-full-ha.xml
```



