## Node Daemon Manager

For using with thigs like Monit, etc. 

Install: `npm i -g nodaemon`

#### Usage:
```sh
nodaemon <command> <path> [name [pidfile [args [logs [log [error-log]]]]]] [options]
```

#### Commands:
- start
- stop
- restart

#### Options:
- `-p` or `--path`: Path to the script file or folder with `index.js`
- `-n` or `--name`: Name of the daemon *(default: the name of the script's parent folder)*
- `-i` or `--pid`: Path to the pid file *(default: /tmp/nodaemon-%name%.pid)*
- `-a` or `--args`: Arguments string to pass to the process *(default: empty)*
- `-l` or `--logs`: Path to the logs dir *(default: /tmp/)*
- `--log`: Path to the log file *(default: /tmp/nodaemon-%name%.log)*
- `--error-log`: Path to the error log file *(default: the same as --log)*
- `--npm`: Use `npm start` command instead of `node %path%`. In this case `%path%` should be a directory with `package.json` file. Also, you have to add `& echo $! > $PIDFILE` into the end of `npm start` command in the `package.json` file.

--

### MIT License

Copyright (c) 2018

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

