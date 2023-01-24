# Ramble, Video Editing for the Lazy

Ramble makes it possible to quickly generate a video and subtitle from an annotated markdown script. It can be used to generate a simple video or a file that can be consumed by another app for additional touches.

## Tags

Ramble consumes markdown files with special tags. These include the following:

`> // Comments ignored by the script parser.`

`> SLIDE src=./slides/slide0.png`

`> CLIP src=./clips/clip0.mp4`

`> TRACK src=./tracks/track0.ogg`

`> VO name=example`

`> /VO`

## Tag Parameters

These tags accept similar parameters with the exception of comments (which do not have parameters) and VO tags (detailed below). For each tag the only required parameter is `src`.

`src={filepath}`: The source file for the tag in an appropriate format e.g. mp4 for clips, png for stills, etc.

`volume={number}`: The volume a track should be played at. During the import process most audio files will be normalized and noise reduced automatically. Volume provides a convenient way of setting the volume relative to that normalized value. For example a value of `0.5` means the track should be played at half the regular volume.

`delay={seconds}`: Manually delay the start of the element by some amount.