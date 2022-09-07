# CCCTRL

CC Tool.amxd contains a Max For Live MIDI effect which allows MIDI CC values to be set from the arrangement view using Live automation tracks (live only has native support for setting these values from midi clips.

The tool has two views, narrow and wide.

In narrow view, the range of the value dial is 0-127. MIDI CC messages will be sent to the selected channel

In wide view, the range of the value dial is 0-16383. MIDI CC messages for the MSB will be sent to the channel selected with the Channel dial while CC messages for the LSB will be sent to the channel selected with the LSB Channel dial.

When the tool is in narrow view, input to the Wide Value dial will be ignored. 
Conversely when the tool is in wide view, input to the Value dial will be ignored.

The tool will pass through any MIDI CC messages to channels other than those it is configured to use, so multiple instances of the tool can be used to control multiple CC channels. 

Incoming MIDI CC messages on the configured channel are ignored.
