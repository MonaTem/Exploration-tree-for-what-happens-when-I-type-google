# your keyboard input is processed to the browser

## Physical part after key press

An electrical circuit specific to the enter key is closed (either directly or capacitively). This allows a small amount of current to flow into the logic circuitry of the keyboard, which scans the state of each key switch, debounces the electrical noise of the rapid intermittent closure of the switch, and converts it to a keycode integer, in this case 13. The keyboard controller then encodes the keycode for transport to the computer. This is now almost universally over a Universal Serial Bus (USB) or Bluetooth connection, but historically has been over PS/2 or ADB connections.

- [Go deeper for USB keyboards](./usb_keyboards/index.md)
- [Go deeper for Virtual Keyboards (as in touch screen devices)](./touchescreens/index.md)

## Logical part after key press

The OS dispatch the signal to the focused window (this process differs for each OS). And the graphical API of the window that receives the character prints the appropriate font symbol in the appropriate focused field.

## The browser receives the key

When you just press "g" the browser receives the event and the entire auto-complete machinery kicks into high gear. Depending on your browser's algorithm and if you are in private/incognito mode or not various suggestions will be presented to you in the dropbox below the URL bar. Most of these algorithms prioritize results based on search history and bookmarks. You are going to type "google.com" so none of it matters, but a lot of code will run before you get there and the suggestions will be refined with each key press. It may even suggest "google.com" before you type it.


## When you press enter

- The browser checks the hostname for characters that are not in ``a-z``, ``A-Z``, ``0-9``, ``-``, or ``.``. Since the hostname is ``google.com`` there won't be any, but if there were the browser would apply `Punycode`_ encoding to the hostname portion of the URL.
