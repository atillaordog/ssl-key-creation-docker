# SSL key creation Docker file

This Dockerfile has the role to create SSL key for use in a docker-compose environment, for example if random keys are needed in test environments, it can create the key upon cluster start. It also creates PEM file and a Java keystore.

# Usage
Simply run 
```
docker-compose -f example.yml up
```
and if all is good, a keys folder should appear with all the keys generated.

## Arguments

You can pass these arguments:

|Argument|Default value|Description|
|-|-|-|
|ARG KEYINIT_KEY_NAME|certificate|Used for the name of the generated files|
|ARG KEYINIT_KEYTORE_NAME|keystore|Name for the java keystore|
|ARG KEYINIT_KEYSTORE_PASSWORD|password|Password or the keystore|
|ARG KEYINIT_KEYSTORE_ALIAS|mykeystore|Alias used in the keystore|
|ARG KEYINIT_KEYGEN_COUNTRY_CODE|US|Country code used in the subject|
|ARG KEYINIT_KEYGEN_STATE|Denial|State used in the subject|
|ARG KEYINIT_KEYGEN_LOCATION|Springfield|Location used in the subject|
|ARG KEYINIT_KEYGEN_ORGANIZATION|Dis|Organization name in the subject|
|ARG KEYINIT_KEYGEN_CN|test|Common name in the subject|
|ARG KEYINIT_ALTERNATIVE_NAMES_DNS|test|DNS entry in the subject alt names|
|ARG KEYINIT_ALTERNATIVE_NAMES_IP|127.0.0.1|IP entry in the subject alt names|