# fetch_wttr
fetch weather reports from `wttr.in`, with i3status compatibility 

Credit to `wttr.in` for doing all the actual work here. What an awesome
resource to have. 

## Installation
Dependent on `curl`, `getopt`, `bash` -- any GNU/Linux system should already have these installed.

Install to `/usr/bin`:

```
# install -Dm755 -t /usr/bin fetch_wttr
```

## i3status-rust block example
To include an automatically updating weather report in i3status-rust, create the following custom block in your i3status-rust config, replacing `[LOCATION]` with your location:

```
[[block]]
# Get current weather from wttr.in every 5 minutes
block = "custom" 
json = true
command = "fetch_wttr --json --location [LOCATION]"
interval = 300
```
