## Bugs Fixed

- **Listening streaks:** The app used to reset a streak when someone listened on Sunday after listening on Saturday; I fixed it by treating every next calendar day the same, so Saturday-to-Sunday now counts as consecutive.
- **Friends Listening Now:** The app used a rolling 24-hour window, which could show a friend from yesterday; I fixed it by only showing listening events from the current UTC day.
- **Search duplicates:** Search could return the same song more than once when tag joins produced repeated rows; I fixed it by searching the song table directly and returning each song only once.
- **Rating notifications:** The app saved ratings but did not tell the original song sharer; I fixed it by creating a `song_rated` notification when another user rates their song.
- **Playlist song lists:** The app accidentally removed the final song before returning playlist results; I fixed it by returning the full ordered list.
- **Adding songs to playlists:** The app could add a song without required playlist-entry details like position and added-by; I fixed it by inserting the playlist entry with all required metadata.
