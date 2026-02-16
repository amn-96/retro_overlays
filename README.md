# Overlays I use:

- Odin 3: [Watomsk's Overlays](https://github.com/Watomsk/Overlays)
- Brick: [KrutzOtrem's Overlays](https://github.com/KrutzOtrem/Trimui-Brick-Overlays?tab=readme-ov-file)
- CubeXX: Combination of [BB64](https://community.muos.dev/t/bb64s-720x720-handheld-bezel-pack-gb-gbc-gba-ngpc-gg-vb-for-rg-cubexx/65) and the custom top-aligned overlays below.

# Custom Top-Aligned Overlays for 720x720 screens

For any platforms that aren't square, I prefer having the game pushed to the top of my screen because it's visually closer to the controls and slightly better for ergos. I wasn't able to find any overlays that accomplished this and also had no grids or scanlines included (I use shaders to get those) so I made my own. Some of them have shadow and no-shadow options; some just have the shadows.

Credits to [Watomsk](https://github.com/Watomsk/Overlays) for the iconography. All my custom overlays use the icons from his 1080p set, just realigned.

Tested on Anbernic RG CubeXX.

## GBA
Use with integer scaling and your choice of the BB64 GBA overlays (included).

This config is just retroarch settings on top of the already excellent 720x720 GBA overlays made by BB64.

#### Quick Menu -> On-Screen Overlay

| Setting | Value | Notes |
|---------|-------|-------|
| Overlay Preset | GBA | Your choice of BB64 GBA Overlays |
| (Portrait) Overlay Y Offset | 0.065 | The top of the overlay will be off screen, but the game itself will be top-aligned. |

#### Settings -> Video -> Scaling

| Setting | Value | Notes |
|---------|-------|-------|
| Integer Scale | ON | |
| Viewport Anchor Bias X | 0.5 | Setting doesn't matter |
| Viewport Anchor Bias Y | 0.0 | Required to align to top | 


## GBC 
Use with **non-integer scaling**.

#### Settings -> Video -> Scaling

| Setting | Value | Notes |
|---------|-------|-------|
| Integer Scale | OFF | |
| Viewport Anchor Bias X | 0.5 | Setting doesn't matter |
| Viewport Anchor Bias Y | 0.0 | Required to align to top |


## 4:3 (PSX, Dreamcast etc.)
Use with **non-integer scaling**.

#### Settings -> Video -> Scaling

| Setting | Value | Notes |
|---------|-------|-------|
| Integer Scale | OFF | |
| Viewport Anchor Bias X | 0.5 | Setting doesn't matter |
| Viewport Anchor Bias Y | 0.0 | Required to align to top |


## SNES / NES (~8:7)
This one is more involved. There are two options:

### Integer overscaled
This is exactly the same as the 3x integer overscale method talked about by RetroGameCorps in his review of the CubeXX. For some reason, Retroarch's viewport anchor bias settings didn't behave the way they should (?) and you need to set up a custom resolution and offest to work properly.

| Setting | Value | Notes |
|---------|-------|-------|
| Aspect Ratio | Custom | These correspond to 1:1 PAR (256x239) |
| Custom Aspect Ratio (X Position) | 0 | |
| Custom Aspect Ratio (Y Position) | -47 | |
| Custom Aspect Ratio (Width) | 768 (3x) | Use the DPAD to select the multipliers |
| Custom Aspect Ratio (Height) | 717 (3x) | Use the DPAD to select the multipliers |

The rest of the settings have no effect. 

### Non-integer scaled
This has the same effect as Integer Scale ON + Axis Y + Smart.

| Setting | Value | Notes |
|---------|-------|-------|
| Aspect Ratio | 1:1 PAR | |
| Viewport Anchor Bias X | 0.5 | This setting won't matter |
| Viewport Anchor Bias Y | 0.0 | Required for alignment |

With these settings, there will still be some blank space at the top (no idea why) but it does fit perfectly with the overlay.	

