# ![LOGO](logo.png) Service Networking **flow**ground Connector

## Description

A generated **flow**ground connector for the Service Networking API (version v1beta).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/servicenetworking/v1beta/swagger.json<br/>
Generated at: 2019-05-23T12:13:39+03:00

## API Description

Provides automatic management of network configurations necessary for certain services.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Gets the latest state of a long-running operation.  Clients can use this<br/>
> method to poll the operation result at intervals as recommended by the API<br/>
> service.

*Tags:* `operations`

#### Input Parameters
* `name` - _required_ - The name of the operation resource.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Updates the allocated ranges that are assigned to a connection.<br/>
> The response from the `get` operation will be of type `Connection` if the<br/>
> operation successfully completes.

*Tags:* `services`

#### Input Parameters
* `force` - _optional_ - If a previously defined allocated range is removed, force flag must be
set to true.
* `name` - _required_ - The service producer peering service that is managing peering connectivity
for a service producer organization.
For Google services that support this functionality, this is
`services/servicenetworking.googleapis.com`.
* `updateMask` - _optional_ - The update mask. If this is omitted, it defaults to "*". You can only
update the listed peering ranges.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### List the private connections that are configured in a service consumer's<br/>
> VPC network.

*Tags:* `services`

#### Input Parameters
* `network` - _optional_ - The name of service consumer's VPC network that's connected with service
producer network through a private connection. The network name must be in
the following format:
`projects/{project}/global/networks/{network}`. {project} is a
project number, such as in `12345` that includes the VPC service
consumer's VPC network. {network} is the name of the service consumer's VPC
network.
* `parent` - _required_ - The service that is managing peering connectivity for a service producer's
organization. For Google services that support this functionality, this
value is `services/servicenetworking.googleapis.com`.
If you specify `-` as the parameter value, all configured public peering
services are listed.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a private connection that establishes a VPC Network Peering<br/>
> connection to a VPC network in the service producer's organization.<br/>
> The administrator of the service consumer's VPC network invokes this<br/>
> method. The administrator must assign one or more allocated IP ranges for<br/>
> provisioning subnetworks in the service producer's VPC network. This<br/>
> connection is used for all supported services in the service producer's<br/>
> organization, so it only needs to be invoked once. The response from the<br/>
> `get` operation will be of type `Connection` if the operation successfully<br/>
> completes.

*Tags:* `services`

#### Input Parameters
* `parent` - _required_ - The service that is managing peering connectivity for a service producer's
organization. For Google services that support this functionality, this
value is `services/servicenetworking.googleapis.com`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### For service producers, provisions a new subnet in a<br/>
> peered service's shared VPC network in the requested region and with the<br/>
> requested size that's expressed as a CIDR range (number of leading bits of<br/>
> ipV4 network mask). The method checks against the assigned allocated ranges<br/>
> to find a non-conflicting IP address range. The method will reuse a subnet<br/>
> if subsequent calls contain the same subnet name, region, and prefix<br/>
> length. This method will make producer's tenant project to be a shared VPC<br/>
> service project as needed. The response from the `get` operation will be of<br/>
> type `Subnetwork` if the operation successfully completes.

*Tags:* `services`

#### Input Parameters
* `parent` - _required_ - Required. A tenant project in the service producer organization, in the
following format: services/{service}/{collection-id}/{resource-id}.
{collection-id} is the cloud resource collection type that represents the
tenant project. Only `projects` are supported.
{resource-id} is the tenant project numeric id, such as
`123456`. {service} the name of the peering service, such as
`service-peering.example.com`. This service must already be
enabled in the service consumer's project.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Service producers can use this method to find a currently unused range<br/>
> within consumer allocated ranges.   This returned range is not reserved,<br/>
> and not guaranteed to remain unused.<br/>
> It will validate previously provided allocated ranges, find<br/>
> non-conflicting sub-range of requested size (expressed in<br/>
> number of leading bits of ipv4 network mask, as in CIDR range<br/>
> notation).<br/>
> Operation<response: Range>

*Tags:* `services`

#### Input Parameters
* `parent` - _required_ - Required. This is in a form services/{service}.
{service} the name of the private access management service, for example
'service-peering.example.com'.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-servicenetworking-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
