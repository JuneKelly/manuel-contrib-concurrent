# manuel-contrib-concurrent

Easily run [manuel](http://github.com/ShaneKilkelly/manuel) tasks
concurrently.

# Installation

Clone this repository into your manuel plugins directory
(`$HOME/.manuel.d/plugins` by default):
```bash
$ cd ~/.manuel.d/plugins
$ git clone git://github.com/ShaneKilkelly/manuel-contrib-concurrent.git
```

# Usage

Simply pass an array of commands to the `manuel_concurrent` function.

Example:
```bash
# in a manuelfile

load_plugin manuel-contrib-concurrent

function work_one {
  echo "working one"
  sleep 7
  echo "done one"
}

function work_two {
  echo "working two"
  sleep 4
  echo "done two"
}

function do_all_work {
  tasks=("work_one" "work_two")
  manuel_concurrent $tasks
}
```
