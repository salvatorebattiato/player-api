# Playlist streaming available mode

## How does backend work? Static or Dynamic
At the state of the art, in the first page user choose one of the streaming services currently natively supported: Tidal and Qobuz. <br>
Entering in one of these two requires a further choose: Static or Dynamic playing. <br>

* **Static** mode means that user will choose a personal playlist from a list and then playlist tracks are loaded once so user can go back and forth the tracks without using the phone app of the corresponding music service. It's just about choosing a playlist and let it sound.
* **Dynamic** mode means that a new playlist will be created in user streaming account, called for example "Queue". At a first time Queue is empty and server is waiting for user to add music and as soon as user adds songs from his smartphone app Queue playlist will be loaded and Dynamic mode can start playing music. When user skips or the song finishes the first Queue track (the earliest to be added) will be removed from the playlist. This means for example that going a track back is never allowed, as you will always play the first track of the playlist. <br>
This is a sort of FIFO logic where at the end of the streaming session the playlist Queue will be empty.<br>
Songs are added time by time by the user by adding more songs to the playlist Queue as long as old songs are removed. This way user can use its desktop/mobile app as a music browser without implementing a much more heavy proprietary api on the UI.

## What should frontend do?
That was a brief explanation of what backend do when you choose one or another mode.<br>
Keeping that in mind, frontend should behave a little bit differently regarding one or another mode.
* In **Static** mode frontend should also keep already-played tracks so user can go back and forth with remote and should load tracklist just once before playing toggle request is performed.
* In **Dynamic** mode frontend should never keep already-played tracks. Currently playing track should be always the first of the playlist. Skip is allowed. <br>
In this mode frontend should also continuously reload tracklist, at least once every 30 seconds and mandatorily for each skip/song finished event, as we never know when user added new music to the Queue playlist.
