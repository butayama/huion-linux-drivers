After commenting out the lines as recommended, the tablet buttons seemd to be responsive. Button 11 and 10 were OK, After pressing button 9 an error occured. The tablet did not answer to movements of the pen.
After plugging and reconnecting the tablet, the pen is reactive and seems to work. The buttons showed some unexpected behavior after testing the bookmark functions of PyCharm. Instead of ctrl+shift+2  ctrl+shift+F2 was executed.
 
```
(venv) uwes@hpi5:/mnt/Volume/GitHub/huion-linux-drivers$ sudo ./huion-tablet-driver.py
[sudo] password for uwes: 
Finding USB device. . . Done!
grabbed interface %d 0
grabbed interface %d 1
grabbed interface %d 2
Reading configuration. . . Done!
Setting up driver. . . Done!
        Tablet model name         1060 PLUS
        Buttons                   ENABLED (12)
        Scrollbar                 disabled (0)
        Notifications:            ENABLED
                for buttons       ENABLED
                for scrollbar     disabled
        Screen                    disabled

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
                        < DEBUG MODE ENABLED >
Enabled by default. You can disable it by setting debug_mode = false
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

SYSTEM: Linux 4.19.0-8-amd64 (x86_64 )
#1 SMP Debian 4.19.98-1 (2020-01-26)

DEVICE: /dev/input/event18 (py-evdev-uinput)
bus: 0003, vendor 0001, product 0001, version 0003

      ENDPOINT 0x81: Interrupt IN ==========================
       bLength          :    0x7 (7 bytes)
       bDescriptorType  :    0x5 Endpoint
       bEndpointAddress :   0x81 IN
       bmAttributes     :    0x3 Interrupt
       wMaxPacketSize   :   0x10 (16 bytes)
       bInterval        :    0x2

TABLET CAPABILITIES:
[('SYN_REPORT', 0), ('SYN_CONFIG', 1), ('SYN_DROPPED', 3), ('?', 21)]
[(['BTN_DIGI', 'BTN_TOOL_PEN'], 320), ('BTN_TOUCH', 330), ('BTN_STYLUS', 331), ('BTN_STYLUS2', 332)]
[(('ABS_X', 0), AbsInfo(value=0, min=0, max=50800, fuzz=0, flat=0, resolution=0)), (('ABS_Y', 1), AbsInfo(value=0, min=0, max=31750, fuzz=0, flat=0, resolution=0)), (('ABS_PRESSURE', 24), AbsInfo(value=0, min=0, max=8191, fuzz=0, flat=0, resolution=0)), (('ABS_TILT_X', 26), AbsInfo(value=0, min=0, max=255, fuzz=0, flat=0, resolution=0)), (('ABS_TILT_Y', 27), AbsInfo(value=0, min=0, max=255, fuzz=0, flat=0, resolution=0))]

VPEN:
name "Tablet Monitor Pen 183943", bus "BUS_USB", vendor "0001", product "0001", version "0003", phys "py-evdev-uinput"
event types: EV_SYN EV_KEY EV_ABS

XINPUT:

Huion Kamvas driver should now be running. . .

(Input from the tablet will be printed out)

[menu_pycharm_10b]
button 0 = key shift+F11      # Show bookmarks
button 1 = key ctrl+shift+1   # test button with bookmark
button 2 = key ctrl+shift+2   # test button with bookmark
button 3 = key ctrl+shift+3   # test button with bookmark
button 4 = key ctrl+shift+4   # test button with bookmark
button 5 = key ctrl+shift+7    # test button with bookmark
button 6 = key ctrl+shift+8    # test button with bookmark
button 7 = key ctrl+shift+9    # test button with bookmark
button 8 = key ctrl+alt+s      # Settings
button 9 = key ctrl+shift+F12  # toggle maximize Editoturn right (krita)
button 10 = 
button 11 = 
07 e0 01 01 00 08 00 00 
07 e0 01 01 00 00 00 00 
07 e0 01 01 00 04 00 00 
07 e0 01 01 00 00 00 00 
07 e0 01 01 00 02 00 00 
No protocol specified
Error: Can't open display: (null)
Failed creating new xdo instance
ERROR running the following comand:
        xdotool key ctrl+shift+F12  # toggle maximize Editoturn right (krita)
RETURN CODE: 1

---------------------------------------------------------------------------  

The results of test with another button assignment are posted below.
The pen responded only after unplug - plug the tablet.

(venv) uwes@hpi5:/mnt/Volume/GitHub/huion-linux-drivers$ sudo ./huion-tablet-driver.py
Finding USB device. . . Done!
grabbed interface %d 0
grabbed interface %d 1
grabbed interface %d 2
Reading configuration. . . Done!
Setting up driver. . . Done!
Tablet model name 1060 PLUS
Buttons ENABLED (12)
Scrollbar disabled (0)
Notifications: ENABLED
for buttons ENABLED
for scrollbar disabled
Screen disabled

                        < DEBUG MODE ENABLED >
Enabled by default. You can disable it by setting debug_mode = false

SYSTEM: Linux 4.19.0-8-amd64 (x86_64 )
#1 SMP Debian 4.19.98-1 (2020-01-26)

DEVICE: /dev/input/event18 (py-evdev-uinput)
bus: 0003, vendor 0001, product 0001, version 0003

  ENDPOINT 0x81: Interrupt IN ==========================
   bLength          :    0x7 (7 bytes)
   bDescriptorType  :    0x5 Endpoint
   bEndpointAddress :   0x81 IN
   bmAttributes     :    0x3 Interrupt
   wMaxPacketSize   :   0x10 (16 bytes)
   bInterval        :    0x2

TABLET CAPABILITIES:
[('SYN_REPORT', 0), ('SYN_CONFIG', 1), ('SYN_DROPPED', 3), ('?', 21)]
[(['BTN_DIGI', 'BTN_TOOL_PEN'], 320), ('BTN_TOUCH', 330), ('BTN_STYLUS', 331), ('BTN_STYLUS2', 332)]
[(('ABS_X', 0), AbsInfo(value=0, min=0, max=50800, fuzz=0, flat=0, resolution=0)), (('ABS_Y', 1), AbsInfo(value=0, min=0, max=31750, fuzz=0, flat=0, resolution=0)), (('ABS_PRESSURE', 24), AbsInfo(value=0, min=0, max=8191, fuzz=0, flat=0, resolution=0)), (('ABS_TILT_X', 26), AbsInfo(value=0, min=0, max=255, fuzz=0, flat=0, resolution=0)), (('ABS_TILT_Y', 27), AbsInfo(value=0, min=0, max=255, fuzz=0, flat=0, resolution=0))]

VPEN:
name "Tablet Monitor Pen 194326", bus "BUS_USB", vendor "0001", product "0001", version "0003", phys "py-evdev-uinput"
event types: EV_SYN EV_KEY EV_ABS

XINPUT:

Huion Kamvas driver should now be running. . .

(Input from the tablet will be printed out)

[menu_pycharm_12]
button 0 = key 0 # Show bookmarks
button 1 = key 1 # test button with bookmark
button 2 = key 2 # test button with bookmark
button 3 = key 3 # test button with bookmark
button 4 = key 4 # test button with bookmark
button 5 = key 5 # test button with bookmark
button 6 = key 6 # test button with bookmark
button 7 = key 7 # test button with bookmark
button 8 = key 8 # Settings
button 9 = key 9 # toggle maximize Editoturn right (krita)
button 10 = key 0
button 11 = key 1
...
07 e0 01 01 01 00 00 00
No protocol specified
Error: Can't open display: (null)
Failed creating new xdo instance
ERROR running the following comand:
xdotool key 0 # Show bookmarks
RETURN CODE: 1
(venv) uwes@hpi5:/mnt/Volume/GitHub/huion-linux-drivers$ sudo ./huion-tablet-driver.py
Finding USB device. . . Done!
Reading configuration. . . Done!
Setting up driver. . . Done!
Tablet model name 1060 PLUS
Buttons ENABLED (12)
Scrollbar disabled (0)
Notifications: ENABLED
for buttons ENABLED
for scrollbar disabled
Screen disabled

                        < DEBUG MODE ENABLED >
Enabled by default. You can disable it by setting debug_mode = false

SYSTEM: Linux 4.19.0-8-amd64 (x86_64 )
#1 SMP Debian 4.19.98-1 (2020-01-26)

DEVICE: /dev/input/event18 (py-evdev-uinput)
bus: 0003, vendor 0001, product 0001, version 0003

  ENDPOINT 0x81: Interrupt IN ==========================
   bLength          :    0x7 (7 bytes)
   bDescriptorType  :    0x5 Endpoint
   bEndpointAddress :   0x81 IN
   bmAttributes     :    0x3 Interrupt
   wMaxPacketSize   :   0x10 (16 bytes)
   bInterval        :    0x2

TABLET CAPABILITIES:
[('SYN_REPORT', 0), ('SYN_CONFIG', 1), ('SYN_DROPPED', 3), ('?', 21)]
[(['BTN_DIGI', 'BTN_TOOL_PEN'], 320), ('BTN_TOUCH', 330), ('BTN_STYLUS', 331), ('BTN_STYLUS2', 332)]
[(('ABS_X', 0), AbsInfo(value=0, min=0, max=50800, fuzz=0, flat=0, resolution=0)), (('ABS_Y', 1), AbsInfo(value=0, min=0, max=31750, fuzz=0, flat=0, resolution=0)), (('ABS_PRESSURE', 24), AbsInfo(value=0, min=0, max=8191, fuzz=0, flat=0, resolution=0)), (('ABS_TILT_X', 26), AbsInfo(value=0, min=0, max=255, fuzz=0, flat=0, resolution=0)), (('ABS_TILT_Y', 27), AbsInfo(value=0, min=0, max=255, fuzz=0, flat=0, resolution=0))]

VPEN:
name "Tablet Monitor Pen 194423", bus "BUS_USB", vendor "0001", product "0001", version "0003", phys "py-evdev-uinput"
event types: EV_SYN EV_KEY EV_ABS

XINPUT:

Huion Kamvas driver should now be running. . .

(Input from the tablet will be printed out)

[menu_pycharm_12]
button 0 = key 0 # Show bookmarks
button 1 = key 1 # test button with bookmark
button 2 = key 2 # test button with bookmark
button 3 = key 3 # test button with bookmark
button 4 = key 4 # test button with bookmark
button 5 = key 5 # test button with bookmark
button 6 = key 6 # test button with bookmark
button 7 = key 7 # test button with bookmark
button 8 = key 8 # Settings
button 9 = key 9 # toggle maximize Editoturn right (krita)
button 10 = key 0
button 11 = key 1
07 e0 01 01 00 00 00 00
07 e0 01 01 02 00 00 00
No protocol specified
Error: Can't open display: (null)
Failed creating new xdo instance
ERROR running the following comand:
xdotool key 1 # test button with bookmark
RETURN CODE: 1
```