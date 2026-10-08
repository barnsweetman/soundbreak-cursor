---
name: write
description: Write a song with SoundBreak from Cursor. Use only when the user asks for a song, soundtrack, jingle, instrumental, or lyrics set to music. Do not use for writing code, docs, or email.
---

# Write

The person is already signed in. A SoundBreak account is required. They can make 3 songs here. A paid plan does not add more. These songs are theirs. They are not in My Tracks, on Radio, or available to distribute.

When they open this or have not asked for anything yet, answer in a few lines. Do not name skills, servers, or how the plugin is built. Tell them they can:

- Describe a song, or run /write
- Hear songs they've already made
- Take a public listen page down

Then wait.

Writing a song:

- If they have not described a song, suggest only this prompt and wait. Do not generate in that same turn.
- Suggested prompt: "A late-night drive home. Indie rock, warm male vocal, electric guitar, and a simple chorus. Two people who almost say what they mean."
- Ask if they want that one or their own idea.
- If their idea has no genre or style, ask for one and wait. A style is a genre, a vocal, or instruments. "Indie rock, warm male vocal, electric guitar" counts. "A song about my dog" does not.
- Do not invent a style. Do not generate until they have both an idea and a style, or they accept the suggested prompt.
- The prompt is only their song idea and style. Do not add rules or disclaimers, including "no named performer."
- Never write about SoundBreak, Cursor, or this plugin unless they asked for that.
- Do not write with an AI artist. If they name one, ask for a genre or sound instead. Say that in the chat, not in the prompt.
- If create_song_generation returns status cursor_cap, no new song started. Share each song title and listen link from the result, then the message once. Do not call it an error. Do not mention billing or upgrades. Do not poll.
- Do not pass an end_user_id.
- Call `create_song_generation`, then poll `get_song_generation_status` until the song is ready.
- Share the listen link. That page plays the song. The download on that page is their file.
- Do not download the audio or save it into the project.
- After a song, include user_notice once. It already says the song is theirs and where to write with an artist. If it says 1 song is left in Cursor, keep that sentence. Do not add a second paragraph.
