0、docker build -t elvizlai/openvon .

1、CID=$(docker run -d --privileged -p 1194:1194/udp -p 443:443/tcp --name openvpn elvizlai/openvon)

2、docker run -t -i -p 12315:12315 --volumes-from $CID elvizlai/openvon serveconfig