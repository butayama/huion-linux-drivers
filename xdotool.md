Xdotool - Keyboard

The xdotool is a utility used from the terminal or in a script to manually perform keyboard input. The commands can also be used to make a script of many xdotool commands to perform large tasks. Later articles will cover the xdotool ability to perform mouse input as well as window and desktop manipulation.

The syntax for xdotool depends on the command being used. Let's start with sending keystrokes to a window by using the 'key' command. The syntax is as follows:

key [options] [keys]

There are three options available for the key command:

    --window window_id – specified keys for the keystrokes are sent to the window_id application.
    --clearmodifiers – all modifiers are cleared, such as CAPS LOCK, NUM LOCK, shift held down, a mouse button held down, etc.
    --delay milliseconds – sets the delay between each keystroke being sent, the default is 12 ms.


The [keys] specify which keys are being sent to the specified window. The keys are based on the X Keysym strings and are:

    space
    exclam
    quotedbl
    numbersign
    dollar
    percent
    ampersand
    quoteright
    parenleft
    parenright
    bracketleft
    asterisk
    backslash
    plus
    bracketright
    comma
    asciicircum
    minus
    underscore
    period
    quoteleft
    slash
    semicolon
    less
    equal
    greater
    question
    at
    braceleft
    bar
    braceright
    asciitilde
    shift (Shift key)
    ctrl (Control key)
    alt (Alternate key)
    BackSpace
    F1-F12 (Function 1 key to Function 12 just use the number of the specific Function key)
    Return (Return or Enter key)

Each of these characters can be used separately and some together. A space is placed between individual keystrokes and simultaneous keystrokes are connected with a plus (+) sign. For example, to perform a single keystroke of a space and then an 'x' would be: 'space x'. When simultaneous keys are pressed, such as CTRL and 'x', the keystroke would be: 'ctrl+x'. Another example would be to open a file in LibreOffice Writer. The keystrokes would be 'alt+f o', or even the shortcut key 'ctrl+o'.

Looking at the previous options for the key command, you may have noticed the –window option which requires the window id. You may wonder how you find the id of a specific window. Finding the id is a simple procedure which will be covered more in another article, but I can give the basics of it now since it is needed.

To find the window id of a specific window, use the following command:

xdotool search --name TITLE