# nodejs-wrapper-opsworks
A wrapper around redguide/nodejs that installs Node 0.12.0 on AWS OpsWorks

# Usage

To use these with OpsWorks do the following:

* Add this cookbook to your cookbooks repository
* Add the redguide/nodejs cookbook as a dependency in your Berksfile
* Create a "Custom Layer" in OpsWorks
* Add the following custom recipes to your layer:
  * Setup: nodejs-wrapper-opsowrks, nodejs-wrapper-opsworks::create-symlink
  * Configure: opsworks_nodejs::configure
  * Deploy: nodejs, deploy::nodejs
  * Undeploy: deploy::nodejs-undeploy
  * Shutdown: deploy::nodejs-stop
