# CCCTRL

CCCTRL Contains two Max For Live MIDI effects.

## CC Tool.amxd 

CC Tool.amxd is a Max For Live MIDI effect which allows MIDI CC values to be set from the arrangement view using Live automation tracks (live only has native support for setting these values from midi clips.

The tool has two views, narrow and wide.

In narrow view, the range of the value dial is 0-127. MIDI CC messages will be sent to the selected channel

In wide view, the range of the value dial is 0-16383. MIDI CC messages for the MSB will be sent to the channel selected with the Channel dial while CC messages for the LSB will be sent to the channel selected with the LSB Channel dial.

When the tool is in narrow view, input to the Wide Value dial will be ignored. 
Conversely when the tool is in wide view, input to the Value dial will be ignored.

The tool will pass through any MIDI CC messages to channels other than those it is configured to use, so multiple instances of the tool can be used to control multiple CC channels. 

Incoming MIDI CC messages on the configured channel are ignored.

## CC Env.amxd

CC Env.amxd is a gate triggered ADSR envelope generator for MIDI CC values.

As with the CC Tool, it has both narrow and wide views, which operate in the same manor. 

Unlike CC Tool it provides its own CC values. In the default mode it will trigger the ADSR envelope on the first key press, and will move the ADSR envelope to the release phase when the same key is released. It will ignore all other keypresses.

In Multi Trig mode, it will re-trigger the ADSR envelope for each fresh key press and will only move to the release phase once all keys are released.

As with CC Tool, multiple instances can be stacked in a single track to control multiple parameters

**NB** With my most basic synth, a Korg Volca Nubass, it is quite easy to overwhelm its tiny electronic brain by trying to automate too many parameters. It is also the only synth I have which exclusively uses a 5 pin MIDI rather than midi over USB, so I have not managed to isolate whether it is a limitation of that synth. I would appreciate anyone else seeing such behaviour raising an issue on github.
