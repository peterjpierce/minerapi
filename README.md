# minerapi
Gather and display statistics for one or more rigs and GPUs that run 
[cgminer](https://github.com/ckolivas/cgminer) to mine cryptocurrencies.

## Installation
### Step 1: Enable RPC
Every instance of cgminer you wish to monitor must be running the RPC API.
To enable it, append the following to cgminer's command line invocation (or
the config file / shell script you run):

```
--api-listen --api-allow W:192.168.1.0/24 --api-mcast
```

In the above example, we allow connections from any IP address containing the
first three octets (192.168.1.xxx). For more information on security and the
`--api-allow` command, visit the [API-README](https://github.com/ckolivas/cgminer/blob/master/API-README)
on the cgminer repository.

### Step 2: Configure minerapi
Download this repository, and edit the `minerstat` file, configuring the `RIGS`
variable to list the machines you are monitoring. Separate each machine with
a newline, like so:

```
RIGS = """
    192.168.1.14
    192.168.1.15
"""
```

## Usage
Simply invoke `minerstat` from the command line once you have completed
the installation steps outlined above.

This has been tested on Linux, FreeBSD and Windows running Python 2.7.

## Donations
If you found this utility helpful, please consider donating to the author:

+ BTC: `1CavTJLrtRXfWJ5MKZH53dudfq9aWa3z6E`
+ LTC: `LhdsXnNjZyMJF8TrvV7y1pSmhyQSs9RyB7`
+ GLD: `E3qqqrLejCXVPjZD9XnabYNXvJ8nDeHymF`

Thank you!
