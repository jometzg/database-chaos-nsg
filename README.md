# Database Chaos Experiments

## Chaos Engineering
Chaos engineering is a discipline where experiments are run to deliberately disrupt a service in order to see how that service survives a disruption.

Azure Chaos Studio is an Azure service that allows chaos experiments to be run in a controlled and repeatable manner. These experiments have "fault actions" that can disrupt a specific service - some of these are at control-plane level and some of these are VM-based which use an agent on the VM.

## Chaos Studio Limitations
There are, however, a number of Azure services that that do not directly have a fault and are not built on accessible virtual machines and so cannot use the agent approach. 

This situation will improve over time, but as it currently stands in mid-2023, there are a number of services that do not directly have a chaos fault.

## The use of Network Security Groups (NSG)
This repo describes the use of network faults (more specifically NSG faults) as a means of creating an experiment that can block access to a resource - as a proxy for that service having a fault. In this manner, you can build an experiment that simulates the failure of a service by blocking access to that service via a network security group (NSG).

chaos experiments on a database via the use of a network security group
