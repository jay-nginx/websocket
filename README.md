# websocket
Proxy and Load Balancing for WebSocket Based Applications

# Test Websocket Application
docker pull giriraj789/ws:v1
docker run -d -p 8010:8010 --name=ws giriraj789/ws:v1

      Hint: You can run multiple versions of the same container on different ports to see traffic being load balanced
      

We used wscat to do the testing

Dynamic header based routing, if header name is custom and value is jaydesai 
request gets routed to upstream jaydesai
else request gets routed to upstream default
Test using -  wscat while true; do wscat -c ws://127.0.0.1:8090 -x test -H custom:jaydesai; sleep 2; done
while true; do wscat -c ws://127.0.0.1:8090 -x test; sleep 2; done
