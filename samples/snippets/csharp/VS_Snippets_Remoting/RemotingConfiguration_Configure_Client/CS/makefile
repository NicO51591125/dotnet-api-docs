all : RemotingConfiguration_Configure_server.exe RemotingConfiguration_Configure_client.exe RemotingConfiguration_Configure_shared.dll

RemotingConfiguration_Configure_shared.dll : RemotingConfiguration_Configure_shared.cs
	csc /debug+ /nologo /t:library RemotingConfiguration_Configure_shared.cs

RemotingConfiguration_Configure_server.exe : RemotingConfiguration_Configure_server.cs RemotingConfiguration_Configure_shared.dll
	csc /debug+ /nologo /r:RemotingConfiguration_Configure_shared.dll RemotingConfiguration_Configure_server.cs

RemotingConfiguration_Configure_client.exe : RemotingConfiguration_Configure_client.cs RemotingConfiguration_Configure_shared.dll
	csc /debug+ /nologo /r:RemotingConfiguration_Configure_shared.dll RemotingConfiguration_Configure_client.cs

