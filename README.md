# Install and use AWS-based Wireguard
Scripts automate the installation and use of Wireguard on AWS with Ubuntu Server 18.04

## How use

### Installation
```
sudo su
git clone https://github.com/fhanjacson/wireguard-aws.git wireguard_aws
cd wireguard_aws
./initial.sh
```

The `initial.sh` script removes the previous Wireguard installation (if any) using the `remove.sh` script. It then installs and configures the Wireguard service using the `install.sh` script. And then creates a client using the `add-client.sh` script.

### Add new customer
`add-client.sh` - Script to add a new VPN client. As a result of the execution, it creates a configuration file ($CLIENT_NAME.conf) on the path ./clients/$CLIENT_NAME/, displays a QR code with the configuration.

```
./add-client.sh
#OR
./add-client.sh $CLIENT_NAME
```

### Reset customers
`reset.sh` - script that removes information about clients. And stopping the VPN server Winguard
```
./reset.sh
```

### Delete Wireguard
```
./remove.sh
```
## Contributors  (alphabetically)
- [Alexey Chernyavskiy](https://github.com/alexey-chernyavskiy)
- [Max Kovgan](https://github.com/mvk)
