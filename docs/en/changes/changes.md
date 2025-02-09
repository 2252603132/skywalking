## 9.5.0

#### Project

* Fix `Duplicate class found` due to the `delombok` goal.

#### OAP Server

* Fix wrong layer of metric `user error` in DynamoDB monitoring.
* ElasticSearch storage does not check field types when OAP running in `no-init` mode.
* Support to bind TLS status as a part of component for service topology.
* Fix component ID priority bug.
* Fix component ID of topology overlap due to storage layer bugs.
* [Breaking Change] Enhance JDBC storage through merging tables and managing day-based table rolling.
* [Breaking Change] Sharding-MySQL implementations and tests get removed due to we have the day-based rolling mechanism by default
* Fix otel k8s-cluster rule add namespace dimension for MAL aggregation calculation(Deployment Status,Deployment Spec Replicas)
* Support continuous profiling feature.
* Support collect process level related metrics.
* Fix K8sRetag reads the wrong k8s service from the cache due to a possible namespace mismatch.
* [Breaking Change] Support cross-thread trace profiling. The data structure and query APIs are changed.

#### UI
* Revert: cpm5d function. This feature is cancelled from backend.
* Fix: alerting link breaks on the topology.
* Refactor Topology widget to make it more hierarchical.
  1. Choose `User` as the first node.
  2. If `User` node is absent, choose the busiest node(which has the most calls of all).
  3. Do a left-to-right flow process.
  4. At the same level, list nodes from top to bottom in alphabetical order.

#### Documentation


All issues and pull requests are [here](https://github.com/apache/skywalking/milestone/169?closed=1)
