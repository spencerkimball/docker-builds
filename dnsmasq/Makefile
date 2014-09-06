all:
	echo "Can do 'clean', 'image' or 'container'"
clean:
	docker stop dnsmasq
	docker rm dnsmasq

image:	
	docker build -rm -t='spencerkimball/dnsmasq' .

container:
	docker run \
	-v="$$(pwd)/dnsmasq.hosts:/dnsmasq.hosts" \
	-name=dnsmasq \
	-d spencerkimball/dnsmasq
	docker ps 
	docker logs $$(sudo docker ps -l -q)
