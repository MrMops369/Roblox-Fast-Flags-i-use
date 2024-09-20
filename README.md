# Fast Flags i know of
I will add what i think the fast flags are doing + games you can ue them in. (Nearly all of the fast flags are physics related and modify what your character does, serversided or clientsided)

If you want to find some exploitable fast flags yourself then you can search them yourself [here](https://raw.githubusercontent.com/MaximumADHD/Roblox-Client-Tracker/roblox/FVariables.txt) (big thanks to maximum adhd for this, the best things to search for are things like Humanoid, Velocity, HipHeight, PGS, Render, Debug and nearly anything thats a FInt)

If you want to test how much you can glitch out stuff, then just use very high/low numbers for Integer values (the highest/lowest values possible: -2147483648, 2147483648)

## "Invisibility" 
Anything higher than 9 will automatically set your CFrame to be 0,0,0 (the CFrame is serversided, you can still move around on the client)
Default: Unknown 

```Json
{
  "DFIntGameNetPVHeaderTranslationZeroCutoffExponent": 10
}
```   

Games: Ability Wars (Buff, Tree, Hive, Alchemist and Mushroom give you the ability to punch everyone while you are at 0,0,0), BIG Paintball, Blade ball 

## Physics Slowdown
This fast flag sets the current physics "FPS", this slows down all the physics related stuff aka falling, walking
Default: 16

```Json
{
  "DFIntMaxMissedWorldStepsRemembered":1
}
```


## Client Simulation Radius
Sets your clients simulation radius ( as far as i know )

```Json
{
  "DFIntMaxClientSimulationRadius":10000,
  "DFIntMinClientSimulationRadius":10000
}
```

Can be used in games with many unanchored parts that have no set network ownership

## Anti Kb (for all the Slap Battles/Ability Wars players)
This automatically teleports all ragdolled players limbs (except torso) to the games 0,0,0 (very unreliable, only drags your torso to the 0,0,0)
Default: Unknown

```Json
{
  "DFIntGameNetLocalSpaceMaxSendIndex":100000
}
```

Games: Slap Battles, Ability wars

## Hip Height modifier
makes you go bounce, on 0 you float a little bit above the ground, always needs to be below zero for bouncing

```Json
{
  "DFIntMaxAltitudePDStickHipHeightPercent":-2147483648
}
```

Games: Blade ball (at high values even the anti fling can't do anything -> ball can't kill you unless you don't parry it within like 40 secs or so)

## Active Physics FPS Change
Go into settings  and change your FPS to 240 (if you can reach that amount of FPS) and you will have full Physics speed, at 30 fps its around 7,5/s. Any Part you have network Ownershipship over is also slowed down, as well as shot projectiles.

```Json
{
  "FFlagGameBasicSettingsFramerateCap": "True",
  "DFIntTaskSchedulerTargetFps": 0,
  "DFIntMaxMissedWorldStepsRemembered":"1"
}
```

Games: any game (obbys are easier to do with slow Physics)

## Good Anti KB
This combination works with every game that uses Ragdolls (the Anti KB is always active). You can change the NewtonIts Flag to stop being stuck on walls or objects (anything below 0 Crashes your game)

```Json
{
  "DFIntDebugSimPrimalPreconditionerMinExp": "1",
  "DFIntDebugSimPrimalNewtonIts": "2",
  "DFIntDebugSimPrimalWarmstartForce": "0",
  "FFlagDebugSimDefaultPrimalSolver": "True",
  "DFIntDebugSimPrimalWarmstartVelocity": "0",
  "DFIntDebugSimPrimalToleranceInv": "1",
  "DFIntDebugSimPrimalPreconditioner": "1"
}
```

## Disable other players animations (Clientsided)

```Json
{
  "FFlagProcessAnimationLooped":"False",
  "FFlagReplicateAnimationLooped":"False"
}
```

## Disable Bloom
This disables all neon effects
```Json
{
  "FIntBloomFrmCutoff":"1654515",
  "FFlagRenderNoLowFrmBloom":"True"
}
```
## Speed up particle emitters

```Json
{
  "FFlagDebugDeterministicParticles":"True"
}
```
## Low quality roblox
The default value is -1
```Json
{
  "DFIntDebugDynamicRenderKiloPixels":"2"
}
```
## Get every possible error message the roblox client can offer
Only a gui. You don't get kicked from the game, but you can't move because of the UI blocking your input.
```Json
{
  "FFlagDebugEnableErrorStringTesting":"True"
}
```
## Change the Layered Clothing deform Limit
The changes are only clientsided. When you set it to the (positive) signed 32 bit integer Limit (2147483647), then you can create really large Clothing combinations. 
All deformations are disabled when put to a low value
```Json
{
  "DFIntLCCageDeformLimit":"2147483647"
}
```
