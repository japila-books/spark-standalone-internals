# ExecutorRunner

## Creating Instance

`ExecutorRunner` takes the following to be created:

* <span id="appId"> Application ID
* <span id="execId"> Executor ID
* <span id="appDesc"> `ApplicationDescription`
* <span id="cores"> Number of CPU cores
* <span id="memory"> Amount of Memory
* <span id="worker"> `RpcEndpointRef`
* <span id="workerId"> Worker ID
* <span id="webUiScheme"> web UI's scheme
* <span id="host"> Host
* <span id="webUiPort"> web UI's port
* <span id="publicAddress"> Public Address
* <span id="sparkHome"> Spark's Home Directory
* <span id="executorDir"> Executor's Directory
* <span id="workerUrl"> Worker's URL
* <span id="conf"> `SparkConf`
* <span id="appLocalDirs"> Local Directories of the Spark Application
* <span id="state"> Executor State
* <span id="resources"> `Map[String, ResourceInformation]` (default: empty)

`ExecutorRunner` is created when:

* `Worker` is requested to handle a [LaunchExecutor](Worker.md#LaunchExecutor) message
