# Sousveillance: Watching the watchers

Hack Manhattan has a [publicly accessible webcam](https://wiki.hackmanhattan.com/Camera).
[I](https://github.com/eaon) was uncomfortable with that setting (you creeps),
so my first attempt to evening the playing field was to at least know when
someone (from outside the space) checked the feed.

`nginx` is now used for proxying `mjpeg-streamer` and writes `agent.log` json
lines.

## Requirements

* `agent.log` with the following format in the same folder:
  `log_format camera escape=json '{"time": "$time_local", "ip": "$remote_addr", "action": "$request", "agent": "$http_user_agent", "referer": "$http_referer"}';`
* `jquery-2.2.4.min.js` in the same foldersousveillance/
