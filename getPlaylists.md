# Playlist service: GET Playlist List
    GET getPlaylists

## Description

Get an array with all available playlists to play along with their unique ID.
This is the same ID that should be passed as an argument when the playlist is going to be played.

***
## Parameters
> + `service` - _required_ : Streaming Service Name (Valid names are Tidal, Qobuz or Local)
***

## Example
**Request**
    http://localhost:5000/getPlaylists?service=Tidal
    
**Return**
```json
{
    "items_count": 4,
    "playlists": [
        {
            "id": "176eba0a-5c73-4edc-91fd-c0c032843e3d",
            "name": "AdvancedDAC",
            "duration": 630,
            "num_tracks": 3
        },
        {
            "id": "498c9320-062e-4939-bb9c-e1446fa2cdb7",
            "name": "HML",
            "duration": 252,
            "num_tracks": 1
        },
        {
            "id": "d0840a63-53ef-4436-a0d5-71f33432d7a0",
            "name": "Italiano",
            "duration": 360,
            "num_tracks": 2
        },
        {
            "id": "df77a868-0b1a-471d-b9d9-a4fd9b0a62da",
            "name": "Si",
            "duration": 1010,
            "num_tracks": 5
        }
    ]
}
```
