# SonyGPSAssist
Sony cameras which embed a GPS are able to use assist data to accelerate the
positioning.

This script downloads and writes Sony GPS assist data to SD cards under Linux.

# Requirements
SonyGPSAssist.bash needs the following commands:

- curl
- md5sum
- base64

# How it works
SonyGPSAssist.bash works in the following order:

- download the GPS assist data from Sony website,
- download the MD5 from Sony website,
- compare the MD5,
- look for each mount point which is FAT formatted and contains a PRIVATE/SONY
  directory that is also writable by the current user,
- create the directory PRIVATE/SONY/GPS if it does not already exist,
- write the GPS data into this directory.

