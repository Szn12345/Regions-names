
[OnlineSubsystemMcp.Xmpp]
bUseSSL=true
ServerAddr="ws://yourip"
ServerPort=70

[OnlineSubsystemMcp.Xmpp Prod]
bUseSSL=true
ServerAddr="ws://yourip"
ServerPort=70

;Enable double pump for everyone
[ConsoleVariables]
;Weapon.TryToFireRestrictedByTypeCooldowns=0 ;doublepump disable with the thingy
n.VerifyPeer=0
FortMatchmakingV2.ContentBeaconFailureCancelsMatchmaking=0
Fort.ShutdownWhenContentBeaconFails=0
FortMatchmakingV2.EnableContentBeacon=0

;Glider redeploy? Not working yet iirc
;Fort.GliderRedeployRequiresJump=1
;Fort.GliderRedeployUseWindowOfTime=0
;Fort.GliderRedeployWindowLength=5.0
;Fort.GliderRedeployPreventSkydiving=1

[/Script/Qos.QosRegionManager]
NumTestsPerRegion=1
PingTimeout=3.0
!RegionDefinitions=ClearArray
+RegionDefinitions=(DisplayName="Blend NA", RegionId="NAE", bEnabled=true, bVisible=true, bAutoAssignable=false)
+RegionDefinitions=(DisplayName="Blend NA", RegionId="NAW", bEnabled=true, bVisible=false, bAutoAssignable=false)
+RegionDefinitions=(DisplayName="Blend OCE", RegionId="OCE", bEnabled=true, bVisible=false, bAutoAssignable=false)
+RegionDefinitions=(DisplayName="Blend EU", RegionId="EU", bEnabled=true, bVisible=true, bAutoAssignable=true)
+RegionDefinitions=(DisplayName="Blend ME", RegionId="ME", bEnabled=false, bVisible=false, bAutoAssignable=false)
+RegionDefinitions=(DisplayName="Blend BR", RegionId="BR", bEnabled=false, bVisible=false, bAutoAssignable=false)
+RegionDefinitions=(DisplayName="Blend AUTO", RegionId="AUTO", bEnabled=false, bVisible=false, bAutoAssignable=false)

;Modify gravity
;[/Script/Engine.PhysicsSettings]
;DefaultGravityZ=-280.000000
;DefaultTerminalVelocity=40.000000

;Not sure yet, appears to change graphics somehow
;[/Script/FortniteGame.FortWorldSettings]
;DefaultWorldTimeOfDayManager=/Game/TimeOfDay/TODM/MASTER_TODM.MASTER_TODM_C

[OnlineSubsystemMcp.OnlineWaitingRoomMcp]
bEnabled=false
ServiceName="waitingroom"
GracePeriod=300
RetryConfigUrl="https://s3-us-west-1.amazonaws.com/launcher-resources/waitingroom"

[OnlineSubsystemMcp]
bUsePartySystemV2=true

[OnlineSubsystemMcp.OnlinePartySystemMcpAdapter]
bUsePartySystemV2=true

[CrashContextProperties]
CrashReportClientRichText=NSLOCTEXT("FortGlobals", "FortniteCrashReportClientText", "Fortnite has crashed. Please join the Momentum server at https://discord.gg/fPdP7XWc to get support.")

[/Script/Qos.QosRegionManager]
; Fix ping timeout on mobile and switch
NumTestsPerRegion=1
PingTimeout=1.0

;Disable first shot accuracy
;[/Script/FortniteGame.FortGlobals]
;bFirstShotAccuracyDisabled=false
