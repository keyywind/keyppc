# keyppc Documentation

##### _PFPC(password, savepath, exceptions)_

|_argument_|_optional_|_default_|_available_|
|---|---|---|---|
|password|_no_| | [ string type ] |
|savepath|_yes_|"./"| [ string type ]|
|exceptions|_yes_|[]| [ list-pynput-key type ]|
|penalty|_yes_|"start chrome.exe"| [ string type ]|

##### Example of using this library

    from keyppc.keyppc import PFPC
    from pynput.keyboard import KeyCode, Key
    exceptions = [Key.esc, Key.ctrl, Key.end, KeyCode(char = 'o')]
    savepath = "./"
    password = "abcdefg"
    penalty = "start chrome.exe"
    PFPC(
      password = password,
      savepath = savepath,
      exceptions = exceptions,
      penalty = penalty
    ).run(chances = 5, verbose = True)
