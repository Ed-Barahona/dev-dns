# DEV-DNS
Basic NodeJS DNS Proxy used in local development


## Usage

Clone the repo

Set up local domains (records.json)

$ npm install
 
$ npm start 
/
$ sudo node index.js 

Add local DEV-DNS to DNS conf
$ echo nameserver 127.0.0.1 | sudo tee /etc/resolv.conf

Test:
$ host test.narvar.dev // Should return 127.0.0.99
 


### DNS Stuff

Port 53 is a priviliged port, to capture DNS requests the app must run as root (sudo).

The A record maps a name to one or more IP addresses. 

The CNAME record maps a name to another name. It should only be used when there are no other records on that name. 

The ALIAS record maps a name to another name, but in turns it can coexist with other records on that name.
