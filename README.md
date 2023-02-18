# Dump Firefox Session

Dump your current Firefox session, listing all windows and tabs, titles and URLs.

The script parses the `recovery.jsonlz4` file from your Firefox profile directory.

Inspired by: [https://gist.github.com/tmonjalo/33c4402b0d35f1233020bf427b5539fa](https://gist.github.com/tmonjalo/33c4402b0d35f1233020bf427b5539fa)


### Prerequisites

You will need the [Python3 LZ4 Compression Library](https://pypi.org/project/lz4/):

    # apt install python3-lz4


## Usage

Edit the `DEFAULT` location of your Firefox profile's `recovery.jsonlz4` file
in the `dump_firefox_session` and `save_firefox_session` files.

Now, run it:

    $ ./dump_firefox_session

	********************************************************************************
	1	swh/timemachine: A JACK aplication that can retrospectively record audio.	https://github.com/swh/timemachine
	1	gbevin/SendMIDI: Multi-platform command-line tool to send out MIDI messages	https://github.com/gbevin/SendMIDI/
	1	Water.css	https://watercss.netlify.app/
	1	New Tab	about:newtab
	********************************************************************************
	2	Audio Injector	https://www.audioinjector.net/rpi-hat
	2	streaming	https://www.rtl-sdr.com/tag/streaming/
	********************************************************************************
    .
    .
    .
    etc.

And to save a copy of the dump file, for archiving and viewing later:

    $ ./save_firefox_session
	firefox-recovery-2023-02-18T14:36:18.jsonlz4 written.

Finally, to view your saved dump file:

    $ ./dump_firefox_session firefox-recovery-2023-02-18T14:36:18.jsonlz4


