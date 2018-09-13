#  Docker compose file to create Nexus and Jenkins behind a Nginx reverse proxy. Also added redis cache

To create and run the Nexus and Jenkins behind a Nginx reverse proxy with an Instance of Redis cache

```
./build.sh
```

Subsequent runs can use docker-compose:

```
docker-compose up -d
```

To stop, use docker-compose:

```
docker-compose down
```

## SSL Certificates

The Ngnix docker image build process generates insecure SSL certificates with fake location information and CNAME of localhost. Understand the risks of using these SSL certificates before proceeding. A deployed solution should use a valid CA certificate.
