# Groupless AutoScaling with Karpenter #

## Traditional AutoScaling ( horizontal ) ##

* Manual Provisioning
* Cluster AutoScaler

### Benefits of Cluster AutoScaler
* Automatically grow the cluster to meet increased demands.
* Reduce infrastructure costs through efficient resource utilization and node termination.
* Vendor neutral with support for all major cloud providers.
* Widely adopted and battle tested approach.
* Works great for clusters sizes ~ 1000 nodes.

#### Node Group
* Well managed capacity templates.
* Mirroring the data center "Rack" model.
* Building upon existing layers in the cloud.

### Drawbacks
* Need separate node group diff type of instance.
* Doesn't work with custom scheduler.

### Groupless Node AutoScaling
Karpenter Allocator

#### Components
**Allocator**   - Fast Acting, latency sensitive controller
**Reallocator** - Slow Acting, Cost sensitive controller
