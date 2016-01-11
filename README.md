# AsusWrtDdnsUpdater

A simple ddns-start skript for use with an Asus Router running AsusWrt by Merlin http://asuswrt.lostrealm.ca/

The script fetches the external IP and stores it locally in file and then updates this IP to dnsomatic, if and only if the fetched IP is different with the previous one stored in the file.

## Requirements

An Asus Router running Merlin's AsusWrt, see http://asuswrt.lostrealm.ca/ and an internal or external storage device attached or built-in the Asus Router

You *must* edit the script and provide your credentials, otherwise, the script will exit without doing anything!

Using your preferred editior, eg. vi, edit the file 

```
vi ddns-start
```
and update the following lines accordingly:

```
USERNAME=<Your DNSoMatic username here>
PASSWORD=<Your DNSoMatic password here>
```

## Installation

Put ddns-start into the jffs script folder, usually: 

```
/jffs/scripts
```

Typically, you would add a cron for running this script e.g. every hour

## Usage

Without any parameters, the script runs (almost) silent and logs into the specified logfile. The specified log file **must be writable**.

A "verbose" switch is available by executing the script as follows:

```
./ddns-start 1
```

## Caveats

For now, username and password are stored **unencrypted** or **otherwise secure** in the script, so please use at your own risk.
