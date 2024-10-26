## Sessions

### New Session

* `tmux new [-s name] [cmd]` (`:new`) - new session

### Switch Session

* `tmux ls` (`:ls`) - list sessions
* `tmux switch [-t name]` (`:switch`) - switches to an existing session
* `tmux as [id] [-t name]` (`:attach`) - attaches to an existing session
* `<C-s>c` (`:detach`) - detach the currently attached session
* `<C-s>(` - switch to next session
* `<C-s>)` - switch to previous session

### Session Management

* `<C-s>s` - list sessions
* `<C-s>$` - name session

### Close Session

* `tmux kill-session [-t name]` (`:kill-session`)

## Windows

### New Window

* `<C-s>c` (`:neww [-n name] [cmd]`) - new window

### Cursor Movement

* `<C-s>[i]` (`:selectw -t [i]`) - go to window `[i]`
* `<C-s>l` - go to last window
* `<C-s>p` - go to previous window
* `<C-s>n` - go to next window

### Window Management

* `<C-s>T` - rename window
* `<C-s>,` - rename window
* `<C-s>w` - list all windows
* `<C-s>f` - find window by name
* `<C-s>.` - move window to another session (promt)
* `:movew` - move window to next unused number

### Close Window

* `<C-s>&` (`:kill-window`) - kill window

## Panes

### New Pane

* (%) `<C-s>|` (`:splitw [-v] [-p width] [-t focus] [cmd]`) - split current pane vertically
* (") `<C-s>s` (`:splitw -h [-p width] [-t focus] [cmd]`) - split current pane horizontally

### Cursor Movement

* (o) `<C-s><Tab>` (`:selectp -t :.+`) - move cursor to the next pane
* `<C-s><Up>` (`:selectp -U`) - move cursor to the pane above
* `<C-s><Down>` (`:selectp -D`) - move cursor to the pane below
* `<C-s><Left>` (`:selectp -L`) - move cursor to the pane to the left
* `<C-s><Right>` (`:selectp -R`) - move cursor to the pane to the right
* `:selectp [i]` - move cursor to the pane `[i]`

### Panes Management

* (`:swap-pane -U`) - move current pane up
* (`:swap-pane -D`) - move current pane down
* `<C-s>{` (`:swap-pane -L`) - move current pane to the left
* `<C-s>}` (`:swap-pane -R`) - move current pane to the right
* `<C-s>q` - show pane numbers (type number to move cursor)
* `<C-s><Space>` - toggle pane arrangements

### Resize Pane

* `:resize-pane -U [i]` - move horizontal divider up by `[i]` lines
* `:resize-pane -D [i]` - move horizontal divider down by `[i]` lines
* `:resize-pane -L [i]` - move vertical divider left by `[i]` columns
* `:resize-pane -R [i]` - move vertical divider right by `[i]` columns

`resize-pane [-DLRUZ] [-x width] [-y height] [-t target-pane] [adjustment]`

### Close Pane

* `<C-s>x` (`:kill-pane`) - kill current pane

### Scroll

* `<C-s>[` -- enters scroll mode
* (while in scroll mode) 
* `q` - exits scroll mode
* `<S-k>` - scroll up
* `<S-j>` - scroll down

```
 The default command key bindings are:

[           Enter copy mode to copy text or view the history.

Function                     vi              emacs
--------                     --              -----
Half page down               C-d             M-Down
Half page up                 C-u             M-Up
Next page                    C-f             Page down
Previous page                C-b             Page up
Scroll down                  C-Down or C-e   C-Down
Scroll up                    C-Up or C-y     C-Up
Search again                 n               n
Search again in reverse      N               N
Search backward              ?               C-r
Search forward               /               C-s

```

## Misc

* `<C-s>t` - show time
* `<C-s>r` - reload config

## Sources

* http://robots.thoughtbot.com/post/2641409235/a-tmux-crash-course
* https://wiki.archlinux.org/index.php/Tmux
* https://gist.github.com/henrik/1967800
* http://blog.hawkhost.com/2010/06/28/tmux-the-terminal-multiplexer/
