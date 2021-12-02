# Compute

## Metrics

This is the `compute` dataset.

An example event for `compute` looks as following:

```json
{
    "@timestamp": "2017-10-12T08:05:34.853Z",
    "cloud": {
        "account": {
            "id": "elastic-observability",
            "name": "elastic-observability"
        },
        "instance": {
            "id": "1113015278728017638",
            "name": "gke-apm-ci-k8s-cluster-pool-2-e8852348-58mx"
        },
        "provider": "gcp",
        "availability_zone": "us-central1-c",
        "region": "us-central1"
    },
    "event": {
        "dataset": "gcp.compute",
        "duration": 115000,
        "module": "gcp"
    },
    "gcp": {
        "compute": {
            "instance": {
                "disk": {
                    "read_bytes_count": {
                        "value": 989296850
                    },
                    "read_ops_count": {
                        "value": 14862
                    },
                    "write_bytes_count": {
                        "value": 1323095
                    },
                    "write_ops_count": {
                        "value": 105
                    }
                }
            }
        },
        "labels": {
            "metrics": {
                "device_name": "gke-apm-ci-k8s-cluster-pool-2-e8852348-58mx",
                "device_type": "permanent",
                "storage_type": "pd-standard"
            }
        }
    },
    "host": {
        "disk": {
            "read": {
                "bytes": 989296850
            },
            "write": {
                "bytes": 1323095
            }
        },
        "id": "1113015278728017638",
        "name": "gke-apm-ci-k8s-cluster-pool-2-e8852348-58mx"
    },
    "metricset": {
        "name": "compute",
        "period": 10000
    },
    "service": {
        "type": "gcp"
    }
}
```

**Exported fields**

| Field | Description | Type |
|---|---|---|
| @timestamp | Event timestamp. | date |
| cloud | Fields related to the cloud or infrastructure the events are coming from. | group |
| cloud.account.id | The cloud account or organization id used to identify different entities in a multi-tenant environment. Examples: AWS account id, Google Cloud ORG Id, or other unique identifier. | keyword |
| cloud.account.name | The cloud account name or alias used to identify different entities in a multi-tenant environment. Examples: AWS account name, Google Cloud ORG display name. | keyword |
| cloud.availability_zone | Availability zone in which this host is running. | keyword |
| cloud.image.id | Image ID for the cloud instance. | keyword |
| cloud.instance.id | Instance ID of the host machine. | keyword |
| cloud.instance.name | Instance name of the host machine. | keyword |
| cloud.machine.type | Machine type of the host machine. | keyword |
| cloud.project.id | Name of the project in Google Cloud. | keyword |
| cloud.provider | Name of the cloud provider. Example values are aws, azure, gcp, or digitalocean. | keyword |
| cloud.region | Region in which this host, resource, or service is located. | keyword |
| container.id | Unique container id. | keyword |
| container.image.name | Name of the image the container was built on. | keyword |
| container.labels | Image labels. | object |
| container.name | Container name. | keyword |
| data_stream.dataset | Data stream dataset. | constant_keyword |
| data_stream.namespace | Data stream namespace. | constant_keyword |
| data_stream.type | Data stream type. | constant_keyword |
| ecs.version | ECS version this event conforms to. `ecs.version` is a required field and must exist in all events. When querying across multiple indices -- which may conform to slightly different ECS versions -- this field lets integrations adjust to the schema version of the events. | keyword |
| error | These fields can represent errors of any kind. Use them for errors that happen while fetching events or in cases where the event itself contains an error. | group |
| error.message | Error message. | match_only_text |
| event.dataset | Event dataset | constant_keyword |
| event.module | Event module | constant_keyword |
| gcp.compute.instance.cpu.reserved_cores.value | Number of cores reserved on the host of the instance | double |
| gcp.compute.instance.cpu.usage_time.value | Usage for all cores in seconds | double |
| gcp.compute.instance.cpu.utilization.value | The fraction of the allocated CPU that is currently in use on the instance | double |
| gcp.compute.instance.disk.read_bytes_count.value | Count of bytes read from disk | long |
| gcp.compute.instance.disk.read_ops_count.value | Count of disk read IO operations | long |
| gcp.compute.instance.disk.write_bytes_count.value | Count of bytes written to disk | long |
| gcp.compute.instance.disk.write_ops_count.value | Count of disk write IO operations | long |
| gcp.compute.instance.firewall.dropped_bytes_count.value | Incoming bytes dropped by the firewall | long |
| gcp.compute.instance.firewall.dropped_packets_count.value | Incoming packets dropped by the firewall | long |
| gcp.compute.instance.memory.balloon.ram_size.value | The total amount of memory in the VM. This metric is only available for VMs that belong to the e2 family. | long |
| gcp.compute.instance.memory.balloon.ram_used.value | Memory currently used in the VM. This metric is only available for VMs that belong to the e2 family. | long |
| gcp.compute.instance.memory.balloon.swap_in_bytes_count.value | The amount of memory read into the guest from its own swap space. This metric is only available for VMs that belong to the e2 family. | long |
| gcp.compute.instance.memory.balloon.swap_out_bytes_count.value | The amount of memory written from the guest to its own swap space. This metric is only available for VMs that belong to the e2 family. | long |
| gcp.compute.instance.network.received_bytes_count.value | Count of bytes received from the network | long |
| gcp.compute.instance.network.received_packets_count.value | Count of packets received from the network | long |
| gcp.compute.instance.network.sent_bytes_count.value | Count of bytes sent over the network | long |
| gcp.compute.instance.network.sent_packets_count.value | Count of packets sent over the network | long |
| gcp.compute.instance.uptime.value | How long the VM has been running, in seconds | long |
| host.architecture | Operating system architecture. | keyword |
| host.containerized | If the host is a container. | boolean |
| host.domain | Name of the domain of which the host is a member. For example, on Windows this could be the host's Active Directory domain or NetBIOS domain name. For Linux this could be the domain of the host's LDAP provider. | keyword |
| host.hostname | Hostname of the host. It normally contains what the `hostname` command returns on the host machine. | keyword |
| host.id | Unique host id. As hostname is not always unique, use values that are meaningful in your environment. Example: The current usage of `beat.name`. | keyword |
| host.ip | Host ip addresses. | ip |
| host.mac | Host mac addresses. | keyword |
| host.name | Name of the host. It can contain what `hostname` returns on Unix systems, the fully qualified domain name, or a name specified by the user. The sender decides which value to use. | keyword |
| host.os.build | OS build information. | keyword |
| host.os.codename | OS codename, if any. | keyword |
| host.os.family | OS family (such as redhat, debian, freebsd, windows). | keyword |
| host.os.kernel | Operating system kernel version as a raw string. | keyword |
| host.os.name | Operating system name, without the version. | keyword |
| host.os.platform | Operating system platform (such centos, ubuntu, windows). | keyword |
| host.os.version | Operating system version as a raw string. | keyword |
| host.type | Type of host. For Cloud providers this can be the machine type like `t2.medium`. If vm, this could be the container, for example, or other information meaningful in your environment. | keyword |
| service.type | The type of the service data is collected from. The type can be used to group and correlate logs and metrics from one service type. Example: If logs or metrics are collected from Elasticsearch, `service.type` would be `elasticsearch`. | keyword |