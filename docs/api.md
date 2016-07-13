## Classes

<dl>
<dt><a href="#Application">Application</a></dt>
<dd></dd>
<dt><a href="#ApplicationResponse">ApplicationResponse</a> : <code>Object</code></dt>
<dd></dd>
<dt><a href="#Call">Call</a></dt>
<dd></dd>
<dt><a href="#CallResponse">CallResponse</a> : <code>Object</code></dt>
<dd></dd>
<dt><a href="#Domain">Domain</a></dt>
<dd></dd>
<dt><a href="#DomainResponse">DomainResponse</a> : <code>Object</code></dt>
<dd></dd>
<dt><a href="#CatapultClient">CatapultClient</a></dt>
<dd></dd>
<dt><a href="#Message">Message</a></dt>
<dd></dd>
<dt><a href="#Recording">Recording</a></dt>
<dd></dd>
</dl>

## Functions

<dl>
<dt><a href="#getNextLink">getNextLink(response)</a> ⇒</dt>
<dd><p>getNextLink</p>
</dd>
</dl>

<a name="Application"></a>

## Application
**Kind**: global class  

* [Application](#Application)
    * [new Application(client)](#new_Application_new)
    * [.list(params, [callback])](#Application+list) ⇒ <code>[Array.&lt;ApplicationResponse&gt;](#ApplicationResponse)</code>
    * [.create(params, [callback])](#Application+create) ⇒ <code>[ApplicationResponse](#ApplicationResponse)</code>
    * [.get(applicationId, [callback])](#Application+get) ⇒ <code>[ApplicationResponse](#ApplicationResponse)</code>
    * [.update(applicationId, params, [callback])](#Application+update)
    * [.delete(applicationId, [callback])](#Application+delete)

<a name="new_Application_new"></a>

### new Application(client)
Application


| Param | Type | Description |
| --- | --- | --- |
| client | <code>Object</code> | Catapult client |

<a name="Application+list"></a>

### application.list(params, [callback]) ⇒ <code>[Array.&lt;ApplicationResponse&gt;](#ApplicationResponse)</code>
List the user's applications

**Kind**: instance method of <code>[Application](#Application)</code>  
**Returns**: <code>[Array.&lt;ApplicationResponse&gt;](#ApplicationResponse)</code> - A promise for the list of applications, has a getNextPage
function if the number of applications returned by the query exceeds the page size.  

| Param | Type | Description |
| --- | --- | --- |
| params | <code>Object</code> | Parameters for filtering applications. |
| [params.size] | <code>Number</code> | The maximum number of applications returned by the query per page (Max size: 1000). |
| [callback] | <code>function</code> | A callback for the list of applications. |

<a name="Application+create"></a>

### application.create(params, [callback]) ⇒ <code>[ApplicationResponse](#ApplicationResponse)</code>
Create a new application

**Kind**: instance method of <code>[Application](#Application)</code>  
**Returns**: <code>[ApplicationResponse](#ApplicationResponse)</code> - A promise for the newly created application.  

| Param | Type | Description |
| --- | --- | --- |
| params | <code>Object</code> | Parameters for creating a new call |
| [params.name] | <code>String</code> | A name you choose for this application. |
| [params.incomingCallUrl] | <code>String</code> | A URL where call events will be sent for an inbound call. This is the endpoint where the Application Platform will send all call events. Either incomingCallUrl or incomingMessageUrl is required. |
| [params.incomingCallUrlCallbackTimeout] | <code>String</code> | Determine how long should the platform wait for incomingCallUrl's response before timing out in milliseconds. |
| [params.incomingCallFallbackUrl] | <code>String</code> | The URL used to send the callback event if the request to incomingCallUrl fails. |
| [params.incomingMessageUrl] | <code>String</code> | A URL where message events will be sent for an inbound message. This is the endpoint where the Application Platform will send all message events. Either incomingMessageUrl or incomingCallUrl is required. |
| [params.incomingMessageUrlCallbackTimeout] | <code>Number</code> | Determine how long should the platform wait for incomingMessageUrl's response before timing out in milliseconds. |
| [params.incomingMessageFallbackUrl] | <code>String</code> | The URL used to send the callback event if the request to incomingMessageUrl fails. |
| [params.callbackHttpMethod] | <code>String</code> | Determine if the callback event should be sent via HTTP GET or HTTP POST. Values are "get" or "post", default: "post". |
| [params.autoAnswer] | <code>Boolean</code> | Determines whether or not an incoming call should be automatically answered. Default value is 'true'. |
| [callback] | <code>function</code> | A callback for the list of applications |

<a name="Application+get"></a>

### application.get(applicationId, [callback]) ⇒ <code>[ApplicationResponse](#ApplicationResponse)</code>
Get an application.

**Kind**: instance method of <code>[Application](#Application)</code>  
**Returns**: <code>[ApplicationResponse](#ApplicationResponse)</code> - A promise for the application.  

| Param | Type | Description |
| --- | --- | --- |
| applicationId | <code>String</code> | The ID of the application to get. |
| [callback] | <code>function</code> | A callback for the application. |

<a name="Application+update"></a>

### application.update(applicationId, params, [callback])
Make changes to an application.

**Kind**: instance method of <code>[Application](#Application)</code>  

| Param | Type | Description |
| --- | --- | --- |
| applicationId | <code>String</code> | The ID of the application to modify. |
| params | <code>Object</code> | Parameters for creating a new call |
| [params.name] | <code>String</code> | A name you choose for this application. |
| [params.incomingCallUrl] | <code>String</code> | A URL where call events will be sent for an inbound call. This is the endpoint where the Application Platform will send all call events. Either incomingCallUrl or incomingMessageUrl is required. |
| [params.incomingCallUrlCallbackTimeout] | <code>String</code> | Determine how long should the platform wait for incomingCallUrl's response before timing out in milliseconds. |
| [params.incomingCallFallbackUrl] | <code>String</code> | The URL used to send the callback event if the request to incomingCallUrl fails. |
| [params.incomingMessageUrl] | <code>String</code> | A URL where message events will be sent for an inbound message. This is the endpoint where the Application Platform will send all message events. Either incomingMessageUrl or incomingCallUrl is required. |
| [params.incomingMessageUrlCallbackTimeout] | <code>Number</code> | Determine how long should the platform wait for incomingMessageUrl's response before timing out in milliseconds. |
| [params.incomingMessageFallbackUrl] | <code>String</code> | The URL used to send the callback event if the request to incomingMessageUrl fails. |
| [params.callbackHttpMethod] | <code>String</code> | Determine if the callback event should be sent via HTTP GET or HTTP POST. Values are "get" or "post", default: "post". |
| [params.autoAnswer] | <code>Boolean</code> | Determines whether or not an incoming call should be automatically answered. Default value is 'true'. |
| [callback] | <code>function</code> | A callback for the list of applications |

<a name="Application+delete"></a>

### application.delete(applicationId, [callback])
Delete an application.

**Kind**: instance method of <code>[Application](#Application)</code>  

| Param | Type | Description |
| --- | --- | --- |
| applicationId | <code>String</code> | The ID of the application to delete. |
| [callback] | <code>function</code> | A callback for the application. |

<a name="ApplicationResponse"></a>

## ApplicationResponse : <code>Object</code>
**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| id | <code>String</code> | The unique identifier for the application. |
| name | <code>String</code> | A name you choose for this application. |
| incomingCallUrl | <code>String</code> | A URL where call events will be sent for an inbound call. This is the endpoint where the Application Platform will send all call events. Either incomingCallUrl or incomingMessageUrl is required. |
| incomingCallUrlCallbackTimeout | <code>String</code> | Determine how long should the platform wait for incomingCallUrl's response before timing out in milliseconds. |
| incomingCallFallbackUrl | <code>String</code> | The URL used to send the callback event if the request to incomingCallUrl fails. |
| callbackHttpMethod | <code>String</code> | Determine if the callback event should be sent via HTTP GET or HTTP POST. Values are "get" or "post", default: "post". |
| autoAnswer | <code>Boolean</code> | Determines whether or not an incoming call should be automatically answered. Default value is 'true'. |
| incomingMessageUrl | <code>String</code> | A URL where message events will be sent for an inbound message. This is the endpoint where the Application Platform will send all message events. Either incomingMessageUrl or incomingCallUrl is required. |
| incomingMessageUrlCallbackTimeout | <code>Number</code> | Determine how long should the platform wait for incomingMessageUrl's response before timing out in milliseconds. |
| incomingMessageFallbackUrl | <code>String</code> | The URL used to send the callback event if the request to incomingMessageUrl fails. |

<a name="Call"></a>

## Call
**Kind**: global class  

* [Call](#Call)
    * [new Call()](#new_Call_new)
    * [.create(params, [callback])](#Call+create) ⇒ <code>[CallResponse](#CallResponse)</code>
    * [.get(callId, callback)](#Call+get) ⇒ <code>Promise</code>
    * [.list(params, callback)](#Call+list) ⇒ <code>Promise</code>

<a name="new_Call_new"></a>

### new Call()
Voice call

<a name="Call+create"></a>

### call.create(params, [callback]) ⇒ <code>[CallResponse](#CallResponse)</code>
Create a new voice call

**Kind**: instance method of <code>[Call](#Call)</code>  
**Returns**: <code>[CallResponse](#CallResponse)</code> - A promise for the newly created call  

| Param | Type | Description |
| --- | --- | --- |
| params | <code>Object</code> | Parameters for creating a new call |
| params.from | <code>String</code> | A Bandwidth phone number on your account the call should come from (must be in E.164 format, like +19195551212). |
| params.to | <code>String</code> | The number to call (must be either an E.164 formated number, like +19195551212, or a valid SIP URI, like sip:someone@somewhere.com). |
| [params.callTimeout] | <code>Number</code> | Determine how long should the platform wait for] call answer before timing out in seconds. |
| [params.callbackUrl] | <code>String</code> | The full server URL where the call events related to the Call will be sent to. |
| [params.callbackTimeout] | <code>Number</code> | Determine how long should the platform wait for callbackUrl's response before timing out in milliseconds. |
| [params.callbackHttpMethod] | <code>String</code> | Determine if the callback event should be sent via HTTP GET or HTTP POST. Values are "GET" or "POST" (if not set the default is POST). |
| [params.fallbackUrl] | <code>String</code> | The full server URL used to send the callback event if the request to callbackUrl fails. |
| [params.bridgeId] | <code>String</code> | The id of the bridge where the call will be added. |
| [params.conferenceId] | <code>String</code> | Id of the conference where the call will be added. This property is required if you want to add this call to a conference. |
| [params.recordingEnabled] | <code>String</code> | Indicates if the call should be recorded after being created. Set to "true" to enable. Default is "false". |
| [params.recordingMaxDuration] | <code>String</code> | Indicates the maximum duration of call recording in seconds. Default value is 1 hour. |
| [params.transcriptionEnabled] | <code>String</code> | Whether all the recordings for this call is going to be automatically transcribed. |
| [params.tag] | <code>String</code> | A string that will be included in the callback events of the call. |
| [params.sipHeaders] | <code>Object</code> | Map of Sip headers prefixed by "X-". Up to 5 headers can be sent per call. |
| [callback] | <code>function</code> | Callback with the newly created call |

<a name="Call+get"></a>

### call.get(callId, callback) ⇒ <code>Promise</code>
Gets information about an active or completed call.

**Kind**: instance method of <code>[Call](#Call)</code>  
**Returns**: <code>Promise</code> - A promise for the call information  

| Param | Type | Description |
| --- | --- | --- |
| callId | <code>String</code> | The ID of the call to get |
| callback | <code>function</code> | A callback with the call information |

<a name="Call+list"></a>

### call.list(params, callback) ⇒ <code>Promise</code>
Gets a list of active and historic calls you made or received.

**Kind**: instance method of <code>[Call](#Call)</code>  
**Returns**: <code>Promise</code> - A promise for the list of calls  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| params | <code>Object</code> |  | Query parameters for listing calls |
| [params.bridgeId] | <code>String</code> |  | The id of the bridge for querying a list of calls history (pagination does not apply). |
| [params.conferenceId] | <code>String</code> |  | The id of the conference for querying a list of calls history |
| [params.from] | <code>String</code> |  | The number to filter calls that came from (must be either an E.164 formated number,like +19195551212, or a valid SIP URI, like sip:someone@somewhere.com). |
| [params.to] | <code>String</code> |  | The number to filter calls that was called to (must be either an E.164 formated number,like +19195551212, or a valid SIP URI, like sip:someone@somewhere.com). |
| [params.page] | <code>Number</code> | <code>0</code> | Used for pagination to indicate the page requested for querying a list of calls. If no value is specified the default is 0. |
| [params.size] | <code>Number</code> | <code>25</code> | Used for pagination to indicate the size of each page requested for querying a list of calls. If no value is specified the default value is 25 (maximum value 1000). |
| callback | <code>function</code> |  | A callback with the list of calls |

<a name="CallResponse"></a>

## CallResponse : <code>Object</code>
**Kind**: global class  
**Properties**

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| id | <code>String</code> |  | The unique ID of the call. |
| direction | <code>String</code> |  | Call direction: values are 'in' for an incoming call, 'out' for an outgoing call |
| from | <code>String</code> |  | The phone number or SIP address that made the call. Phone numbers are in E.164 format (e.g. +15555555555) -or- SIP addresses (e.g. identify@domain.com). |
| to | <code>String</code> |  | The phone number or SIP address that received the call. Phone numbers are in E.164 format (e.g. +15555555555) -or- SIP addresses (e.g. identify@domain.com). |
| state | <code>String</code> |  | The call state. Described below, values are 'started' 'rejected' 'active' 'completed' 'transferring' |
| startTime | <code>String</code> |  | Date when the call was created. Timestamp follows the ISO8601 format. |
| activeTime | <code>String</code> |  | Date when the call was answered. Timestamp follows the ISO8601 format. |
| endTime | <code>String</code> |  | Date when the call ended. Timestamp follows the ISO8601 format. |
| callTimeout | <code>Number</code> |  | Determine how long should the platform wait for call answer before timing out in seconds |
| callbackUrl | <code>String</code> |  | The server URL where the call events related to the call will be sent. |
| callbackHttpMethod | <code>String</code> |  | Determine if the callback event should be sent via HTTP GET or HTTP POST. Values are 'get' or 'post' Default is 'post' |
| callbackTimeout | <code>Number</code> |  | Determine how long should the platform wait for callbackUrl's response before timing out (milliseconds). |
| fallbackUrl | <code>String</code> |  | The server URL used to send the call events if the request to callbackUrl fails. |
| chargeableDuration | <code>Number</code> |  | The number of seconds the call will be billed for. |
| transferTo | <code>String</code> |  | Phone number or SIP address that the call is going to be transferred to. |
| transferCallerId | <code>String</code> |  | This is the caller id that will be used when the call is transferred. This parameter is only considered in transfer state. |
| whisperAudio | <code>String</code> |  | Audio to be played to the caller that the call will be transferred to. |
| bridgeId | <code>String</code> |  | The id of the bridge where the call will be added. |
| bridge | <code>String</code> |  | The URL of the bridge, if any, that contains the call. |
| conferenceId | <code>String</code> |  | The id of the conference where the call will be added. This property is required if you want to add this call to a conference. |
| conference | <code>String</code> |  | The complete URL of the conference resource the call is associated with. |
| events | <code>String</code> |  | The URL to retrieve the events related to the call. |
| recordingEnabled | <code>String</code> | <code>false</code> | Indicates if the call should be recorded after being created. Set to 'true' to enable. Default is 'false' |
| recordingFileFormat | <code>String</code> | <code>wav</code> | The file format of the recorded call. Supported values are 'wav' (default) and 'mp3'. |
| recordingMaxDuration | <code>Number</code> | <code>3600</code> | Indicates the maximum duration of call recording in seconds. Default value is 1 hour. |
| transcriptionEnabled | <code>Boolean</code> |  | Whether all the recordings for this call should be be automatically transcribed. tag Any string, it will be included in the callback events of the call. |
| page | <code>Number</code> | <code>0</code> | Used for pagination to indicate the page requested for querying a list of calls. If no value is specified the default is 0. |
| size | <code>Number</code> | <code>25</code> | Used for pagination to indicate the size of each page requested for querying a list of calls. If no value is specified the default value is 25 (maximum value 1000). |
| sipHeaders | <code>Object</code> |  | Map of Sip headers prefixed by "X-". Up to 5 headers can be sent per call. Max length for header and value is 256 characters. |

<a name="Domain"></a>

## Domain
**Kind**: global class  

* [Domain](#Domain)
    * [new Domain()](#new_Domain_new)
    * [.create(params, [callback])](#Domain+create) ⇒ <code>[DomainResponse](#DomainResponse)</code>
    * [.list(callback)](#Domain+list) ⇒ <code>[Array.&lt;DomainResponse&gt;](#DomainResponse)</code>
    * [.delete(domainId, [callback])](#Domain+delete) ⇒ <code>Promise</code>

<a name="new_Domain_new"></a>

### new Domain()
Domain

<a name="Domain+create"></a>

### domain.create(params, [callback]) ⇒ <code>[DomainResponse](#DomainResponse)</code>
Create a domain

**Kind**: instance method of <code>[Domain](#Domain)</code>  
**Returns**: <code>[DomainResponse](#DomainResponse)</code> - A promise for the newly created domain  

| Param | Type | Description |
| --- | --- | --- |
| params | <code>Object</code> | Parameters for creating a new domain |
| params.name | <code>String</code> | The name is a unique URI to be used in DNS lookups. |
| params.description | <code>String</code> | String to describe the domain. |
| [callback] | <code>function</code> | Callback with the newly created domain |

<a name="Domain+list"></a>

### domain.list(callback) ⇒ <code>[Array.&lt;DomainResponse&gt;](#DomainResponse)</code>
Gets a list of all domains.

**Kind**: instance method of <code>[Domain](#Domain)</code>  
**Returns**: <code>[Array.&lt;DomainResponse&gt;](#DomainResponse)</code> - A promise for the list of domains.  

| Param | Type | Description |
| --- | --- | --- |
| callback | <code>function</code> | A callback with the list of calls |
| [params.size] | <code>Number</code> | the maximum number of domains returned by the query per page (Max size: 100). |

<a name="Domain+delete"></a>

### domain.delete(domainId, [callback]) ⇒ <code>Promise</code>
Delete a domain.

**Kind**: instance method of <code>[Domain](#Domain)</code>  
**Returns**: <code>Promise</code> - A promise for current operation.  

| Param | Type | Description |
| --- | --- | --- |
| domainId | <code>String</code> | ID of the domain to delete. |
| [callback] | <code>function</code> | A callback for the domain. |

<a name="DomainResponse"></a>

## DomainResponse : <code>Object</code>
**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| id | <code>String</code> | The unique identifier for the domain. |
| name | <code>String</code> | A name you choose for this domain. |
| description | <code>String</code> | A description of this domain. |

<a name="CatapultClient"></a>

## CatapultClient
**Kind**: global class  
<a name="new_CatapultClient_new"></a>

### new CatapultClient(config)
Catapult API Client


| Param | Type | Default | Description |
| --- | --- | --- | --- |
| config | <code>Object</code> |  | Client configuration parameters |
| config.userId | <code>String</code> |  | Your Catapult user ID |
| config.apiToken | <code>String</code> |  | Your Catapult API token |
| config.apiSecret | <code>String</code> |  | Your Catapult API secret |
| [config.baseUrl] | <code>String</code> | <code>https://api.catapult.inetwork.com</code> | The catapult base URL. Configurable for using alternative Catapult environments. |

<a name="Message"></a>

## Message
**Kind**: global class  

* [Message](#Message)
    * [new Message(client)](#new_Message_new)
    * [.send(params, The, The, [callback])](#Message+send) ⇒ <code>MessageResponse</code>
    * [.get(messageId, [callback])](#Message+get) ⇒ <code>MessageResponse</code>
    * [.list(params, [callback])](#Message+list) ⇒ <code>Array</code>

<a name="new_Message_new"></a>

### new Message(client)
SMS or MMS Message


| Param | Type | Description |
| --- | --- | --- |
| client | <code>Object</code> | Catapult client |

<a name="Message+send"></a>

### message.send(params, The, The, [callback]) ⇒ <code>MessageResponse</code>
Send a new SMS or MMS message

**Kind**: instance method of <code>[Message](#Message)</code>  
**Returns**: <code>MessageResponse</code> - A promise for the new message object  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| params | <code>Object</code> |  | Parameters for sending a new message |
| The | <code>params.text</code> |  | message text to send |
| The | <code>params.from</code> |  | message sender"s telephone number (or short code) This must be a Catapult number that you own |
| [params.to] | <code>String</code> |  | Message recipient telephone number (or short code) |
| [params.media] | <code>Array</code> |  | Json array containing list of media urls to be sent as content for an mms. Valid URLs are: https://api.catapult.inetwork.com/v1/users/<user-id>/media/ We also support media URLs that are external to Bandwidth API, http:// or https:// format: Example: http://customer-web-site.com/file.jpg |
| [params.callbackUrl] | <code>String</code> |  | The complete URL where the events related to the outgoing message will be sent |
| [params.callbackTimeout] | <code>Number</code> |  | Determine how long should the platform wait for callbackUrl"s response before timing out (milliseconds) |
| [params.fallbackUrl] | <code>String</code> |  | The server URL used to send message events if the request to callbackUrl fails |
| [params.tag] | <code>String</code> |  | A string that will be included in the callback events of the message |
| [params.receiptRequested] | <code>String</code> | <code>none</code> | Requested receipt option for outbound messages: `none` `all` `error` |
| [callback] | <code>function</code> |  | A callback for the new message object |

<a name="Message+get"></a>

### message.get(messageId, [callback]) ⇒ <code>MessageResponse</code>
Get a message

**Kind**: instance method of <code>[Message](#Message)</code>  
**Returns**: <code>MessageResponse</code> - A promise for the message  

| Param | Type | Description |
| --- | --- | --- |
| messageId | <code>String</code> | The ID of the message to get |
| [callback] | <code>function</code> | A callback for the message |

<a name="Message+list"></a>

### message.list(params, [callback]) ⇒ <code>Array</code>
Gets a list of messages

**Kind**: instance method of <code>[Message](#Message)</code>  
**Returns**: <code>Array</code> - A promise for the list of messages  

| Param | Type | Description |
| --- | --- | --- |
| params | <code>Object</code> | Search parameters |
| [callback] | <code>function</code> | A callback for the list of messages |

<a name="Recording"></a>

## Recording
**Kind**: global class  

* [Recording](#Recording)
    * [new Recording()](#new_Recording_new)
    * [.get(recordingId, [callback])](#Recording+get) ⇒ <code>RecordingResponse</code>
    * [.list(params, [callback])](#Recording+list) ⇒ <code>RecordingResponse</code>

<a name="new_Recording_new"></a>

### new Recording()
Retrieve information about call recordings

<a name="Recording+get"></a>

### recording.get(recordingId, [callback]) ⇒ <code>RecordingResponse</code>
Get a recording

**Kind**: instance method of <code>[Recording](#Recording)</code>  
**Returns**: <code>RecordingResponse</code> - A promise for the recording object  

| Param | Type | Description |
| --- | --- | --- |
| recordingId | <code>String</code> | The ID of the recording to retrieve |
| [callback] | <code>function</code> | Callback with the recording object |

<a name="Recording+list"></a>

### recording.list(params, [callback]) ⇒ <code>RecordingResponse</code>
Get a list of recordings

**Kind**: instance method of <code>[Recording](#Recording)</code>  
**Returns**: <code>RecordingResponse</code> - A promise for the recording objects  

| Param | Type | Description |
| --- | --- | --- |
| params | <code>Object</code> | [description] |
| [callback] | <code>function</code> | Callback with the recording objects |

<a name="getNextLink"></a>

## getNextLink(response) ⇒
getNextLink

**Kind**: global function  
**Returns**: A parsed version of the link to the subsequent page, or null if no such page exists.  

| Param | Type | Description |
| --- | --- | --- |
| response | <code>Object</code> | A response object returned from calling 'client.makeRequest' |
