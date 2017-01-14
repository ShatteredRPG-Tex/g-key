This plugin allows you to use the macro G-Keys on any Logitech keyboard to directly control TeamSpeak 3 without rebinding them to other keys. It achieves this by using the debugger functions of the LUA scripting engine in the Logitech Gaming Software.


For use with a Logitech headset, use the followoing:
*Please note that "gkey == 1" refernces the key number.*

function OnEvent(event, gkey, family)
if family ~= "kbd" and family ~= "lhc" then
if gkey == 1 then
if event == "G_PRESSED" then
OutputDebugMessage("TS3_PTT_ACTIVATE")
end
if event == "G_RELEASED" then
OutputDebugMessage("TS3_PTT_DEACTIVATE")
end
end
end
end
