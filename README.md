# keymaps
### Setup
Install qmk package for arch and set it up.
 
  `yay qmk`
  `qmk setup`
  
### Build
Steps to build keymap and flash it from arch.
  1. `qmk new-keymap -kb mechwild/obe/f401`

Open the keymap.c file (location provided in the output of previous command).
Change any maps that need to be changed. List of keycodes [here](https://beta.docs.qmk.fm/using-qmk/simple-keycodes/keycodes_basic)
  
  2. `qmk compile -kb mechwild/obe/f401 -km obe_arch_401_multilayer`

If successful, disconnect keeb, hold ESC key and connect again to put it in DFU mode
Keeb should become unresponsive if it goes into DFU mode
  
  3. `qmk flash -kb mechwild/obe/f401 -km obe_arch_401_multilayer`

If there are any success messages, then it's good to go.
Disconnect keeb and reconnect, it should be working now.
