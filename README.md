# custom-jenkins

If using minishift, launch the virtual machine with extra memory (default 1GB isn't enough)
  * `minikube start --memory 8192`

Create imagestream
  * `oc create imagestream custom-jenkins`

Create the resources. For a quick setup, you can create them all from the following file
  * `oc create -f builds/jenkins-full.yml`

Build the image
  * `oc start-build custom-jenkins-build`
