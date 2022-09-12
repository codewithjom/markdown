# :point_right: Xorg DPMS 

## Table of Contents

- [What is DPMS](#what-is-dpms)
- [Setting up DPMS in X](#setting-up-dpms-in-x)

## What is DPMS

DPMS (Display Power Management Signaling) enables power saving behaviour of monitors when the computer is not in use. The time of inactivity before the monitor enters into a given saving power level, by standby, suspend or off, can be set as described in `DPMSSetTimeouts`. Note that DPMS was developed for CRT monitors, and on LCD displays, there is normally no difference between the standby, suspend and off modes.

## Setting up DPMS in X

> :book: **NOTE**: As of Xorg 1.8 DPMS is auto detected and enabled if ACPI is also enabled at kernel runtime.

Add the following to a file in `/etc/X11/xorg.conf.d/` in the `Monitor` section:

``` sh
Options "DPMS" "true"
```

Add the following to the `ServerFlags` section, change the times (in minutes) as necessary:

``` sh
Option "StandbyTime" "10"
Option "SuspendTime" "20"
Option "OffTime" "30"
```

> :book: **NOTE**: If the `"OffTime"` option does not work, use screen blanking instead, which will keep the monitor turned on with a black image. Alternatively, change `"blanktime"` to `"0"` to disable screen blanking

``` sh
Option "BlankTime" "30"
```

An example file `/etc/X11/xorg.conf.d/10-monitor.conf` could look like this.

``` sh
Section "Monitor"
    Identifier "LVDS0"
    Option "DPMS" "false"
EndSection

Section "ServerFlags"
    Option "StandbyTime" "0"
    Option "SuspendTime" "0"
    Option "OffTime" "0"
    Option "BlankTime" "0"
EndSection

Section "ServerLayout"
    Identifier "ServerLayout0"
EndSection
```
