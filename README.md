# MUMT306-Final-project
## Introduction/motivation: 
`	`Have you ever come across this anime girl studying with a pair of headset on YouTube? For me, this YouTube channel called lofi girl which livestreams lofi hip hop music has companied me for countless late night study sessions. Lofi hip hop is also called chill hop, it is a form of downtempo music that combines elements of hip hop and chill-out music. I like to have it on as background music while I’m studying because I found the perfect balance of the chill-out and upbeat vibes helps me stay awake and focused. Therefore, for this final project I decided to make a lofi hip hop beat maker so that I’ll have a more interactive and fun way to play my study music. 

## Design



The project is fully implemented in Max/Msp and it includes a 32-step drum sequencer and also provides additional features for other lofi hip hop elements. The Max patch can be divided into 3 sections. A drum sequencer, a filler instrument channel and a reverberator. To add more lofi vibe, there is also a collection of various white noises that the user can choose from to play in the background. The patch is designed to be as interactive as possible. The user can control the tempo of the beat by selecting a BPM value. Then it will be converted to milliseconds and be fed into a metro object. The drum sequencer simulates a real life drum sequencer and allows the users to create any pattern they want. A live.grid object is used to make the drum sequencer interface neater and easier to use. However, due to the variation and complication of the melody part, the filler instrument is only semi-interactive. The filler instrument panel allows the user to choose from some predefined chord progression patterns, a key from the piano keyboard interface, and will play that chosen chord progression in the selected key. The reverberator consists of different kinds of filters that are implemented as subpatches. In the main user interface, the levell of the reverb effect can be controlled through a slider.
## Subpatches
### The Chord progression generator

The arpeggiator exercise we did for homework is very helpful when implementing this. This patch takes the midi number of the input note and computes the rest of the chords in the progression.
###


###
###
### The Schroder Reverberator

To implement the reverberation effect, I followed the model developed by Prof. John Chowning from the CCRMA. As the figure shows, this model consists of a series[ connection](https://ccrma.stanford.edu/~jos/pasp/Series_Combination_One_Ports.html) of several [allpass filters](https://ccrma.stanford.edu/~jos/filters/Allpass_Filters.html), a parallel bank of [feedback comb filters](https://ccrma.stanford.edu/~jos/pasp/Feedback_Comb_Filters.html) and a mixing [matrix](https://ccrma.stanford.edu/~jos/mdft/Matrices.html). An allpass filter is a [signal processing filter](https://en.wikipedia.org/wiki/Filter_\(signal_processing\)) that passes all [frequencies](https://en.wikipedia.org/wiki/Frequency) equally in gain, but changes the [phase](https://en.wikipedia.org/wiki/Phase_\(waves\)) relationship among various frequencies. A comb filter is a [filter](https://en.wikipedia.org/wiki/Filter_\(signal_processing\)) implemented by adding a delayed version of a [signal](https://en.wikipedia.org/wiki/Signal_processing) to itself. Here are the subpatches I made for each of the elements shown in the figure.


`	`Allpass filter 			Comb filter                                                 signal mixer


## Limitations
The reverberator doesn’t work for the filler instrument since Schroeder reverberator only works for audio signals and the filler instrument is implemented with built in Max/msp objects.
## Conclusion
`	`Overall, I’m satisfied with the result I got. I was able to make some decent sounding beats with the Max patcher. However, there is definitely still a lot of room for improvements. For example, an additional Arduino interface can be made for the control panels (tempo, level of reverberation,etc..,) to make the project more interactive and interesting. The filler instrument can also be improved to make more various and complex melodies.
