# Playlist service: GET Playlist Tracks
    GET getPlaylistTracks

## Description

Get an array with all available tracks to play in the selected playlist.
The plid should be sent as received after the getPlaylists request. This request should be performed at least once every 30s if in dynamic playlist mode, or once before the start to load tracklist in static playlist mode.

***
## Parameters
> + `service` - _required_ : Streaming Service Name (Valid names are Tidal, Qobuz or Local)
> + `plid` - _required_ : Playlist ID (Can be set to AUTO if user selected Dynamic Mode. For more informations [Playlist Modes](PLAYLISTMODE.md))
***

## Behavior

A call to this api **will NOT** immediately start the music player service in the backend. A further play toggle api call is required.
***

## Example
**Request**
    http://localhost:5000/getPlaylistTracks?service=Tidal&plid=498c9320-062e-4939-bb9c-e1446fa2cdb7
    
**Return**
```json
{
    "status": "success",
    "track_count": 3,
    "tracks": [
        {
            "name": "Heavy Metal Lover",
            "artist": "Lady Gaga",
            "album": "Born This Way",
            "cover": "http://images.osl.wimpmusic.com/im/im?w=512&h=512&albumid=77669919",
            "duration": 252,
            "quality": {
                "codec": "MP3",
                "bitrate": "320",
                "bitdepth": null,
                "samplerate": null
            }
        },
        {
            "name": "Sultans Of Swing",
            "artist": "Dire Straits",
            "album": "Dire Straits",
            "cover": "http://images.osl.wimpmusic.com/im/im?w=512&h=512&albumid=622353",
            "duration": 349,
            "quality": {
                "codec": "FLAC",
                "bitrate": "1411",
                "bitdepth": "16",
                "samplerate": "41.1"
            }
        },
        {
            "name": "Viva La Vida",
            "artist": "Coldplay",
            "album": "Viva La Vida or Death and All His Friends",
            "cover": "http://images.osl.wimpmusic.com/im/im?w=512&h=512&albumid=1783269",
            "duration": 242,
            "quality": {
                "codec": "MQA",
                "bitrate": "4608",
                "bitdepth": "24",
                "samplerate": "96"
            }
        }
    ]
}
```
