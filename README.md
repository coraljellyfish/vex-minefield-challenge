# Vex IQ Clawbot Minefield

The robot used for this challenge is a clawbot, a robot that has an arm of sorts to pick up items. I also added an extension to my robot -- a storage space to store objects that were picked up.

For this challenge, the robot was supposed to navigate a "minefield" -- a small field with red cubes (mines) and green cubes (aid packs). The robot was supposed to avoid touching the mines, and pick up the aid packs and bring them back to the "Safe Zone."

<img width="667" alt="image" src="https://github.com/user-attachments/assets/9e62a183-9f9d-4129-bea8-585a2644e3fe">

There were three zones:
- Zone 1: 1 aid pack
- Zone 2: 2 aid packs
- Zone 3: 4 aid packs

With each run, the locations of aid packs and mines changed, but the places where they could be remained the same. (i.e. they were never just randomly scattered across the field, there were designated places for aid packs and mines)

However, time was also an issue, because the score was computed like this:
(Number of aid packs brought to safe zone) / (time + 10 seconds for each mine touched)

I had originally planned to check Zone 1 and Zone 3 to get at least 3 aid packs, but because that was easier said than done, I ended up going for Zone 1 only to get at least 1 aid pack and see the lowest time I could get. This code uses a gyro and color sensors to tell if a cube is red (mine)/green (aid pack).
