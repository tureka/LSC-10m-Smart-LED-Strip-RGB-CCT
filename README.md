# LSC-10m-Smart-LED-Strip-RGB-CCT
ESPHome code for LSC 10m Smart LED Strip RGB/CCT

After flashing this LED Strip with OpenBeken and finally with ESPHome, I've restored part of its functionality.
I've split code to device code (lsc-ledstrip.yaml) and functions code (smartled-common.yaml) in includes folder, because I have 4 of them in diffrent rooms.
For testing comfort, OTA security is removed.

What works?
# 1. CCT and RGB (not my work)
# 2. CCT - White light temperature and brightness in Home Assistant  (not my work)
# 3. CCT - Warm, Neutral, Cold white light on hardware button an remote
# 4. RGB - light, colors, brightness, effects in Home Assistant  (not my work)
# 6. Microphone (not my work, just added filter)
# 7. Hardware button functionality
##      long click - OFF -> CCT -> RGB -> OFF
##      short click - CCT (CW -> NW -> WW) / RGB (change effect)
# 8. IR and remote functions restored (may be diffrent from original functions)
# 9. Remote functions:
##    ON/OFF - unfortunately ON button needs to be used twice on first turn on
##    Brightness +/-
##    Colors and white light temps WW, NW, CW
##    Timers 1H, 2H, 3H (working script in background or it may send event to HA, not tested)
##    Effect speed +/- (native ESPHome effects with 7 speed presets)
##    Mode button to change effects (always speed 4 after change)
##    UP/DOWN Buttons to change static colors
##    Music buttons with four Music