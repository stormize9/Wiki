
#### Github link
[Docker - OpenVPN](https://hub.docker.com/r/kylemanna/openvpn/)


#### Installation

1. Pick a name for the `$OVPN_DATA` data volume container. It's recommended to use the `ovpn-data-` prefix to operate seamlessly with the reference systemd service. Users are encourage to replace `example` with a descriptive name of their choosing.

	```
	OVPN_DATA="ovpn-data-example"
	```

2. Initialize the `$OVPN_DATA` container that will hold the configuration files and certificates. The container will prompt for a passphrase to protect the private key used by the newly generated certificate authority. Remplace ``VPN.SERVERNAME.COM`` by an IP address or a server name.

	```
	docker volume create --name $OVPN_DATA
	docker run -v $OVPN_DATA:/etc/openvpn --rm kylemanna/openvpn ovpn_genconfig -u udp://VPN.SERVERNAME.COM
	docker run -v $OVPN_DATA:/etc/openvpn --rm -it kylemanna/openvpn ovpn_initpki
	```

 3. Start OpenVPN server process

    ```
    docker run -v $OVPN_DATA:/etc/openvpn -d -p 1194:1194/udp --cap-add=NET_ADMIN kylemanna/openvpn
    ```

4. Generate a client certificate without a passphrase. Remplace ``CLIENTNAME`` by the name of the user.

    ```
    docker run -v $OVPN_DATA:/etc/openvpn --rm -it kylemanna/openvpn easyrsa build-client-full CLIENTNAME nopass
    ```

5. Retrieve the client configuration with embedded certificates. Remplace ``CLIENTNAME`` by the name of the user.

    ```
    docker run -v $OVPN_DATA:/etc/openvpn --rm kylemanna/openvpn ovpn_getclient CLIENTNAME > CLIENTNAME
    ```

6. Copy you opvn configuration file to your client host. For Windows you can use the SCP command described here [Powershell - SCP](/Programmation/Command%20Line/Powershell)