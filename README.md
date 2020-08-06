# PyMp3ToSheets
Converting raw mp3 files into printable music sheets

07/25/2020 -- Still in the early phase of things. Project on pause until I finish my finals.
Progress:
1) Troubleshooting with Librosa library. Finally got the library to load() my mp3 file, but only works through anaconda (Can't get it to work on my standalone environment)
2) Researched some quick things to do with Librosa & implemented some visual aspects of the mp3 for playing around
3) Researched libraries I would want to use for the project

To do:
1) Learning how to interact with Librosa library
2) Need to learn how to use Abjad library to generate music sheets
---- If #2 is not a good alternative to LilyPond --> Go back to using Mingus/Lilypond to generate music sheets


08/02/2020 -- Librosa Learning + Choice in Music Composition library
Updates:
1) Abjad library is not what I thought it was. Performs similar to Mingus which I already have knowledge of -- May look into it further after concluding Librosa exploration
2) Librosa learning:
--- a) Note detection via Chromatogram is pretty accurate
------- i) Cleaned up noise of chromatogram to enhance performance
--- b) Note duration via Chromatogram is however not accurate
------- i) Can be paired (maybe) with Onset detection to better determine when notes are played
------- ii) Using Onset of the note, duration can be determined by the time difference between notes being played

Progress: Working with only first 2 measures of song so far
1) Cleaned Chromatogram from original output by reducing noise & smoothing out note detection
2) Created onset detection, but having issues linking the time-scale from the onset array to chromatogram's time-scale
3) Played with Abjad briefly to see that it is essentially similar to mingus -- However no full testing yet.

To do:
1) Polish up onset detection
2) Find out if note durations can be obtained/determined via onset/chroma method pairing
3) Work on Abjad later once project progresses to music sheet generation
