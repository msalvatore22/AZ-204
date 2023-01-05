# Commands

## Connect to vm

1. Open WSL on Windows, Terminal on Mac, Shell on Linux
2. chmod 400 <keyname>.pem
3. private key path: ~/.ssh/<keyname>.pem
4. ssh -i ~/.ssh/<keyname>.pem azureuser@<ip address>