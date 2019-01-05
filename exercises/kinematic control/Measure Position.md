# How to measure position

### Encoders

**Absolute**: it's an optical disk with a certain number of tracks, everyone has alternate opaque and transparent sectors. A light flash towards the track and detect if it's an opaque section or not, so that a photodiode catch this detection. It's often used with the Grey Code to have less errors on detection.

**Incremental**: optical disk with two tracks and one absolute zero for position reference; the two tracks have opaque and transparent sections. Signals are fed in a digital counterwith a D-flip-flop to sense direction and used for reset. 

### Resolvers

It's made up by a rotor and stator which has two windings at 90 electrical degrees dfference. On this windings, when applied a tension on rotor, it's induced current. This current is manipulated and then demodulated to be sent to a converter in frequency which pulses are detected by a counter.
