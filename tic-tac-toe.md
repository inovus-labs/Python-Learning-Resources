# A Tic-Tac-Toe Game 

## About the Program
> This is a project built for learning python . It is developed with python tkinter libray along with other regular libraries.
> 
## Source Code

```ino
nes (168 sloc)  6.6 KB

"""A tic-tac-toe game built with Python and Tkinter."""

import tkinter as tk
from itertools import cycle
from tkinter import font
from typing import NamedTuple


class Player(NamedTuple):
    label: str
    color: str


class Move(NamedTuple):
    row: int
    col: int
    label: str = ""


BOARD_SIZE = 3
DEFAULT_PLAYERS = (
    Player(label="X", color="blue"),
    Player(label="O", color="green"),
)
```