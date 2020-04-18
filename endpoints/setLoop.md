# Control service: set Repeat/Loop mode
    GET setLoop

## Description

This simple api call sets Normal/Loop/Repeat mode.


***
## Parameters
> + `mode` - _required_ : Loop mode (Valid names are Normal, Loop or Repeat)
***

## Example
**Request**
    http://localhost:5000/setLoop?mode=Loop
    
**Return**
```json
{
    "status": "success"
}
```
