# DWM UART Instructions

## Running UART

Find serial port being used:

```$ dmesg | grep tty```

Once you get the correct serial port for *ACM* device, install *minicom* and run it with your serial port.

```$ minicom -D /dev/ttyS0```


## Set Network ID
```
dwm> nis 0x1234
nis: ok
```

## Set Device Mode

### Bridge
```dwm> nmb```

### Anchor

#### Initiator
A network must contain at least one initiator to initiate network.
```
dwm> nmi
enter
enter
```
Run `si` to verify:

```[000005.870 INF] mode: ani (act,real)```

#### Non-Initiator

```
dwm> nma
enter
enter
```
Run `si` to verify:

```[000003.140 INF] mode: an (act,-)```

## Tag

```
dwm> nmt
enter
enter
```
Run `si` to verify:

```[000005.080 INF] mode: tn (act,twr,np,le)```

### Set Position
Set coordinates in mm.

```dwm> aps <x> <y> <z>```

## Labels
Each node can have a label por identification purposes.

```
dwm> nls <label>
nis: ok
```
