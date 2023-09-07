# This repository is now deprecated
I've archived this repository because Vantra Hub moved to a new custom server and API.

# Vantra Data
Welcome to the github repository where Vantra's public data is stored in.
<br>
<br>
<b>Please know: Vantra's Changelogs are written in a way to work with Roblox's RichText feature.</b>

# Code Example
This simple lua code prints the current Vantra Version and Changelog to your console in Roblox.
<br>
```
local changelog = request(
    {
        Url = "https://raw.githubusercontent.com/VantraRoblox/VantraData/main/changelog.txt",
        Method = "GET"
    }
)

local version = request(
    {
        Url = "https://raw.githubusercontent.com/VantraRoblox/VantraData/main/version.txt",
        Method = "GET"
    }
)

repeat wait() until version.StatusCode == 200 and changelog.StatusCode == 200

print("Vantra Version: " .. version.Body)
print("Vantra Changelog: " .. changelog.Body)
```
