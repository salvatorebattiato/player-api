# Control service: skips to the next track in setlist
    GET nextTrack

## Description

This simple api call skips to the next track in setlist. This can be done both in Dynamic and Static playlist mode but just if there's another song after the one I want to skip.

## Example
**Request**
    http://localhost:5000/nextTrack
    
**Return**
```json
{
    "status": "success"
}
```
