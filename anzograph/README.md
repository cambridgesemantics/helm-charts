# CSI AnzoGraph Chart
AnzoGraph is a massively parallel distributed native graph database built to query and interactively analyze trillions of relationships and is in production at large enterprise customers using the W3C’s RDF and the associated SPARQL query language, plus over 90 extensions for business intelligence. AnzoGraph (previously known as Anzo Graph Query Engine) has been deployed as an integral component of Anzo Smart Data Lake® supporting enterprise knowledge graphs, drug discovery, pharmacovigilance, fraud analytics, sales analytics, and risk analysis, among many other use cases.

# Chart Details
## Installing the Chart

To install the charts with release name csi-anzograph execute following helm command:
```sh
$ helm install --name <release-name> -f values.yaml .
```
This will deploy the single POD anzograph on targetted kubernetes cluster with default configurations. 
> Note that you need at least xx GB of RAM, xx number of CPUs. These resource parameters can be customised by editing values.yaml or by providing 'CsiAnzograph.LeaderNode.Resources.Cpu' and 'CsiAnzograph.LeaderNode.Resources.Memory' params at the time of deployment

## Configuration
The following table lists the configurable parameters of the anzograph chart and their default values

| Parameter                                   | Description                                                | Default                                                        |
|---------------------------------------------|------------------------------------------------------------|----------------------------------------------------------------|
| `CsiAnzograph.image`                        | AnzoGraph image                                            | docker.io/cambridgesemantics/anzograph:latest                  |
| `CsiAnzograph.imagePullPolicy`              | Pull policy for the images                                 | IfNotPresent                                                   |
| `CsiAnzograph.Resources.Cpu`                | Resource request for anzograph POD, number of CPUs         | 4000m                                                          |
| `CsiAnzograph.Resources.Memory`             | Resource request for anzograph POD,  memory size in MB     | 7000Mi                                                         |
| `AnzographUICredentials.UIAdminUser`        | AnzoGraph frontend administrator user name                 | admin                                                          |
| `AnzographUICredentials.UIAdminPassword`    | AnzoGraph frontend administrator user login password       | Passw0rd1                                                      |
| `AnzographUICredentials.QUERYUser`           | AnzoGraph frontend query user name                         | query                                                          |
| `AnzographUICredentials.QUERYUserPassword`  | AnzoGraph frontend query user login password               | Passw0rd2                                                      |
| `AnzographUICredentials.user_cert_path`     | AnzoGraph UI access certificate file path                  | ""                                                             |
| `AnzographUICredentials.user_key_path`      | AnzoGraph UI access certificate key file path              | ""                                                             |
| `AnzographUICredentials.user_ca_cert_path`  | AnzoGraph UI access ca certificate file path               | ""                                                             |
| `AnzographUIService.Ports.Jetty_Http.Port`  | AnzoGraph UI access port configured on the POD             | 80                                                         |
| `AnzographUIService.Ports.Jetty_Http.TargetPort` | AnzoGraph UI access port configured on the Service         | 8080                                                            |

Next release details:

Reference:


