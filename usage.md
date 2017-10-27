# Usage

A visual guide to using EyeJam, an eye-controlled application for 
realtime-oriented music performance and composition.

## The Clip Launcher

The main interface to EyeJam is the clip launching window. This is the window
seen when EyeJam first starts. 

![The Clip Launcher Screen](images/launcher.png)

The internal clock plays by default, but there is no sound. In order to 
make any sound, a clip needs to be launched. A **clip** is a short chunk of 
music (be it melodic, harmonic/chordal, or percussive in nature). Compositions
in EyeJam are composed of little clips that can be mixed and matched together.
A clip in eyejam is tied to a specific instrument in what is known as a
**clip region**.

### Clip Regions

A clip region is a group 5 clips. If you use your imagination, they kind of look 
like ponies. 

![Clip Region](images/region.png)

There are 4 clip regions inside of EyeJam. Each region controls a different
kind of instrument: Melody, Melody 2, Drums, and Chords.

### Selecting a Clip
Each clip inside a clip region is represented by a white square button. 
Dwelling on a clip will cause it to be selected.

![Selected Clip](images/button_selected.png)


### Scheduled clips

A selected clip will often briefly be a cyan color and pulse to the beat:

![Scheduled Clip](images/scheduled.png)

This means that the particular clip is **scheduled** to be played. A clip
will wait until the next *downbeat* (first beat of a measure) to play the clip. 
That way, the clip being played is *quantized* and aligned precisely to the
beat of the song.

### Playing Clips

A clip that is currently is being played will show up as grey:

![Playing  Clip](images/playing.png)

There can only be one playing clip per clip region. 

### Turning off clips

The way to turn off a clip depends on the mode they are in.
Clips can either be in looped mode or single-shot mode. 
The clips melody clip region are in single-shot mode: the clip will play, and 
will automatically turn themselves off when they reach the end of their clip.
Looping clips will play continuously, and can be stopped by re-launching the
clip, or selecting another clip in the region.

### Reset Button

Dwelling on the **reset button** will cause all the clips to immediately turn
off. 

![Reset Button](images/reset.png)

### Play Button

Dwelling on the **play button** will resume playback of Eyejam, assuming it 
is stopped.

![Play](images/play.png)


### Stop Button

Dwelling on the **stop button** will stop all sound for EyeJam. 

![Stop](images/stop.png)


### Tempo Control 

Dwelling on the +/- buttons will increase/decrease the tempo by 5 BPM. 

![Tempo Control](images/tempo.png)

### XY control

Dwelling on the XY control button turns on XY mode. In XY mode, 
a global filter and feedback delay effect is turned on. The XY position of the
eye pointer continuously maps to the effect parameters. The X-axis maps to
delay feedback amount and filter resonance, and the Y-axis maps to filter 
cutoff.

![XY Control](images/xy.png)

### Edit Screen

Dwelling on the edit button takes you to the clip editor screen.

![Edit Button](images/edit.png)

## The Clip Editor

The clip editor is a general purpose editor for reprogramming clips found on
the clip launcher page. It features a piano roll for visualizing notes in time, 
and a series of buttons used to insert or remove notes in a given clip. 

![The Clip Editor Screen](images/editor.png)

### The Piano Roll

The piano roll is the used to visualize note information of the currently
selected clip. It can be read like a bar graph. Time moves on the x-axis in
equal steps, and pitches are plotted on the Y axis. 

![The Piano Roll](images/pianoroll.png)

### The Edit Playhead

The edit playhead is a green line which tells you where the current edit 
position is. This is analogous to an edit cursor in a word processor. A 
semi-transparent rectangle follows the edit playhead. This displays this
current edit step size. Notes that are inserted will also be at this length
as well.

![Edit Playhead](images/edit_playhead.png)

### The Playback Playhead

When a clip is playing, a vertical blue line will appear, indicated where
the current playback position is.

![Playback Playhead](images/playback_playhead.png)


### Navigation

The navigation buttons are found to the left of the piano roll. The left and
right keys move the playhead position forwards and backwards in time in 
edit step increments. The up and down keys scroll piano roll up and down, and
can be used to see notes out of range.

![Navigational Keys](images/navigation.png)


### Keyboard Input

The way to input notes into a clip is to use the keyboard interface. These
are series of buttons arranged to be a keyboard. When a note is pressed,
it will be inserted at the current edit position. The edit cursor will then 
move to the end of the note. The duration of the note is determined by the
edit step size.

![Keyboard](images/keyboard.png)

### Information

To the right of the keyboard, additional information about the current melody
editor state is displayed. **Octave** refers to the current keyboard octave. 
**Clip** refers to the current clip number being edited. **Track** refers
to the current track being edited.

![Note Information](images/info.png)

### Clip Operations

**Play Clip** will launch the clip currently being edited. 
**Next Clip** will go to the next clip in the track.
**Prev Clip** will go to the previous clip in the track.

![Clip Buttons](images/clip_buttons.png)

### Clear a clip
The button **Clear Clip** will clear all note information in the currently
selected clip.

![Clear Clip](images/clip_buttons.png)

### Track Operations
**Next Track** will select the next instrument track.
**Prev Track** will select the previous instrument track.

![Track Buttons](images/track_buttons.png)

### Changing Edit Step Size
**Step++** will increase the step size by 1.
**Step--** will decrease the step size by 1.

![Step Size](images/stepsize.png)

### Doubling and Halving Step Size
Often there are situations where changing the step size is too slow. 
The **Double** and **Half** buttons will double and halve the current edit step 
size.

![Double and Half](images/double_half.png)


### Removing a Note
The button **Remove** will remove a note. In order for a note to be removed, the
edit playhead must be at the beginning of the note. For polyphonic passages,
the correct voice channel must be selected.

![Remove a Note](images/remove.png)


### Polyphony 
![Polyphony Piano Roll](images/polyphony.png)

Polyphony editing in EyeJam is a little strange compared to other DAWs. This
is largely due to how things are handled under the hood (the EyeJam 
implemenation is simpler). A polyphonic instrument such as the drum kit or
the instrument for chord progressions has what will be referred as 
**voice channels**, where a particular voice is assigned to a particular 
channel. In eyejam, a maximum of 4 voice channels are implemented. 
As seen in the picture above, the voice channels are color coded: 
channel 1 is yellow, channel 2 is blue, channel 3 is red, and channel 4 
is green. 

The current voice channel can be changed using the **voice++** and the
**voice--** to increase and decrease the voice channel. The current channel
is indicated by the colored tint of the edit cursor bar. 

![Voice Buttons](images/voice_buttons.png)