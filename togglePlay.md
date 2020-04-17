# Playlist service: Toggle Play/Pause
    GET togglePlay

## Description

This simple api call starts the music player daemon in the backend or toggles play/pause. This is mandatory to start automatically a playlist after it's been loaded using getPlaylistTracks method.

## Example
**Request**
    http://localhost:5000/togglePlay
    
**Return**
```json
{
    "status": "success"
}
```
