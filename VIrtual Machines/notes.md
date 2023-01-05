# Virtual Machines Notes

## Create Virtual Machine
1. Use the Azure Portal
2. Create a resource -> Compute Tab
3. Click Virtual Machine
4. Configure the machine
    1. Geo location
    2. Availability options (1 machine not expected to have 100% uptime need redundancy)
        1. Availability set: basic, VMs are related and distributed across fault domains (far enough apart to maintain redundancy). If a regional outage, they would go down.
        2. Availability zone: corresponds to a region and the datacenters in that region
        3. Virtual Machine scale set: vms scale up and down for high demand
    3. Select an image
    4. Spot instance is a discounted rate based on availability (low priority tasks like batch jobs)
    5. Select your size (CPUs, memory etc.)
        1. Different lettered series for sizes and types
        2. B series is burstable (varying performance), good for development and testing. B2ms good for general purpose
        3. D series is more for production uses
    6. Select authentication type (SSH or username/password)
    7. Select inboud ports
5. Disks
    1. Choose your SSD/HD
    2. Key management and encryption
6. Networking
    1. Creat a new virtual network for your vm
    2. Defaults work for most use cases
    3. Choose to add load balancing or not
7. Management
    1. Identity is for assigning permissions to act on other Azure resources
    2. Auto shut down is good for development and testing
8. Advanced
    1. Host: can select a dedicated physical machine that is not shared with other VMs
    2. Capacity reservations: reserve capacity (compute resources) ahead of time, charged for full reservation immediately
    3. Proximity placement group: set up machines in close proximity for latency performance
9. Tags
    1. Meta data (key value pairs) for the resource (i.e "CreatedBy": "Your Name", "environment")


## Connect to VM

1. Go to connect tab in portal
3. Follow steps to connect via ssh or rdp to the vm

## While its Running

1. Size tab in Azure portal allows you to scale the vm up or down, requires restart
2. You can set up Azure DevOps for CI/CD
3. You can enable automatic backups
