# StandaloneSchedulerBackend

`StandaloneSchedulerBackend` is a `CoarseGrainedSchedulerBackend`.

## Creating Instance

`StandaloneSchedulerBackend` takes the following to be created:

* <span id="scheduler"> `TaskSchedulerImpl`
* <span id="sc"> `SparkContext`
* <span id="masters"> Standalone master URLs

`StandaloneSchedulerBackend` is created when:

* `SparkContext` is requested for a `SchedulerBackend` (and `TaskScheduler`) (for `spark://` and `local-cluster` master URLs)

## <span id="StandaloneAppClientListener"> StandaloneAppClientListener

`StandaloneSchedulerBackend` is a [StandaloneAppClientListener](StandaloneAppClientListener.md).

## <span id="start"> Starting SchedulerBackend

```scala
start(): Unit
```

`start`...FIXME

`start` creates a [StandaloneAppClient](#StandaloneAppClient) and requests it to [start](StandaloneAppClient.md#start).

`start`...FIXME

`start` is part of the `SchedulerBackend` abstraction.

## <span id="client"><span id="StandaloneAppClient"> StandaloneAppClient

`StandaloneSchedulerBackend` creates a [StandaloneAppClient](StandaloneAppClient.md) (with itself as a [StandaloneAppClientListener](#StandaloneAppClientListener)) when requested to [start](#start).

`StandaloneAppClient` is [started](StandaloneAppClient.md#start) with [StandaloneSchedulerBackend](#start).

`StandaloneAppClient` is [stopped](StandaloneAppClient.md#stop) with [StandaloneSchedulerBackend](#stop).

`StandaloneAppClient` is used for the following:

* [doRequestTotalExecutors](#doRequestTotalExecutors)
* [doKillExecutors](#doKillExecutors)
