# Playlist service: GET Service Track
    GET getServiceTrack

## Description

When user streams music through a service listed in the block #2 (see [Project Flowchart](WORKFLOW.md)) is able to send tracks from apps to streamer individually (one at a time) so request response is very similar to a playlist get response, but the playlist array is always populated by just 1 element.

***
## Parameters
> + `service` - _required_ : Service Name (Valid names are SpotifyConnect, UPnP, AirPlay or Roon)
***

## Example
**Request**
    http://localhost:5000/getServiceTrack?service=SpotifyConnect
    
**Return**
```json
{
    "status": "success",
    "track_count": 1,
    "tracks": [
        {
            "name": "Viva La Vida",
            "artist": "Coldplay",
            "album": "Viva La Vida or Death and All His Friends",
            "cover": "http://images.osl.wimpmusic.com/im/im?w=512&h=512&albumid=1783269",
            "duration": 242,
            "quality": {
                "codec": "MP3",
                "bitrate": "320",
                "bitdepth": null,
                "samplerate": null
            }
        }
    ]
}
```
