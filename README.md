# PiHole with Unbound TLS Support

2 environment variables are required before standing up the docker stack

	export HOST_IP_ADDRESS=$(ip a s eth0 | awk '/inet / {print$2}')
	export PIHOLE_PASSWORD= ENTER SOME PASSWORD HERE PLEASE K THX

Once those variables are set, you can build the containers.

	docker-compose build

And finally launch the stack.

	docker-compose up -d

