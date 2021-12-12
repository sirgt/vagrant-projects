# centos-globalprotect-vpn
This repository intends to create a virtual machine that can connect to GlobalProtect VPN without having to disconnect from Big-IP VPN.

## Clone repository
`git clone ssh://git@git.xoom.com:7999/prodops/centos-globalprotect.git; cd centos-globalprotect`

## Copy ansible configuration and Modify ansible config file with current username on lines 38 and 40
`cp ./config/update-configs-example.yaml ./config/update-configs.yaml`

## Start VM
`vagrant up`

## GlobalProtect most used commands
### Connect to VPN
`globalprotect connect -p panvpn.xoom.com -u USERNAME`
### Show connection status
`globalprotect show --status`
### Disconnect from VPN
`globalprotect disconnect`
### Restart service in case connection is not possible
`sudo systemctl restart gpd`
