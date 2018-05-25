# test-kompose
Kompose test docker-compose file

## Example instructions 

### Create a project
oc new-project rtview-dataserver-sp

### Bring up our configuration
kompose --provider openshift up

### See what he have created 
oc get dc,svc,is,pvc,routes

### Force a restart of rtview-dataserver-spvy updating a deployment config 
oc set-env dc/rtview-dataserver-sp RESTART=1

### Bring down (and remove) our configuration 
kompose --provider openshift down

### Delete the project 
oc delete project rtview-dataserver-sp

### See the individual resources used in our configuration in openshift 
kompose --provider openshift convert



