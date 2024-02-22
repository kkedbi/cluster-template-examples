# RKE2 cluster template

This project is a fork of https://github.com/rancher/cluster-template-examples/tree/main.

The purpose is to show an concrete example of a template for AWS EC2.

This project contains rke2 clustertemplate helm chart for AWS EC2, which can be applied with values.yaml as configurations to create clusters.

### How to use

The general cluster configuration options are available through [values.yaml](./charts/values.yaml).

To provide your own configuration, modify the original values.yaml and create your own version, and pass it to helm. For example:

```bash
helm package charts

helm repo index .
```

Once done, push your modification into your git repository and refresh your Rancher repo apps.

Then your updated template should be visible in Rancher when creating the cluster.


### Version control

The version control is implemented as helm release history and can easily be implemented by UI to provide operation history and rollback.

# License

Copyright (c) 2014-2021 [Rancher Labs, Inc.](http://rancher.com)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
