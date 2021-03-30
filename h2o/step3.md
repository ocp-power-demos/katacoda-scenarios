Let's now deploy the H2O Container.

Cloning the repository

`git clone https://github.com/ocp-power-demos/h2o_on_ocp`{{execute}}

This repository contains the service and deployment configuration files that can be used as-is on the OpenShift or any Kubernetes platform.

Change Directory

`cd h2o_on_ocp`{{execute}}

Create a new `Project`

`oc new-project sample `{{execute}}

Deploy the application

`oc create -f  h2o-service.yaml; oc create -f h2o-deployment.yaml `{{execute}}

Check status of Pods

`oc get pods `{{execute}}

Assuming pods have successfully started, let us now login into the container via : (Ensure to replace <podman with the podname from the previous output>)

`oc rsh <podname>`
Running an example to ensure that the H2O application is up and running via:
`ls `{{execute}}
`./run_example.sh `{{execute}}
