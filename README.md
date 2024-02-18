# Fast Flags i know of
I will add what i think the fast flags are doing + games you can ue them in. (Nearly all of the fast flags are physics related and modify what your character does, serversided or clientsided)

If you want to find some exploitable fast flags yourself then you can search them yourself [here](https://raw.githubusercontent.com/MaximumADHD/Roblox-Client-Tracker/roblox/FVariables.txt) (big thanks to maximum adhd for this, the best things to search for are things like Humanoid, Velocity, HipHeight, PGS, Render, Debug and nearly anything thats a FInt)

If you want to test how much you can glitch out stuff, then just use very high/low numbers for Integer values (the highest/lowest values possible: -2147483648, 2147483648)

## "Invisibility" 
Anything higher than 9 will automatically set your CFrame to be 0,0,0 (the CFrame is serversided, you can still move around on the client)
Default: Unknown 

`{"DFIntGameNetPVHeaderTranslationZeroCutoffExponent": 10}`

Games: Ability Wars, BIG Paintball, Blade ball

## Physics Slowdown
This fast flag sets the current physics "FPS", this slows down all the physics related stuff aka falling, walking
Default: 16

`{"DFIntMaxMissedWorldStepsRemembered":1}`

Don't know in which games you can use this in

## Client Simulation Radius
Sets your clients simulation radius ( as far as i know )

`{"DFIntMaxClientSimulationRadius":10000, "DFIntMinClientSimulationRadius":10000}`

Can be used in games with many unanchored parts that have no set network ownership

## Anti Kb (for all the Slap Battles/Ability Wars players)
This automatically teleports all ragdolled players limbs (except torso) to the games 0,0,0 (very unreliable, only drags your torso to the 0,0,0)
Default: Unknown

`{"DFIntGameNetLocalSpaceMaxSendIndex":100000}`

Games: Slap Battles, Ability wars

## Hip Height modifier
makes you go bounce, on 0 you float a little bit above the ground, always needs to be below zero for bouncing

`{"DFIntMaxAltitudePDStickHipHeightPercent":-2147483648}`

Games: Blade ball (at high values even the anti fling can't do anything -> ball can't kill you unless you don't parry it within like 40 secs or so)

## FFlags where i don't rlly know what they do: 

`{"DFIntDefaultBalanceD":2147483648,"DFIntDefaultBalanceP":2147483648}`
