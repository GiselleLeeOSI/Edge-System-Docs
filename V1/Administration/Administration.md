---
uid: edgeSystemAdministration
---

# Edge Data Store administration

The Edge Data Store provides a number of administration level functions.

## Reset Edge Data Store

Edge Data Store provides a method of performing a complete reset of the product. When you perform a reset, all event data and Edge Data Store configuration is deleted, and the product is restarted.

**Note:** All configuration and stored data will be lost as a result of performing this action.

To reset the Edge Data Store, use any REST client and make a request using one of the following:

```http
Method: POST
Endpoint: http://localhost:5590/api/v1/administration/System/Reset
Header: Content-Type application/json
```

Example using curl:

```bash
curl -v -d "" -X POST http://localhost:5590/api/v1/Administration/System/Reset
```

An HTTP status 204 message indicates success.

## Reset the Edge Storage Component

Edge Data Store provides a method by which a user may delete and reset all event and configuration data related to the Edge Data Store component, after which the product will be restarted.

To reset the Storage component, use any REST client and make a request using one of the following:

```http
Method: POST
Endpoint: http://localhost:5590/api/v1/administration/Storage/Reset
Header: Content-Type application/json
```

Example using cURL:

```bash
curl -v -d "" -X POST http://localhost:5590/api/v1/Administration/Storage/Reset
```

An HTTP status 204 message indicates success.

## Stop and Start an EDS Connectivity component

Edge Data Store provides the ability to stop and start EDS Connectivity components. When Edge Data Store starts, all currently configured connectivity components are started By default, and remain running until the product shuts down.

### Stop an EDS Connectivity component

To stop an individual EDS Connectivity component, use any REST client and make a request using one of the following:

```http
Method: POST
Endpoint: http://localhost:5590/api/v1/administration/ConnectivityId/Stop
Header: Content-Type application/json
```

Example using curl:

```bash
curl -v -d "" -X POST http://localhost:5590/api/v1/Administration/ConnectivityId/Stop
```

**Note:** Replace **ConnectivityId** with the id of the EDS Connectivity component you want to stop.

An HTTP status 204 message indicates success.

### Start an EDS Connectivity component

To start an individual EDS Connectivity component, use any REST client and make a request using the following:

```http
Method: POST
Endpoint: http://localhost:5590/api/v1/administration/ConnectivityId/Start
Header: Content-Type application/json
```

Example using curl:

```bash
curl -v -d "" -X POST http://localhost:5590/api/v1/Administration/ConnectivityId/Start
```

**Note:** Replace **ConnectivityId** with the id of the EDS Connectivity component you want to start.

An HTTP status 204 message indicates success.
