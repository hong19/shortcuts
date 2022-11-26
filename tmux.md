[tmux shortcuts & cheatsheet](https://gist.github.com/MohamedAlaa/2961058)

start new:

    tmux
list sessions:

    tmux ls
In tmux, hit the prefix `ctrl+b` (my modified prefix is ctrl+a) and then:


## Sessions

    :new<CR>  new session
    s  list sessions
    $  name session

## <a name="WindowsTabs"></a>Windows (tabs)

    c  create window
    w  list windows
    n  next window
    p  previous window
    f  find window
    ,  name window
    &  kill window

## <a name="PanesSplits"></a>Panes (splits)

    %  vertical split
    "  horizontal split

    o  swap panes
    q  show pane numbers
    x  kill pane
    +  break pane into window (e.g. to select text by mouse to copy)
    -  restore pane from window
    ⍽  space - toggle between layouts
    <prefix> q (Show pane numbers, when the numbers show up type the key to goto that pane)
    <prefix> { (Move the current pane left)
    <prefix> } (Move the current pane right)
    <prefix> z toggle pane zoom


## Copy & Paste

    [  enter copy mode, in the copy mode, use hjkl to move and y to yark.  
    ]  paste 

### Prerequisite
In `~/.tmux.conf`, add 
```
setw -g mode-keys vi
bind-key -T copy-mode-vi 'v' send -X begin-selection 
bind-key -T copy-mode-vi 'y' send -X copy-selection-and-cancel 
``` 


    
