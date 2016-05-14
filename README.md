# Sousveillance: Watching the watchers

Hack Manhattan has a [publicly accessible webcam](https://wiki.hackmanhattan.com/Camera).
[I](https://github.com/eaon) was uncomfortable with that setting (you creeps),
so my first attempt to evening the playing field was to at least know when
someone (from outside the space) checked the feed.

`mjpeg-streamer` which ships its own http server doesn't support any logging,
so I'm using [ngrep](http://ngrep.sourceforge.net/) to dig through the incoming
traffic to see what/where/etc.

## Requirements

* ngrep
* `jquery-2.1.3.min.js` in /www/sousveillance/
