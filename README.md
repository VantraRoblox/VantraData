# Vantra Data
Welcome to the github repository where Vantra's public data is stored in.
<br>

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
