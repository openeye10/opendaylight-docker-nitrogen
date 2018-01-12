# opendaylight-docker-nitrogen
Containerized OpenDaylight SDN Controller - Nitrogen Release

[OpenDaylight Home](https://www.opendaylight.org/)

[OpenDaylight Nitrogen Documentation](http://docs.opendaylight.org/en/stable-nitrogen/index.html)

## Supported Tags
- latest

## What's Inside?
- Based on alpine:latest
- Exposed Ports: 8101 (Karaf CLI) and 8181 (Web UI / REST API)
- Installed ODL Features: 
    DLUX Web UI (odl-dluxapps-applications),
    NETCONF-over-SSH (odl-netconf-connector-ssh),
    RESTCONF API (odl-restconf)
    
## How To Use It?

### Run Container
`docker run -d -p 8181:8181 -p 8101:8101 --name=opendaylight techmocha/opendaylight-docker-nitrogen`

### Access OpenDaylight Karaf CLI
`ssh -p 8101 karaf@localhost` (If accessing Karaf CLI directly from local machine)

`ssh -p 8101 karaf@<SERVER_IP>` (If accessing Karaf CLI from remote machine)

(NOTE: Default username/password for ODL Karaf CLI is "karaf"/"karaf")

### Access OpenDaylight DLUX Web UI
`http://<SERVER_IP>:8181/index.html`
