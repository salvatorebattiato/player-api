# Control service: Start user-app streaming service daemon
    GET startService

## Description

This simple api call starts a specific service daemon so user can find device in its favorite apps.

## Behavior

When this api is called for a service, user is able to find device as an endpoint to stream music.

***
## Parameters
> + `service` - _required_ : Service Name (Valid names are SpotifyConnect, UPnP, AirPlay or Roon)
***

## Example
**Request**
    http://localhost:5000/startService
    
**Return**
```json
{
    "status": "success"
}
```
