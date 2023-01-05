# Commands

## Connect to existing VM

1. Open WSL on Windows, Terminal on Mac, Shell on Linux
2. `chmod 400 <keyname>.pem`
3. private key path: `~/.ssh/<keyname>.pem`
4. `ssh -i ~/.ssh/<keyname>.pem azureuser@<ip address>`

## Azure Cloud Shell

1. Create Resource Group
    `New-AzResourceGroup -Name pwrsgroup -Location 'EastUS'`
2. Create VM
    `New-AzVM -ResourceGroupName 'pwrsgroup' -Location 'EastUS' -Name 'pwrsdemo' -PublicIpAddressName 'myPublicIP' -OpenPort 80,443,338`

## Powershell Local Desktop

1. Connect/Authenticate with Azure portal
    `Connect-AzAccount`
2. Get Vms running on your account
    `Get-AzVm`
3. Follow same steps as above
4. Stop the vm
    `Stop-AzVm -Name "<vm name>" -ResourceGroupName "<resource group name>`

## Azure CLI

1. Create resource group
    `az group create --name cligroup --location eastus`
2. Create VM
    `az vm create --resource-group cligroup --name aznewvm2 --image win2016datacenter --admin-username aztestuser`
