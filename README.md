# hamster-dmenu

[dmenu](https://wiki.archlinux.org/index.php/Dmenu) interface for the [hamster time tracker](https://github.com/projecthamster/hamster).

On invocation, **hamster-dmenu** opens *dmenu* with the list of previously entered *hamster* tasks, ordered with the most recently entered task first.

You can enter a new task, or rely on the auto-completion to find a previous task. The task format is as per *hamster*: `activity@category`

## Usage

- To cancel, type escape;
- If you enter a single question mark ("?") the current/last activity of the day is sent to notify;
- If you enter a single minus sign ("-"), time tracking is stopped;
- Anything else will start a new task. Format is the *hamster* format: `activity@category`

**Note**: Just pressing enter without typing anything will not cancel, it will start the last entered task. This is how *dmenu* selects entries. To cancel you must press escape.

## Installation

**hamster-dmenu** is a shell script and depends on `hamster-cli`, `dmenu`, `notify-send`, `sed` and `awk`.

Just download the `hamster-dmenu` script and invoke it with parameters you want to pass to *dmenu* (You probably will want `-i` for case insensitive.). Here is how I invoke it:

```
   hamster-dmenu -i -fn "Arial-12" -nb "#666" -nf "#FFF"
```

(This requires dmenu with xft support - the Ubuntu version has it by default)
