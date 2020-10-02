# PiHole with Unbound TLS Support

2 environment variables are required before standing up the docker stack

	export IP_ADDRESS=$(ip a s eth0 | awk '/inet / {print$2}')
	read -s -p "Enter a password for the pihole UI: " PIHOLE_PASSWORD

Once those variables are set, you can launch the stack.

	docker-compose up -d

