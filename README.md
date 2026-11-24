# Commit Chord

Hear any public GitHub repo. Type `owner/repo` and its last 100 commits play as a tune.

**Live:** https://vinceychu.github.io/commit-chord/

| In the repo | In the tune |
| --- | --- |
| First byte of the commit hash | Pitch (so the same repo always gives the same tune) |
| Author | Color, octave and timbre |
| Merge commit | Chord |
| Message starting with `fix` | Short pluck |
| Message starting with `revert` | Note that slides down |
| Long message | Longer note |
| A day or a week with no commits | Rest |

Pick a mood (scale) and a tempo, copy a link that reopens the same tune, or download it as a WAV.

## How it works

One static file, `index.html`. No build step, no backend, no tracking. It calls the public GitHub REST API from your browser (60 requests an hour per network without a token) and synthesises the sound with the Web Audio API. If GitHub can't be reached it plays a clearly labelled made-up demo pattern.

Run it locally by opening `index.html`.

## License

MIT
