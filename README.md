# PITCHGEN

## A little pitch pipe for puredata and TouchOSC

![Pitchgen puredata screenshot](screenshots/main-pd.png?raw=true)

### Features
* Sine tone pitch for any equal-tempered "note"
* Deviate from that by +/- 100 cents
* Add up to the 11th partial above that
* Control from your phone or tablet using [TouchOSC](https://hexler.net/software/touchosc)

![Pitchgen TouchOSC screenshot](screenshots/main-touchosc.png?raw=true) ![Pitchgen TouchOSC screenshot](screenshots/partials-touchosc.png?raw=true)

### NB
The pd patch supports the [purr-data / Pd-L2Ork](https://git.purrdata.net/jwilkes/purr-data) version of puredata, and it doesn't seem to work too well in pd-extended. Hasn't been tested in pd-vanilla.

### Setup
The pd patch will work fine on its own, but it's much easier to control from TouchOSC (and more fun). Your computer and your TouchOSC device will need to be on the same network, and you'll need to know their IP addresses.

1. Transfer `pitchgen.touchosc` to your phone and load it with TouchOSC (instructions [here](https://hexler.net/docs/touchosc-editor-sync))
2. Open `main.pd` in purr-data
3. Navigate to the `networking` subpatch
4. Input the IP address and port of your TouchOSC device
5. Input your computer's IP address and port in [TouchOSC](https://hexler.net/docs/touchosc-configuration-connections-osc)
6. Turn on the `NETWORKING` toggle in the main part of `main.pd`
7. Turn on the `DSP` toggle in the same patch
8. Make some sweet sine tones

#### Known Issues
* Accidentals are displayed poorly. Notably, sharps are rendered as dollarsigns.

Please feel free to download, use for practicing, post issues, or make pull requests. If you use it in a performance, I'd be flattered if you let me know.
