# dotnet-maui-bug-repro-ios-arm64
AL1012: 'arm64' is not a valid setting for option 'platform' thrown when localized resources are available and debugging on remote iOS device

**Workaround: .csproj**
```xml
<!-- Uncomment this to fix the build as a workaround for the following Bug: https://github.com/dotnet/maui/issues/10342 -->
<!--<GenerateSatelliteAssembliesForCore>true</GenerateSatelliteAssembliesForCore>-->
```

**Console output**
```
Build started...
1>------ Build started: Project: bug-ios-arm64, Configuration: Debug Any CPU ------
1>C:\Program Files\dotnet\sdk\7.0.100-rc.1.22431.12\Sdks\Microsoft.NET.Sdk\targets\Microsoft.NET.RuntimeIdentifierInference.targets(219,5): message NETSDK1057: You are using a preview version of .NET. See: https://aka.ms/dotnet-support-policy
1>Executing SayHello Task to establish a connection to a Remote Server. 
1>			Properties: 
1>				SessionId=dc1368a9a6dab0211bfb119e43a97cb6e416dfcae24548d35ca4417c3e3dd190, 
1>				Addresss=192.168.30.24, 
1>				SshPort=22, 
1>				TcpPort=50241, 
1>				User=Julian Ewers-Peters, 
1>				AppName=bugiosarm64,
1>				VisualStudioProcessId=18044,
1>				ContinueOnDisconnected=False
1>Executing SayHello Task to establish a connection to a Remote Server. 
1>			Properties: 
1>				SessionId=dc1368a9a6dab0211bfb119e43a97cb6e416dfcae24548d35ca4417c3e3dd190, 
1>				Addresss=192.168.30.24, 
1>				SshPort=22, 
1>				TcpPort=50241, 
1>				User=Julian Ewers-Peters, 
1>				AppName=bugiosarm64,
1>				VisualStudioProcessId=18044,
1>				ContinueOnDisconnected=False
1>Detected signing identity:
1>  Code Signing Key: "Apple Development: Julian Ewers-Peters (...)" (...)
1>  Provisioning Profile: "VS: WildCard Development" (...)
1>  Bundle Id: com.companyname.bug_ios_arm64
1>  App Id: P9BACKA8J2.com.companyname.bug_ios_arm64
1>Skipping analyzers to speed up the build. You can execute 'Build' or 'Rebuild' command to run analyzers.
1>ALINK : error AL1012: 'arm64' is not a valid setting for option 'platform'
1>Done building project "bug-ios-arm64.csproj" -- FAILED.
========== Build: 0 succeeded, 1 failed, 0 up-to-date, 0 skipped ==========
========== Elapsed 00:07,577 ==========
========== Deploy: 0 succeeded, 0 failed, 0 skipped ==========
========== Elapsed 00:07,577 ==========
```
