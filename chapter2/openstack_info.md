# What is OpenStack?

OpenStack is an [free and opensource](https://en.wikipedia.org/wiki/Free_and_open-source_software) cloud operating system, mostly deployed as Infrastructure-As-Service(IaaS) which controls large pools of compute, storage, and networking resources throughout a data center.
Here [Infrastructure-As-Service](https://en.wikipedia.org/wiki/Infrastructure_as_a_service) means that OpenStack serves the user with quickly adding new instance upon which the other cloud components can run.

##  Components of OpenStack

OpenStack has a modular architecture with various code names for its components:

  1. Nova (Compute)
  2. Swift (Object Storage)
  3. Cinder (Block Storage)
  4. Glance (Image Service)
  5. Neutron (Networking)
  6. Horizon (Dashboard )
  7. Ceilometer (Telemetry)
  8. Heat (Orchestration)

### Keystone (Identity Service)

 It’s the main authentication and authorization service as I heard from someone, it’s the a who are you and what do you want service. It authorizes
1. Users
2. Services
3. Endpoints

Keystone uses tokens for authorization and maintains Session state.

### Nova (Compute)

Nova compute provides a platform on which we are going to run our guest machines. It’s the virtual machine provisioning and management module that defines drivers that interact with underlying virtualization.

### Glance (Image Service)

In simple words glance is the Image Registry, it stores and Manage our guest (VM) images, Disk Images, snap shots etc. Instances are booted from the glance image registry.  A feature of Glance is to store images remotely so to save local disk space.

### Swift (Object Storage)

Swift offers cloud storage software, as they are not attached to servers, they are individual addressable objects. It’s built for scale and optimized for durability, availability, and concurrency across the entire data set.

### Cinder (Block Storage)

Cinder is also one of the storage modules of Openstack; It has the performance characteristics of a Hard drive but much slower then Swift and has low latency. Block Volume are created in swift and attached to running Volumes for which you want to attach an extra partition or for copying data to it. It survives the termination of an Instance. It is used to keep persistence storage. Cinder Images are mostly stored on our shared storage environment for readily availability. These Images can be clones and snapshot which can be turned in to bootable images. Its similar to Amazon Elastic block Storage.

### Neutron (Networking)

Neutron, the networking component which was formally called Quantum. This component provides the software defined Networking Stack for Openstack. It Provides networking as a service. It gives the cloud tenants an API to build rich networking topologies, and configure advanced network policies in the cloud. It enables innovation plugins (open and closed source) that introduce advanced network capabilities which let anyone build advanced network services (open and closed source) that plug into Openstack tenant networks means that you can create advance managed switches and routers. You can even create an intelligent switch from a PC (Yes you can use it as a standalone component) and use it to replace your managed switch or atleast make it act as a backup Switch.

### Heat (Orchestration)

It creates a human and machine-accessible service for managing the entire lifecycle of infrastructure and applications within Openstack clouds. It contains human readable templates with simple instruction that is read by the Heat Engine. Heat along with ceilometer (explained below) can create an auto-scaling the cloud.

### Telemetry (Ceilometer)

This module is responsible for metering Information. It can be used generate bills and based on the statistics of usage. Its API can be used with external billing systems. Administrators can create certain alarms that are triggered based on performance statistics

### Horizon (Dashboard )

Horizon is the Dashboard to Openstack, your eyes and ears. It provides a web based user interface to OpenStack services including Nova, Swift, Keystone etc

# OpenStack Releases


| Release Date  | Release Name  |                             Components used|
|: -------------:|:-------------:|:------------------------------------------:|
|21 October 2010| Austin        |               Nova, Swift                  |
|3 February 2011| Bexar	        |            Nova, Glance, Swift             |
|15 April 2011  | Cactus        |            Nova, Glance, Swift             |
|22 September 2011| Diablo      |	                        Nova, Glance, Swift|
|5 April 2012   | Essex	        |	     Nova, Glance, Swift, Horizon, Keystone|
|27 September 2012|	Folsom      | Nova, Glance, Swift, Horizon, Keystone, Quantum, Cinder |
|4 April 2013   |Grizzly		    | Nova, Glance, Swift, Horizon, Keystone, Quantum, Cinder |
|17 October 2013|Havana	        |	Nova, Glance, Swift, Horizon, Keystone, Neutron, Cinder, Heat, Ceilometer|
|17 April 2014  | Icehouse		  | Nova, Glance, Swift, Horizon, Keystone, Neutron, Cinder, Heat, Ceilometer, Trove|
|16 October 2014 | Juno		      | Nova, Glance, Swift, Horizon, Keystone, Neutron, Cinder, Heat, Ceilometer, Trove, Sahara|
|30 April 2015   | Kilo	        |	Nova, Glance, Swift, Horizon, Keystone, Neutron, Cinder, Heat, Ceilometer, Trove, Sahara, Ironic|
|16 October 2015 | Liberty	    |	Nova, Glance, Swift, Horizon, Keystone, Neutron, Cinder, Heat, Ceilometer, Trove, Sahara, Ironic, Zaqar, Manila, Designate, Barbican, Searchlight |
|7 April 2016   |  Mitaka		    |Nova, Glance, Swift, Horizon, Keystone, Neutron, Cinder, Heat, Ceilometer, Trove, Sahara, Ironic, Zaqar, Manila, Designate, Barbican, Searchlight, Magnum|
|6 October 2016 | Newton		    | Nova, Glance, Swift, Horizon, Keystone, Neutron, Cinder, Heat, Ceilometer, Trove, Sahara, Ironic, Zaqar, Manila, Designate, Barbican, Searchlight, Magnum, aodh, cloudkitty, congress, freezer, mistral, monasca-api, monasca-log-api, murano, panko, senlin, solum, tacker, vitrage, Watcher |
|22 February 2017| Ocata	    	| Nova, Glance, Swift, Horizon, Keystone, Neutron, Cinder, Heat, Ceilometer, Trove, Sahara, Ironic, Zaqar, Manila, Designate, Barbican, Searchlight, Magnum, aodh, cloudkitty, congress, freezer, mistral, monasca-api, monasca-log-api, murano, panko, senlin, solum, tacker, vitrage, Watcher|
|30 August 2017 |Pike	          |	Nova, Glance, Swift, Horizon, Keystone, Neutron, Cinder, Heat, Ceilometer, Trove, Sahara, Ironic, Zaqar, Manila, Designate, Barbican, Searchlight, Magnum, aodh, cloudkitty, congress, freezer, mistral, monasca-api, monasca-log-api, murano, panko, senlin, solum, tacker, vitrage, Watcher |
