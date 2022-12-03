Nothing fancy in this repo, just created to have blank sysmon config handy.
Based on sysmon version one should change schema version in config file, You can get the current schema version by using the "-? config" command line.
This config will include all the events.
--------------------------
# sysmon64.exe -? config 
--------------------------

<Sysmon schemaversion="4.83">
  <!-- Capture all hashes -->
  <HashAlgorithms>*</HashAlgorithms>
  <EventFiltering>
    
	<ProcessCreate onmatch="exclude"> </ProcessCreate>
	<FileCreateTime onmatch="exclude"> </FileCreateTime>
	<NetworkConnect onmatch="exclude"> </NetworkConnect>
	<ProcessTerminate onmatch="exclude" ></ProcessTerminate>
	<DriverLoad onmatch="exclude"> </DriverLoad>
  <ImageLoad="exclude"> </ImageLoad>
	<CreateRemoteThread onmatch="exclude"> </CreateRemoteThread>
  <RawAccessRead onmatch="exclude" ></RawAccessRead>
  <ProcessAccess onmatch="exclude"> </ProcessAccess>
	<FileCreate onmatch="exclude"> </FileCreate>
	<RegistryEvent onmatch="exclude"> </RegistryEvent>
	<FileCreateStreamHash onmatch="exclude"> </FileCreateStreamHash>
	<PipeEvent onmatch="exclude"> </PipeEvent>
  <WmiEvent onmatch="exclude" ></WmiEvent>
  <DNSQuery onmatch="exclude"> </DNSQuery>
	<FileDelete onmatch="exclude"> </FileDelete>
	<ClipboardChange onmatch="exclude"> </ClipboardChange>
	<ProcessTampering onmatch="exclude"> </ProcessTampering>
	<FileDeleteDetected onmatch="exclude"> </FileDeleteDetected>
  <FileBlockExecutable onmatch="exclude" ></FileBlockExecutable>
  <FileBlockShredding onmatch="exclude"> </FileBlockShredding>
    
  </EventFiltering>
</Sysmon>
