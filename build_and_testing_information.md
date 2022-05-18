<h3>testing container</h3>

- Oracle VirtualBox 6.1.34.150636 (2022-03-23T0039+000)
- machine configured/enhanced with https://gist.github.com/eladkarako/3e6aee4c58ab0e8d6357d7ee24fb6cee#file-virtualbox-tricks-you-were-not-aware-of-and-installing-a-new-android-x86-machine-from-iso-and-network-monitoring-using-burp-suite-on-host-with-full-support-in-viewing-https-and-quic-decrypted-content-md

<h3>testing OS (just using the Windows "trial"/"grace period")</h3>

- Windows 10 19044.1706 AMD64 en-us <sub>(Feature update to Windows 10, version 21H2 (19044.1706))</sub> https://uupdump.net/fetchupd.php?arch=amd64&ring=rp&build=19044.1
- Windows 11 25115.1000 AMD64 en-us <sub>(Windows 11 Insider Preview 25115.1000 (rs_prerelease))</sub> https://uupdump.net/fetchupd.php?arch=amd64&ring=wif&build=latest

<h3>technical details</h3>

- updated to https://github.com/JannesP/AudioMirror/commit/a6adaadaadf6a37d762aed4d2ab934caebc535fb (December 10, 2021).
- signed using a test signature (will change, don't relay on it).
- configuration: DEBUG.
- platform architecture: x64 <sub>(AMD64)</sub>.
- VS C++ 2019 (16.3.0)
- Windows Driver Kit (WDK) - Windows 10.0.19041.685
- (Platform Toolset: WindowsKernelModeDriver10.0)

<h3>(NOTE: only configured for DEBUG x64, with any other configuration and architecture the build will fail.)</h3>

<hr/>

<details><summary>build log:</summary>

```txt
1>------ Build started: Project: AudioMirror, Configuration: Debug x64 ------
1>Building 'AudioMirror' with toolset 'WindowsKernelModeDriver10.0' and the 'Universal' target platform.
1>Stamping x64\Debug\AudioMirror.inf
1>Stamping [Version] section with DriverVer=05/17/2022,18.43.47.932
1>C:\Users\Elad\Desktop\AudioMirror\AudioMirror\AudioMirror.inf(5-5): warning 1324: [Version] section should specify PnpLockdown=1.
1>AdapterCommon.cpp
1>Driver.cpp
1>KsHelper.cpp
1>MinipairDescriptorFactory.cpp
1>MiniportTopology.cpp
1>MiniportWaveRT.cpp
1>MiniportWaveRTStream.cpp
1>MiniportWaveRTStreamAudioEngineNode.cpp
1>NewDelete.cpp
1>RegistryHelper.cpp
1>RingBuffer.cpp
1>SubdeviceCache.cpp
1>SubdeviceHelper.cpp
1>Generating Code...
1>Processed /NODEFAULTLIB (suppressing all default libs)
1>
1>Starting pass 1
1>
1>Searching libraries
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\\portcls.lib:
1>      Found __imp_PcGetPhysicalDeviceObject
1>        Referenced in AdapterCommon.obj
1>        Loaded portcls.lib(portcls.sys)
1>      Found __imp_PcInitializeAdapterDriver
1>        Referenced in Driver.obj
1>        Loaded portcls.lib(portcls.sys)
1>      Found __imp_PcDispatchIrp
1>        Referenced in Driver.obj
1>        Loaded portcls.lib(portcls.sys)
1>      Found __imp_PcAddAdapterDevice
1>        Referenced in Driver.obj
1>        Loaded portcls.lib(portcls.sys)
1>      Found __imp_PcRegisterSubdevice
1>        Referenced in SubdeviceHelper.obj
1>        Loaded portcls.lib(portcls.sys)
1>      Found __imp_PcRegisterPhysicalConnection
1>        Referenced in SubdeviceHelper.obj
1>        Loaded portcls.lib(portcls.sys)
1>      Found __imp_PcNewPort
1>        Referenced in SubdeviceHelper.obj
1>        Loaded portcls.lib(portcls.sys)
1>      Found __imp_PcNewMiniport
1>        Referenced in SubdeviceHelper.obj
1>        Loaded portcls.lib(portcls.sys)
1>      Found __IMPORT_DESCRIPTOR_portcls
1>        Referenced in portcls.lib(portcls.sys)
1>        Referenced in portcls.lib(portcls.sys)
1>        Referenced in portcls.lib(portcls.sys)
1>        Referenced in portcls.lib(portcls.sys)
1>        Referenced in portcls.lib(portcls.sys)
1>        Referenced in portcls.lib(portcls.sys)
1>        Referenced in portcls.lib(portcls.sys)
1>        Referenced in portcls.lib(portcls.sys)
1>        Loaded portcls.lib(portcls.sys)
1>      Found __NULL_IMPORT_DESCRIPTOR
1>        Referenced in portcls.lib(portcls.sys)
1>        Loaded portcls.lib(portcls.sys)
1>      Found portcls_NULL_THUNK_DATA
1>        Referenced in portcls.lib(portcls.sys)
1>        Loaded portcls.lib(portcls.sys)
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\\stdunk.lib:
1>      Found "public: __cdecl CUnknown::CUnknown(struct IUnknown *)" (??0CUnknown@@QEAA@PEAUIUnknown@@@Z)
1>        Referenced in AdapterCommon.obj
1>        Referenced in MiniportTopology.obj
1>        Referenced in MiniportWaveRT.obj
1>        Loaded stdunk.lib(stdunk.obj)
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\\libcntpr.lib:
1>      Found __guard_dispatch_icall_fptr
1>        Referenced in MiniportWaveRTStream.obj
1>        Referenced in MiniportWaveRTStreamAudioEngineNode.obj
1>        Referenced in SubdeviceCache.obj
1>        Referenced in SubdeviceHelper.obj
1>        Referenced in AdapterCommon.obj
1>        Referenced in Driver.obj
1>        Referenced in MiniportTopology.obj
1>        Referenced in MiniportWaveRT.obj
1>        Loaded libcntpr.lib(guard_support.obj)
1>      Found memcmp
1>        Referenced in KsHelper.obj
1>        Referenced in MiniportWaveRT.obj
1>        Loaded libcntpr.lib(memcmp.obj)
1>      Found __GSHandlerCheck
1>        Referenced in MiniportWaveRT.obj
1>        Loaded libcntpr.lib(gshandler.obj)
1>      Found _guard_dispatch_icall_nop
1>        Referenced in libcntpr.lib(guard_support.obj)
1>        Loaded libcntpr.lib(guard_dispatch.obj)
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\BufferOverflowFastFailK.lib:
1>      Found __security_check_cookie
1>        Referenced in MiniportWaveRT.obj
1>        Referenced in libcntpr.lib(gshandler.obj)
1>        Loaded BufferOverflowFastFailK.lib(amdsecgs.obj)
1>      Found __security_cookie
1>        Referenced in MiniportWaveRT.obj
1>        Referenced in BufferOverflowFastFailK.lib(amdsecgs.obj)
1>        Loaded BufferOverflowFastFailK.lib(gs_support.obj)
1>      Found __report_gsfailure
1>        Referenced in BufferOverflowFastFailK.lib(amdsecgs.obj)
1>        Loaded BufferOverflowFastFailK.lib(gs_report.obj)
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\ntoskrnl.lib:
1>      Found __imp_RtlAssert
1>        Referenced in MiniportWaveRT.obj
1>        Referenced in MiniportWaveRTStream.obj
1>        Referenced in MiniportWaveRTStreamAudioEngineNode.obj
1>        Referenced in SubdeviceHelper.obj
1>        Referenced in AdapterCommon.obj
1>        Referenced in Driver.obj
1>        Referenced in KsHelper.obj
1>        Referenced in MiniportTopology.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found DbgPrint
1>        Referenced in MiniportWaveRTStream.obj
1>        Referenced in RingBuffer.obj
1>        Referenced in SubdeviceCache.obj
1>        Referenced in SubdeviceHelper.obj
1>        Referenced in AdapterCommon.obj
1>        Referenced in Driver.obj
1>        Referenced in MiniportTopology.obj
1>        Referenced in MiniportWaveRT.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_ExFreePoolWithTag
1>        Referenced in RegistryHelper.obj
1>        Referenced in RingBuffer.obj
1>        Referenced in AdapterCommon.obj
1>        Referenced in MiniportWaveRT.obj
1>        Referenced in MiniportWaveRTStream.obj
1>        Referenced in NewDelete.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_DbgPrintEx
1>        Referenced in Driver.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_KeInitializeEvent
1>        Referenced in MiniportWaveRT.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_ExAllocatePoolWithTag
1>        Referenced in RingBuffer.obj
1>        Referenced in MiniportWaveRT.obj
1>        Referenced in MiniportWaveRTStream.obj
1>        Referenced in NewDelete.obj
1>        Referenced in RegistryHelper.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_ExAcquireFastMutex
1>        Referenced in MiniportWaveRT.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_ExReleaseFastMutex
1>        Referenced in MiniportWaveRT.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_KeFlushQueuedDpcs
1>        Referenced in MiniportWaveRTStream.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_KeSetEvent
1>        Referenced in MiniportWaveRTStream.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_KeInitializeSpinLock
1>        Referenced in MiniportWaveRTStream.obj
1>        Referenced in RingBuffer.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_KeAcquireSpinLockRaiseToDpc
1>        Referenced in MiniportWaveRTStream.obj
1>        Referenced in MiniportWaveRTStreamAudioEngineNode.obj
1>        Referenced in RingBuffer.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_KeReleaseSpinLock
1>        Referenced in MiniportWaveRTStream.obj
1>        Referenced in MiniportWaveRTStreamAudioEngineNode.obj
1>        Referenced in RingBuffer.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_ExAllocateTimer
1>        Referenced in MiniportWaveRTStream.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_ExSetTimer
1>        Referenced in MiniportWaveRTStream.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_ExCancelTimer
1>        Referenced in MiniportWaveRTStream.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_ExDeleteTimer
1>        Referenced in MiniportWaveRTStream.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_RtlInitUnicodeString
1>        Referenced in RegistryHelper.obj
1>        Referenced in SubdeviceHelper.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_ZwClose
1>        Referenced in RegistryHelper.obj
1>        Referenced in SubdeviceHelper.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_ZwCreateKey
1>        Referenced in RegistryHelper.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_ZwOpenKey
1>        Referenced in RegistryHelper.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_ZwEnumerateKey
1>        Referenced in RegistryHelper.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_ZwEnumerateValueKey
1>        Referenced in RegistryHelper.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_ZwSetValueKey
1>        Referenced in RegistryHelper.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_RtlFreeUnicodeString
1>        Referenced in SubdeviceHelper.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_IoRegisterDeviceInterface
1>        Referenced in SubdeviceHelper.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_IoOpenDeviceInterfaceRegistryKey
1>        Referenced in SubdeviceHelper.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_IoSetDeviceInterfacePropertyData
1>        Referenced in SubdeviceHelper.obj
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __imp_ExFreePool
1>        Referenced in stdunk.lib(stdunk.obj)
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found __IMPORT_DESCRIPTOR_ntoskrnl
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>      Found ntoskrnl_NULL_THUNK_DATA
1>        Referenced in ntoskrnl.lib(ntoskrnl.exe)
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\hal.lib:
1>      Found __imp_KeQueryPerformanceCounter
1>        Referenced in MiniportWaveRTStream.obj
1>        Referenced in MiniportWaveRTStreamAudioEngineNode.obj
1>        Loaded hal.lib(HAL.dll)
1>      Found __IMPORT_DESCRIPTOR_HAL
1>        Referenced in hal.lib(HAL.dll)
1>        Loaded hal.lib(HAL.dll)
1>      Found HAL_NULL_THUNK_DATA
1>        Referenced in hal.lib(HAL.dll)
1>        Loaded hal.lib(HAL.dll)
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\wmilib.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\wdf\kmdf\x64\1.15\WdfLdr.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\wdf\kmdf\x64\1.15\WdfDriverEntry.lib:
1>      Found FxDriverEntry
1>        Loaded WdfDriverEntry.lib(stub.obj)
1>      Found "long __cdecl FxStubInitTypes(void)" (?FxStubInitTypes@@YAJXZ)
1>        Referenced in WdfDriverEntry.lib(stub.obj)
1>        Loaded WdfDriverEntry.lib(inittypes.obj)
1>      Found "void __cdecl FxStubUnbindClasses(struct _WDF_BIND_INFO *)" (?FxStubUnbindClasses@@YAXPEAU_WDF_BIND_INFO@@@Z)
1>        Referenced in WdfDriverEntry.lib(stub.obj)
1>        Loaded WdfDriverEntry.lib(classbind.obj)
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\\portcls.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\\stdunk.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\\libcntpr.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\BufferOverflowFastFailK.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\ntoskrnl.lib:
1>      Found __imp_RtlCopyUnicodeString
1>        Referenced in WdfDriverEntry.lib(stub.obj)
1>        Loaded ntoskrnl.lib(ntoskrnl.exe)
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\hal.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\wmilib.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\wdf\kmdf\x64\1.15\WdfLdr.lib:
1>      Found WdfVersionBind
1>        Referenced in WdfDriverEntry.lib(stub.obj)
1>        Loaded WdfLdr.lib(WDFLDR.SYS)
1>      Found WdfVersionUnbind
1>        Referenced in WdfDriverEntry.lib(stub.obj)
1>        Loaded WdfLdr.lib(WDFLDR.SYS)
1>      Found WdfVersionBindClass
1>        Referenced in WdfDriverEntry.lib(classbind.obj)
1>        Loaded WdfLdr.lib(WDFLDR.SYS)
1>      Found WdfVersionUnbindClass
1>        Referenced in WdfDriverEntry.lib(classbind.obj)
1>        Loaded WdfLdr.lib(WDFLDR.SYS)
1>      Found __IMPORT_DESCRIPTOR_WDFLDR
1>        Referenced in WdfLdr.lib(WDFLDR.SYS)
1>        Referenced in WdfLdr.lib(WDFLDR.SYS)
1>        Referenced in WdfLdr.lib(WDFLDR.SYS)
1>        Referenced in WdfLdr.lib(WDFLDR.SYS)
1>        Loaded WdfLdr.lib(WDFLDR.SYS)
1>      Found WDFLDR_NULL_THUNK_DATA
1>        Referenced in WdfLdr.lib(WDFLDR.SYS)
1>        Loaded WdfLdr.lib(WDFLDR.SYS)
1>
1>Finished searching libraries
1>
1>Finished pass 1
1>
1>
1>Searching libraries
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\\portcls.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\\stdunk.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\\libcntpr.lib:
1>      Found _load_config_used
1>        Loaded libcntpr.lib(loadcfg.obj)
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\BufferOverflowFastFailK.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\ntoskrnl.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\hal.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\wmilib.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\wdf\kmdf\x64\1.15\WdfLdr.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\wdf\kmdf\x64\1.15\WdfDriverEntry.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\\portcls.lib:
1>    Searching C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\\stdunk.lib:
1>
1>Finished searching libraries
1>
1>
1>Unused libraries:
1>  C:\Program Files (x86)\Windows Kits\10\lib\10.0.19041.0\km\x64\wmilib.lib
1>
1>    Discarded IID_IPort from AdapterCommon.obj
1>    Discarded IID_IResourceList from AdapterCommon.obj
1>    Discarded IID_IMusicTechnology from AdapterCommon.obj
1>    Discarded IID_IDmaChannel from AdapterCommon.obj
1>    Discarded IID_IInterruptSync from AdapterCommon.obj
1>    Discarded IID_IServiceSink from AdapterCommon.obj
1>    Discarded IID_IServiceGroup from AdapterCommon.obj
1>    Discarded IID_IRegistryKey from AdapterCommon.obj
1>    Discarded IID_IPortMidi from AdapterCommon.obj
1>    Discarded IID_IMiniportMidi from AdapterCommon.obj
1>    Discarded IID_IMiniportMidiStream from AdapterCommon.obj
1>    Discarded IID_IPortWaveCyclic from AdapterCommon.obj
1>    Discarded IID_IMiniportWaveCyclic from AdapterCommon.obj
1>    Discarded IID_IMiniportWaveCyclicStream from AdapterCommon.obj
1>    Discarded IID_IPortWavePci from AdapterCommon.obj
1>    Discarded IID_IPortWavePciStream from AdapterCommon.obj
1>    Discarded IID_IMiniportWavePci from AdapterCommon.obj
1>    Discarded IID_IMiniportWavePciStream from AdapterCommon.obj
1>    Discarded IID_IPortWaveRTStream from AdapterCommon.obj
1>    Discarded IID_IPortWMIRegistration from AdapterCommon.obj
1>    Discarded IID_IPortClsSubdeviceEx from AdapterCommon.obj
1>    Discarded IID_IPortClsPower from AdapterCommon.obj
1>    Discarded IID_IPortClsRuntimePower from AdapterCommon.obj
1>    Discarded IID_IPinName from AdapterCommon.obj
1>    Discarded IID_IPortClsEtwHelper from AdapterCommon.obj
1>    Discarded IID_IPortClsStreamResourceManager from AdapterCommon.obj
1>    Discarded IID_IPortClsStreamResourceManager2 from AdapterCommon.obj
1>    Discarded IID_IAdapterPnpManagement from AdapterCommon.obj
1>    Discarded IID_IMiniportPnpNotify from AdapterCommon.obj
1>    Discarded IID_IPortClsPnp from AdapterCommon.obj
1>    Discarded IID_IAdapterPowerManagement2 from AdapterCommon.obj
1>    Discarded IID_IAdapterPowerManagement3 from AdapterCommon.obj
1>    Discarded IID_IPowerNotify from AdapterCommon.obj
1>    Discarded IID_IWaveCyclicClock from AdapterCommon.obj
1>    Discarded IID_IWavePciClock from AdapterCommon.obj
1>    Discarded IID_IPortEvents from AdapterCommon.obj
1>    Discarded IID_IDrmPort from AdapterCommon.obj
1>    Discarded IID_IDrmPort2 from AdapterCommon.obj
1>    Discarded IID_IPortClsVersion from AdapterCommon.obj
1>    Discarded IID_IPinCount from AdapterCommon.obj
1>    Discarded IID_IPreFetchOffset from AdapterCommon.obj
1>    Discarded IID_IUnregisterSubdevice from AdapterCommon.obj
1>    Discarded CLSID_PortMidi from AdapterCommon.obj
1>    Discarded CLSID_PortWaveCyclic from AdapterCommon.obj
1>    Discarded CLSID_PortWavePci from AdapterCommon.obj
1>    Discarded CLSID_MiniportDriverFmSynth from AdapterCommon.obj
1>    Discarded CLSID_MiniportDriverUart from AdapterCommon.obj
1>    Discarded CLSID_MiniportDriverFmSynthWithVol from AdapterCommon.obj
1>    Discarded DEVPKEY_KsAudio_PacketSize_Constraints from AdapterCommon.obj
1>    Discarded DEVPKEY_KsAudio_Controller_DeviceInterface_Path from AdapterCommon.obj
1>    Discarded DEVPKEY_KsAudio_PacketSize_Constraints2 from AdapterCommon.obj
1>    Discarded IID_IMiniportAudioEngineNode from AdapterCommon.obj
1>    Discarded IID_IMiniportAudioSignalProcessing from AdapterCommon.obj
1>    Discarded IID_IPortClsNotifications from AdapterCommon.obj
1>    Discarded EventTraceGuid from AdapterCommon.obj
1>    Discarded SystemTraceControlGuid from AdapterCommon.obj
1>    Discarded EventTraceConfigGuid from AdapterCommon.obj
1>    Discarded DefaultTraceSecurityGuid from AdapterCommon.obj
1>    Discarded PrivateLoggerNotificationGuid from AdapterCommon.obj
1>    Discarded GUID_MAX_POWER_SAVINGS from AdapterCommon.obj
1>    Discarded GUID_MIN_POWER_SAVINGS from AdapterCommon.obj
1>    Discarded GUID_TYPICAL_POWER_SAVINGS from AdapterCommon.obj
1>    Discarded NO_SUBGROUP_GUID from AdapterCommon.obj
1>    Discarded ALL_POWERSCHEMES_GUID from AdapterCommon.obj
1>    Discarded GUID_POWERSCHEME_PERSONALITY from AdapterCommon.obj
1>    Discarded GUID_ACTIVE_POWERSCHEME from AdapterCommon.obj
1>    Discarded GUID_IDLE_RESILIENCY_SUBGROUP from AdapterCommon.obj
1>    Discarded GUID_IDLE_RESILIENCY_PERIOD from AdapterCommon.obj
1>    Discarded GUID_DEEP_SLEEP_ENABLED from AdapterCommon.obj
1>    Discarded GUID_DEEP_SLEEP_PLATFORM_STATE from AdapterCommon.obj
1>    Discarded GUID_DISK_COALESCING_POWERDOWN_TIMEOUT from AdapterCommon.obj
1>    Discarded GUID_EXECUTION_REQUIRED_REQUEST_TIMEOUT from AdapterCommon.obj
1>    Discarded GUID_VIDEO_SUBGROUP from AdapterCommon.obj
1>    Discarded GUID_VIDEO_POWERDOWN_TIMEOUT from AdapterCommon.obj
1>    Discarded GUID_VIDEO_ANNOYANCE_TIMEOUT from AdapterCommon.obj
1>    Discarded GUID_VIDEO_ADAPTIVE_PERCENT_INCREASE from AdapterCommon.obj
1>    Discarded GUID_VIDEO_DIM_TIMEOUT from AdapterCommon.obj
1>    Discarded GUID_VIDEO_ADAPTIVE_POWERDOWN from AdapterCommon.obj
1>    Discarded GUID_MONITOR_POWER_ON from AdapterCommon.obj
1>    Discarded GUID_DEVICE_POWER_POLICY_VIDEO_BRIGHTNESS from AdapterCommon.obj
1>    Discarded GUID_DEVICE_POWER_POLICY_VIDEO_DIM_BRIGHTNESS from AdapterCommon.obj
1>    Discarded GUID_VIDEO_CURRENT_MONITOR_BRIGHTNESS from AdapterCommon.obj
1>    Discarded GUID_VIDEO_ADAPTIVE_DISPLAY_BRIGHTNESS from AdapterCommon.obj
1>    Discarded GUID_CONSOLE_DISPLAY_STATE from AdapterCommon.obj
1>    Discarded GUID_ALLOW_DISPLAY_REQUIRED from AdapterCommon.obj
1>    Discarded GUID_VIDEO_CONSOLE_LOCK_TIMEOUT from AdapterCommon.obj
1>    Discarded GUID_ADVANCED_COLOR_QUALITY_BIAS from AdapterCommon.obj
1>    Discarded GUID_ADAPTIVE_POWER_BEHAVIOR_SUBGROUP from AdapterCommon.obj
1>    Discarded GUID_NON_ADAPTIVE_INPUT_TIMEOUT from AdapterCommon.obj
1>    Discarded GUID_ADAPTIVE_INPUT_CONTROLLER_STATE from AdapterCommon.obj
1>    Discarded GUID_DISK_SUBGROUP from AdapterCommon.obj
1>    Discarded GUID_DISK_MAX_POWER from AdapterCommon.obj
1>    Discarded GUID_DISK_POWERDOWN_TIMEOUT from AdapterCommon.obj
1>    Discarded GUID_DISK_IDLE_TIMEOUT from AdapterCommon.obj
1>    Discarded GUID_DISK_BURST_IGNORE_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_DISK_ADAPTIVE_POWERDOWN from AdapterCommon.obj
1>    Discarded GUID_DISK_NVME_NOPPME from AdapterCommon.obj
1>    Discarded GUID_SLEEP_SUBGROUP from AdapterCommon.obj
1>    Discarded GUID_SLEEP_IDLE_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_STANDBY_TIMEOUT from AdapterCommon.obj
1>    Discarded GUID_UNATTEND_SLEEP_TIMEOUT from AdapterCommon.obj
1>    Discarded GUID_HIBERNATE_TIMEOUT from AdapterCommon.obj
1>    Discarded GUID_HIBERNATE_FASTS4_POLICY from AdapterCommon.obj
1>    Discarded GUID_CRITICAL_POWER_TRANSITION from AdapterCommon.obj
1>    Discarded GUID_SYSTEM_AWAYMODE from AdapterCommon.obj
1>    Discarded GUID_ALLOW_AWAYMODE from AdapterCommon.obj
1>    Discarded GUID_USER_PRESENCE_PREDICTION from AdapterCommon.obj
1>    Discarded GUID_STANDBY_BUDGET_GRACE_PERIOD from AdapterCommon.obj
1>    Discarded GUID_STANDBY_BUDGET_PERCENT from AdapterCommon.obj
1>    Discarded GUID_STANDBY_RESERVE_GRACE_PERIOD from AdapterCommon.obj
1>    Discarded GUID_STANDBY_RESERVE_TIME from AdapterCommon.obj
1>    Discarded GUID_STANDBY_RESET_PERCENT from AdapterCommon.obj
1>    Discarded GUID_ALLOW_STANDBY_STATES from AdapterCommon.obj
1>    Discarded GUID_ALLOW_RTC_WAKE from AdapterCommon.obj
1>    Discarded GUID_LEGACY_RTC_MITIGATION from AdapterCommon.obj
1>    Discarded GUID_ALLOW_SYSTEM_REQUIRED from AdapterCommon.obj
1>    Discarded GUID_POWER_SAVING_STATUS from AdapterCommon.obj
1>    Discarded GUID_ENERGY_SAVER_SUBGROUP from AdapterCommon.obj
1>    Discarded GUID_ENERGY_SAVER_BATTERY_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_ENERGY_SAVER_BRIGHTNESS from AdapterCommon.obj
1>    Discarded GUID_ENERGY_SAVER_POLICY from AdapterCommon.obj
1>    Discarded GUID_SYSTEM_BUTTON_SUBGROUP from AdapterCommon.obj
1>    Discarded GUID_POWERBUTTON_ACTION from AdapterCommon.obj
1>    Discarded GUID_SLEEPBUTTON_ACTION from AdapterCommon.obj
1>    Discarded GUID_USERINTERFACEBUTTON_ACTION from AdapterCommon.obj
1>    Discarded GUID_LIDCLOSE_ACTION from AdapterCommon.obj
1>    Discarded GUID_LIDOPEN_POWERSTATE from AdapterCommon.obj
1>    Discarded GUID_BATTERY_SUBGROUP from AdapterCommon.obj
1>    Discarded GUID_BATTERY_DISCHARGE_ACTION_0 from AdapterCommon.obj
1>    Discarded GUID_BATTERY_DISCHARGE_LEVEL_0 from AdapterCommon.obj
1>    Discarded GUID_BATTERY_DISCHARGE_FLAGS_0 from AdapterCommon.obj
1>    Discarded GUID_BATTERY_DISCHARGE_ACTION_1 from AdapterCommon.obj
1>    Discarded GUID_BATTERY_DISCHARGE_LEVEL_1 from AdapterCommon.obj
1>    Discarded GUID_BATTERY_DISCHARGE_FLAGS_1 from AdapterCommon.obj
1>    Discarded GUID_BATTERY_DISCHARGE_ACTION_2 from AdapterCommon.obj
1>    Discarded GUID_BATTERY_DISCHARGE_LEVEL_2 from AdapterCommon.obj
1>    Discarded GUID_BATTERY_DISCHARGE_FLAGS_2 from AdapterCommon.obj
1>    Discarded GUID_BATTERY_DISCHARGE_ACTION_3 from AdapterCommon.obj
1>    Discarded GUID_BATTERY_DISCHARGE_LEVEL_3 from AdapterCommon.obj
1>    Discarded GUID_BATTERY_DISCHARGE_FLAGS_3 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_SETTINGS_SUBGROUP from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_THROTTLE_POLICY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_THROTTLE_MAXIMUM from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_THROTTLE_MAXIMUM_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_THROTTLE_MINIMUM from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_THROTTLE_MINIMUM_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_FREQUENCY_LIMIT from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_FREQUENCY_LIMIT_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_ALLOW_THROTTLING from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_IDLESTATE_POLICY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERFSTATE_POLICY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_INCREASE_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_INCREASE_THRESHOLD_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_DECREASE_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_DECREASE_THRESHOLD_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_INCREASE_POLICY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_INCREASE_POLICY_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_DECREASE_POLICY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_DECREASE_POLICY_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_INCREASE_TIME from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_INCREASE_TIME_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_DECREASE_TIME from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_DECREASE_TIME_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_TIME_CHECK from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_BOOST_POLICY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_BOOST_MODE from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_AUTONOMOUS_MODE from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_ENERGY_PERFORMANCE_PREFERENCE from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_ENERGY_PERFORMANCE_PREFERENCE_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_AUTONOMOUS_ACTIVITY_WINDOW from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_DUTY_CYCLING from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_IDLE_ALLOW_SCALING from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_IDLE_DISABLE from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_IDLE_STATE_MAXIMUM from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_IDLE_TIME_CHECK from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_IDLE_DEMOTE_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_IDLE_PROMOTE_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_INCREASE_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_DECREASE_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_INCREASE_POLICY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_DECREASE_POLICY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_MAX_CORES from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_MAX_CORES_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_MIN_CORES from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_MIN_CORES_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_INCREASE_TIME from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_DECREASE_TIME from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_AFFINITY_HISTORY_DECREASE_FACTOR from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_AFFINITY_HISTORY_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_AFFINITY_WEIGHTING from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_OVER_UTILIZATION_HISTORY_DECREASE_FACTOR from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_OVER_UTILIZATION_HISTORY_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_OVER_UTILIZATION_WEIGHTING from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CORE_PARKING_OVER_UTILIZATION_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PARKING_CORE_OVERRIDE from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PARKING_PERF_STATE from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PARKING_PERF_STATE_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PARKING_CONCURRENCY_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PARKING_HEADROOM_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PARKING_DISTRIBUTION_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_SOFT_PARKING_LATENCY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_HISTORY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_HISTORY_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_INCREASE_HISTORY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_DECREASE_HISTORY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_CORE_PARKING_HISTORY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_LATENCY_HINT from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_LATENCY_HINT_PERF from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_PERF_LATENCY_HINT_PERF_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_LATENCY_HINT_MIN_UNPARK from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_LATENCY_HINT_MIN_UNPARK_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_DISTRIBUTE_UTILITY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_HETEROGENEOUS_POLICY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_HETERO_DECREASE_TIME from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_HETERO_INCREASE_TIME from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_HETERO_DECREASE_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_HETERO_INCREASE_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CLASS0_FLOOR_PERF from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_CLASS1_INITIAL_PERF from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_THREAD_SCHEDULING_POLICY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_SHORT_THREAD_SCHEDULING_POLICY from AdapterCommon.obj
1>    Discarded GUID_SYSTEM_COOLING_POLICY from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_RESPONSIVENESS_DISABLE_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_RESPONSIVENESS_DISABLE_THRESHOLD_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_RESPONSIVENESS_ENABLE_THRESHOLD from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_RESPONSIVENESS_ENABLE_THRESHOLD_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_RESPONSIVENESS_DISABLE_TIME from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_RESPONSIVENESS_DISABLE_TIME_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_RESPONSIVENESS_ENABLE_TIME from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_RESPONSIVENESS_ENABLE_TIME_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_RESPONSIVENESS_EPP_CEILING from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_RESPONSIVENESS_EPP_CEILING_1 from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_RESPONSIVENESS_PERF_FLOOR from AdapterCommon.obj
1>    Discarded GUID_PROCESSOR_RESPONSIVENESS_PERF_FLOOR_1 from AdapterCommon.obj
1>    Discarded GUID_LOCK_CONSOLE_ON_WAKE from AdapterCommon.obj
1>    Discarded GUID_DEVICE_IDLE_POLICY from AdapterCommon.obj
1>    Discarded GUID_CONNECTIVITY_IN_STANDBY from AdapterCommon.obj
1>    Discarded GUID_DISCONNECTED_STANDBY_MODE from AdapterCommon.obj
1>    Discarded GUID_ACDC_POWER_SOURCE from AdapterCommon.obj
1>    Discarded GUID_LIDSWITCH_STATE_CHANGE from AdapterCommon.obj
1>    Discarded GUID_BATTERY_PERCENTAGE_REMAINING from AdapterCommon.obj
1>    Discarded GUID_BATTERY_COUNT from AdapterCommon.obj
1>    Discarded GUID_GLOBAL_USER_PRESENCE from AdapterCommon.obj
1>    Discarded GUID_SESSION_DISPLAY_STATUS from AdapterCommon.obj
1>    Discarded GUID_SESSION_USER_PRESENCE from AdapterCommon.obj
1>    Discarded GUID_IDLE_BACKGROUND_TASK from AdapterCommon.obj
1>    Discarded GUID_BACKGROUND_TASK_NOTIFICATION from AdapterCommon.obj
1>    Discarded GUID_APPLAUNCH_BUTTON from AdapterCommon.obj
1>    Discarded GUID_PCIEXPRESS_SETTINGS_SUBGROUP from AdapterCommon.obj
1>    Discarded GUID_PCIEXPRESS_ASPM_POLICY from AdapterCommon.obj
1>    Discarded GUID_ENABLE_SWITCH_FORCED_SHUTDOWN from AdapterCommon.obj
1>    Discarded GUID_INTSTEER_SUBGROUP from AdapterCommon.obj
1>    Discarded GUID_INTSTEER_MODE from AdapterCommon.obj
1>    Discarded GUID_INTSTEER_LOAD_PER_PROC_TRIGGER from AdapterCommon.obj
1>    Discarded GUID_INTSTEER_TIME_UNPARK_TRIGGER from AdapterCommon.obj
1>    Discarded GUID_GRAPHICS_SUBGROUP from AdapterCommon.obj
1>    Discarded GUID_GPU_PREFERENCE_POLICY from AdapterCommon.obj
1>    Discarded GUID_MIXED_REALITY_MODE from AdapterCommon.obj
1>    Discarded GUID_SPR_ACTIVE_SESSION_CHANGE from AdapterCommon.obj
1>    Discarded _GUID_4d837fe0_c555_11d0_8a2b_00a0c9255ac1 from MinipairDescriptorFactory.obj
1>    Discarded WdfDumpGuid2 from WdfDriverEntry.lib(stub.obj)
1>    Discarded WdfDumpGuid from WdfDriverEntry.lib(stub.obj)
1>    Discarded GUID_WDF_LOADER_INTERFACE_DIAGNOSTIC from WdfDriverEntry.lib(stub.obj)
1>    Discarded GUID_WDF_LOADER_INTERFACE_STANDARD from WdfDriverEntry.lib(stub.obj)
1>    Discarded WdfTraceGuid from WdfDriverEntry.lib(stub.obj)
1>    Discarded GUID_WDF_LOADER_INTERFACE_CLASS_BIND from WdfDriverEntry.lib(stub.obj)
1>    Discarded $unwind$?PropertyHandler_BasicSupportPeakMeter2@KsHelper@@SAJPEAU_PCPROPERTY_REQUEST@@K@Z from KsHelper.obj
1>    Discarded $unwind$?PropertyHandler_BasicSupportMute@KsHelper@@SAJPEAU_PCPROPERTY_REQUEST@@K@Z from KsHelper.obj
1>    Discarded $unwind$?PropertyHandler_BasicSupportVolume@KsHelper@@SAJPEAU_PCPROPERTY_REQUEST@@K@Z from KsHelper.obj
1>    Discarded $unwind$?ValidatePropertyParams@KsHelper@@SAJPEAU_PCPROPERTY_REQUEST@@KK@Z from KsHelper.obj
1>    Discarded $unwind$?GetSystemPinId@MiniportWaveRT@@AEAAKXZ from MiniportWaveRT.obj
1>    Discarded $unwind$?GetAudioEngineSupportedDeviceFormats@MiniportWaveRT@@AEAAKPEAPEAUKSDATAFORMAT_WAVEFORMATEXTENSIBLE@@@Z from MiniportWaveRT.obj
1>    Discarded $unwind$?GetAudioModuleListCount@MiniportWaveRT@@AEAAKXZ from MiniportWaveRT.obj
1>    Discarded $unwind$?GetChannelVolume@MiniportWaveRTStream@@QEAAJIPEAJ@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>    Discarded $unwind$?SetLoopbackProtection@MiniportWaveRTStream@@QEAAJW4CONSTRICTOR_OPTION@@@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>    Discarded $unwind$??_V@YAXPEAX@Z from NewDelete.obj
1>    Discarded $unwind$??_V@YAXPEAX_K@Z from NewDelete.obj
1>    Discarded $unwind$??2@YAPEAX_KW4_POOL_TYPE@@@Z from NewDelete.obj
1>    Discarded $unwind$??3@YAXPEAXK@Z from NewDelete.obj
1>    Discarded $unwind$?PutInternal@RingBuffer@@AEAAJPEAE_K@Z from RingBuffer.obj
1>    Discarded $unwind$??1RingBuffer@@QEAA@XZ from RingBuffer.obj
1>    Discarded $unwind$?GetAvailableBytes@RingBuffer@@QEAA_KXZ from RingBuffer.obj
1>    Discarded $unwind$??1SubdeviceHelper@@QEAA@XZ from SubdeviceHelper.obj
1>    Discarded $unwind$??3@YAXPEAX@Z from stdunk.lib(stdunk.obj)
1>    Discarded ExPoolZeroingNativelySupported from AdapterCommon.obj
1>    Discarded ExDefaultMdlProtection from WdfDriverEntry.lib(stub.obj)
1>    Discarded ExDefaultNonPagedPoolType from WdfDriverEntry.lib(stub.obj)
1>    Discarded $pdata$?PropertyHandler_BasicSupportPeakMeter2@KsHelper@@SAJPEAU_PCPROPERTY_REQUEST@@K@Z from KsHelper.obj
1>    Discarded $pdata$?PropertyHandler_BasicSupportMute@KsHelper@@SAJPEAU_PCPROPERTY_REQUEST@@K@Z from KsHelper.obj
1>    Discarded $pdata$?PropertyHandler_BasicSupportVolume@KsHelper@@SAJPEAU_PCPROPERTY_REQUEST@@K@Z from KsHelper.obj
1>    Discarded $pdata$?ValidatePropertyParams@KsHelper@@SAJPEAU_PCPROPERTY_REQUEST@@KK@Z from KsHelper.obj
1>    Discarded $pdata$?GetSystemPinId@MiniportWaveRT@@AEAAKXZ from MiniportWaveRT.obj
1>    Discarded $pdata$?GetAudioEngineSupportedDeviceFormats@MiniportWaveRT@@AEAAKPEAPEAUKSDATAFORMAT_WAVEFORMATEXTENSIBLE@@@Z from MiniportWaveRT.obj
1>    Discarded $pdata$?GetAudioModuleListCount@MiniportWaveRT@@AEAAKXZ from MiniportWaveRT.obj
1>    Discarded $pdata$?GetChannelVolume@MiniportWaveRTStream@@QEAAJIPEAJ@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>    Discarded $pdata$?SetLoopbackProtection@MiniportWaveRTStream@@QEAAJW4CONSTRICTOR_OPTION@@@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>    Discarded $pdata$??_V@YAXPEAX@Z from NewDelete.obj
1>    Discarded $pdata$??_V@YAXPEAX_K@Z from NewDelete.obj
1>    Discarded $pdata$??2@YAPEAX_KW4_POOL_TYPE@@@Z from NewDelete.obj
1>    Discarded $pdata$??3@YAXPEAXK@Z from NewDelete.obj
1>    Discarded $pdata$?PutInternal@RingBuffer@@AEAAJPEAE_K@Z from RingBuffer.obj
1>    Discarded $pdata$??1RingBuffer@@QEAA@XZ from RingBuffer.obj
1>    Discarded $pdata$?GetAvailableBytes@RingBuffer@@QEAA_KXZ from RingBuffer.obj
1>    Discarded $pdata$??1SubdeviceHelper@@QEAA@XZ from SubdeviceHelper.obj
1>    Discarded $pdata$??3@YAXPEAX@Z from stdunk.lib(stdunk.obj)
1>    Discarded "private: __cdecl KsHelper::KsHelper(void)" (??0KsHelper@@AEAA@XZ) from KsHelper.obj
1>    Discarded "private: __cdecl KsHelper::~KsHelper(void)" (??1KsHelper@@AEAA@XZ) from KsHelper.obj
1>    Discarded "private: __cdecl MinipairDescriptorFactory::MinipairDescriptorFactory(void)" (??0MinipairDescriptorFactory@@AEAA@XZ) from MinipairDescriptorFactory.obj
1>    Discarded "private: __cdecl MinipairDescriptorFactory::~MinipairDescriptorFactory(void)" (??1MinipairDescriptorFactory@@AEAA@XZ) from MinipairDescriptorFactory.obj
1>    Discarded "void * __cdecl operator new(unsigned __int64,enum _POOL_TYPE)" (??2@YAPEAX_KW4_POOL_TYPE@@@Z) from NewDelete.obj
1>    Discarded "void __cdecl operator delete(void *,unsigned long)" (??3@YAXPEAXK@Z) from NewDelete.obj
1>    Discarded "void __cdecl operator delete[](void *)" (??_V@YAXPEAX@Z) from NewDelete.obj
1>    Discarded "void __cdecl operator delete[](void *,unsigned __int64)" (??_V@YAXPEAX_K@Z) from NewDelete.obj
1>    Discarded "private: __cdecl RegistryHelper::RegistryHelper(void)" (??0RegistryHelper@@AEAA@XZ) from RegistryHelper.obj
1>    Discarded "private: __cdecl RegistryHelper::~RegistryHelper(void)" (??1RegistryHelper@@AEAA@XZ) from RegistryHelper.obj
1>    Discarded "public: __cdecl RingBuffer::~RingBuffer(void)" (??1RingBuffer@@QEAA@XZ) from RingBuffer.obj
1>    Discarded "public: unsigned __int64 __cdecl RingBuffer::GetAvailableBytes(void)" (?GetAvailableBytes@RingBuffer@@QEAA_KXZ) from RingBuffer.obj
1>    Discarded "private: long __cdecl RingBuffer::PutInternal(unsigned char *,unsigned __int64)" (?PutInternal@RingBuffer@@AEAAJPEAE_K@Z) from RingBuffer.obj
1>    Discarded "public: __cdecl SubdeviceCache::~SubdeviceCache(void)" (??1SubdeviceCache@@QEAA@XZ) from SubdeviceCache.obj
1>    Discarded "public: __cdecl SubdeviceHelper::~SubdeviceHelper(void)" (??1SubdeviceHelper@@QEAA@XZ) from SubdeviceHelper.obj
1>    Discarded PcGetPhysicalDeviceObject from portcls.lib(portcls.sys)
1>    Discarded PcInitializeAdapterDriver from portcls.lib(portcls.sys)
1>    Discarded PcDispatchIrp from portcls.lib(portcls.sys)
1>    Discarded PcAddAdapterDevice from portcls.lib(portcls.sys)
1>    Discarded PcRegisterSubdevice from portcls.lib(portcls.sys)
1>    Discarded PcRegisterPhysicalConnection from portcls.lib(portcls.sys)
1>    Discarded PcNewPort from portcls.lib(portcls.sys)
1>    Discarded PcNewMiniport from portcls.lib(portcls.sys)
1>    Discarded "public: __cdecl INonDelegatingUnknown::INonDelegatingUnknown(void)" (??0INonDelegatingUnknown@@QEAA@XZ) from stdunk.lib(stdunk.obj)
1>    Discarded "void __cdecl operator delete(void *)" (??3@YAXPEAX@Z) from stdunk.lib(stdunk.obj)
1>    Discarded ReadNoFence64 from libcntpr.lib(guard_support.obj)
1>    Discarded ReadPointerNoFence from libcntpr.lib(guard_support.obj)
1>    Discarded _guard_icall_checks_enforced from libcntpr.lib(guard_support.obj)
1>    Discarded _guard_rf_checks_enforced from libcntpr.lib(guard_support.obj)
1>    Discarded __report_rangecheckfailure from BufferOverflowFastFailK.lib(gs_report.obj)
1>    Discarded __report_securityfailure from BufferOverflowFastFailK.lib(gs_report.obj)
1>    Discarded RtlAssert from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded ExFreePoolWithTag from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded DbgPrintEx from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded KeInitializeEvent from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded ExAllocatePoolWithTag from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded ExAcquireFastMutex from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded ExReleaseFastMutex from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded KeFlushQueuedDpcs from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded KeSetEvent from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded KeInitializeSpinLock from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded KeAcquireSpinLockRaiseToDpc from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded KeReleaseSpinLock from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded ExAllocateTimer from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded ExSetTimer from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded ExCancelTimer from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded ExDeleteTimer from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded RtlInitUnicodeString from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded ZwClose from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded ZwCreateKey from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded ZwOpenKey from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded ZwEnumerateKey from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded ZwEnumerateValueKey from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded ZwSetValueKey from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded RtlFreeUnicodeString from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded IoRegisterDeviceInterface from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded IoOpenDeviceInterfaceRegistryKey from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded IoSetDeviceInterfacePropertyData from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded ExFreePool from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded KeQueryPerformanceCounter from hal.lib(HAL.dll)
1>    Discarded RtlCopyUnicodeString from ntoskrnl.lib(ntoskrnl.exe)
1>    Discarded "public: static long __cdecl KsHelper::PropertyHandler_BasicSupportMute(struct _PCPROPERTY_REQUEST *,unsigned long)" (?PropertyHandler_BasicSupportMute@KsHelper@@SAJPEAU_PCPROPERTY_REQUEST@@K@Z) from KsHelper.obj
1>    Discarded "public: static long __cdecl KsHelper::PropertyHandler_BasicSupportPeakMeter2(struct _PCPROPERTY_REQUEST *,unsigned long)" (?PropertyHandler_BasicSupportPeakMeter2@KsHelper@@SAJPEAU_PCPROPERTY_REQUEST@@K@Z) from KsHelper.obj
1>    Discarded "public: static long __cdecl KsHelper::PropertyHandler_BasicSupportVolume(struct _PCPROPERTY_REQUEST *,unsigned long)" (?PropertyHandler_BasicSupportVolume@KsHelper@@SAJPEAU_PCPROPERTY_REQUEST@@K@Z) from KsHelper.obj
1>    Discarded "public: static long __cdecl KsHelper::ValidatePropertyParams(struct _PCPROPERTY_REQUEST *,unsigned long,unsigned long)" (?ValidatePropertyParams@KsHelper@@SAJPEAU_PCPROPERTY_REQUEST@@KK@Z) from KsHelper.obj
1>    Discarded "private: unsigned long __cdecl MiniportWaveRT::GetAudioEngineSupportedDeviceFormats(struct KSDATAFORMAT_WAVEFORMATEXTENSIBLE * *)" (?GetAudioEngineSupportedDeviceFormats@MiniportWaveRT@@AEAAKPEAPEAUKSDATAFORMAT_WAVEFORMATEXTENSIBLE@@@Z) from MiniportWaveRT.obj
1>    Discarded "private: unsigned long __cdecl MiniportWaveRT::GetAudioModuleDescriptorListCount(void)" (?GetAudioModuleDescriptorListCount@MiniportWaveRT@@AEAAKXZ) from MiniportWaveRT.obj
1>    Discarded "private: unsigned long __cdecl MiniportWaveRT::GetAudioModuleListCount(void)" (?GetAudioModuleListCount@MiniportWaveRT@@AEAAKXZ) from MiniportWaveRT.obj
1>    Discarded "private: struct _GUID const * __cdecl MiniportWaveRT::GetAudioModuleNotificationDeviceId(void)" (?GetAudioModuleNotificationDeviceId@MiniportWaveRT@@AEAAPEBU_GUID@@XZ) from MiniportWaveRT.obj
1>    Discarded "private: class MiniportWaveRTStream * __cdecl MiniportWaveRT::GetStream(void)" (?GetStream@MiniportWaveRT@@AEAAPEAVMiniportWaveRTStream@@XZ) from MiniportWaveRT.obj
1>    Discarded "private: unsigned long __cdecl MiniportWaveRT::GetSystemPinId(void)" (?GetSystemPinId@MiniportWaveRT@@AEAAKXZ) from MiniportWaveRT.obj
1>    Discarded "public: long __cdecl MiniportWaveRTStream::GetChannelVolume(unsigned int,long *)" (?GetChannelVolume@MiniportWaveRTStream@@QEAAJIPEAJ@Z) from MiniportWaveRTStreamAudioEngineNode.obj
1>    Discarded "public: long __cdecl MiniportWaveRTStream::SetLoopbackProtection(enum CONSTRICTOR_OPTION)" (?SetLoopbackProtection@MiniportWaveRTStream@@QEAAJW4CONSTRICTOR_OPTION@@@Z) from MiniportWaveRTStreamAudioEngineNode.obj
1>    Discarded " ?? ?? ::NNGAKEGL::`string'" (??_C@_0BA@JNNKNEEL@MaxChannels?5?$DO?50@NNGAKEGL@) from KsHelper.obj
1>    Discarded " ?? ?? ::NNGAKEGL::`string'" (??_C@_0BB@MFBFHHGJ@IsRenderDevice?$CI?$CJ@NNGAKEGL@) from MiniportWaveRT.obj
1>    Discarded " ?? ?? ::NNGAKEGL::`string'" (??_C@_0CB@GINHJDGB@m_DeviceFormatsAndModesCount?5?$DO?5@NNGAKEGL@) from MiniportWaveRT.obj
1>    Discarded " ?? ?? ::NNGAKEGL::`string'" (??_C@_0DE@BIPBDOKL@pDeviceFormatsAndModes?$FLi?$FN?4PinTy@NNGAKEGL@) from MiniportWaveRT.obj
1>    Discarded " ?? ?? ::NNGAKEGL::`string'" (??_C@_0CO@FNMEOCLD@pDeviceFormatsAndModes?$FLi?$FN?4WaveF@NNGAKEGL@) from MiniportWaveRT.obj
1>    Discarded " ?? ?? ::NNGAKEGL::`string'" (??_C@_0CP@FLJHLBJK@pDeviceFormatsAndModes?$FLi?$FN?4WaveF@NNGAKEGL@) from MiniportWaveRT.obj
1>    Discarded " ?? ?? ::NNGAKEGL::`string'" (??_C@_08PJEMJIBH@_pVolume@NNGAKEGL@) from MiniportWaveRTStreamAudioEngineNode.obj
1>
1>    Selected symbol:
1>        "public: virtual struct _DEVICE_OBJECT * __cdecl AdapterCommon::GetDeviceObject(void)" (?GetDeviceObject@AdapterCommon@@UEAAPEAU_DEVICE_OBJECT@@XZ) from AdapterCommon.obj
1>    Replaced symbol(s):
1>        "public: unsigned __int64 __cdecl RingBuffer::GetSize(void)" (?GetSize@RingBuffer@@QEAA_KXZ) from RingBuffer.obj
1>
1>    Selected symbol:
1>        "long __cdecl RtlStringValidateDestW(unsigned short const *,unsigned __int64,unsigned __int64)" (?RtlStringValidateDestW@@YAJPEBG_K_K@Z) from RegistryHelper.obj
1>    Replaced symbol(s):
1>        "long __cdecl RtlStringValidateDestW(unsigned short const *,unsigned __int64,unsigned __int64)" (?RtlStringValidateDestW@@YAJPEBG_K_K@Z) from SubdeviceCache.obj
1>
1>    Selected symbol:
1>        "long __cdecl RtlStringCopyWorkerW(unsigned short *,unsigned __int64,unsigned __int64 *,unsigned short const *,unsigned __int64)" (?RtlStringCopyWorkerW@@YAJPEAG_KPEA_KPEBG1@Z) from RegistryHelper.obj
1>    Replaced symbol(s):
1>        "long __cdecl RtlStringCopyWorkerW(unsigned short *,unsigned __int64,unsigned __int64 *,unsigned short const *,unsigned __int64)" (?RtlStringCopyWorkerW@@YAJPEAG_KPEA_KPEBG1@Z) from SubdeviceCache.obj
1>
1>    Selected symbol:
1>        "public: __cdecl IAdapterCommon::IAdapterCommon(void)" (??0IAdapterCommon@@QEAA@XZ) from AdapterCommon.obj
1>    Replaced symbol(s):
1>        "public: __cdecl IMiniport::IMiniport(void)" (??0IMiniport@@QEAA@XZ) from MiniportTopology.obj
1>        "public: __cdecl IMiniportStreamAudioEngineNode2::IMiniportStreamAudioEngineNode2(void)" (??0IMiniportStreamAudioEngineNode2@@QEAA@XZ) from MiniportWaveRT.obj
1>        "public: __cdecl IMiniportStreamAudioEngineNode::IMiniportStreamAudioEngineNode(void)" (??0IMiniportStreamAudioEngineNode@@QEAA@XZ) from MiniportWaveRT.obj
1>        "public: __cdecl IMiniportWaveRTInputStream::IMiniportWaveRTInputStream(void)" (??0IMiniportWaveRTInputStream@@QEAA@XZ) from MiniportWaveRT.obj
1>        "public: __cdecl IMiniportWaveRTOutputStream::IMiniportWaveRTOutputStream(void)" (??0IMiniportWaveRTOutputStream@@QEAA@XZ) from MiniportWaveRT.obj
1>        "public: __cdecl IMiniportWaveRTStream::IMiniportWaveRTStream(void)" (??0IMiniportWaveRTStream@@QEAA@XZ) from MiniportWaveRT.obj
1>
1>    Selected symbol:
1>        "public: __cdecl IMiniportTopology::IMiniportTopology(void)" (??0IMiniportTopology@@QEAA@XZ) from MiniportTopology.obj
1>    Replaced symbol(s):
1>        "public: __cdecl IMiniportWaveRT::IMiniportWaveRT(void)" (??0IMiniportWaveRT@@QEAA@XZ) from MiniportWaveRT.obj
1>        "public: __cdecl IMiniportWaveRTStreamNotification::IMiniportWaveRTStreamNotification(void)" (??0IMiniportWaveRTStreamNotification@@QEAA@XZ) from MiniportWaveRT.obj
1>
1>    Selected symbol:
1>        "public: virtual unsigned long __cdecl AdapterCommon::Release(void)" (?Release@AdapterCommon@@UEAAKXZ) from AdapterCommon.obj
1>    Replaced symbol(s):
1>        "public: virtual unsigned long __cdecl MiniportTopology::Release(void)" (?Release@MiniportTopology@@UEAAKXZ) from MiniportTopology.obj
1>        "public: virtual unsigned long __cdecl MiniportWaveRT::Release(void)" (?Release@MiniportWaveRT@@UEAAKXZ) from MiniportWaveRT.obj
1>
1>    Selected symbol:
1>        "public: virtual unsigned long __cdecl AdapterCommon::AddRef(void)" (?AddRef@AdapterCommon@@UEAAKXZ) from AdapterCommon.obj
1>    Replaced symbol(s):
1>        "public: virtual unsigned long __cdecl MiniportTopology::AddRef(void)" (?AddRef@MiniportTopology@@UEAAKXZ) from MiniportTopology.obj
1>        "public: virtual unsigned long __cdecl MiniportWaveRT::AddRef(void)" (?AddRef@MiniportWaveRT@@UEAAKXZ) from MiniportWaveRT.obj
1>
1>    Selected symbol:
1>        "public: virtual long __cdecl AdapterCommon::QueryInterface(struct _GUID const &,void * *)" (?QueryInterface@AdapterCommon@@UEAAJAEBU_GUID@@PEAPEAX@Z) from AdapterCommon.obj
1>    Replaced symbol(s):
1>        "public: virtual long __cdecl MiniportTopology::QueryInterface(struct _GUID const &,void * *)" (?QueryInterface@MiniportTopology@@UEAAJAEBU_GUID@@PEAPEAX@Z) from MiniportTopology.obj
1>        "public: virtual long __cdecl MiniportWaveRT::QueryInterface(struct _GUID const &,void * *)" (?QueryInterface@MiniportWaveRT@@UEAAJAEBU_GUID@@PEAPEAX@Z) from MiniportWaveRT.obj
1>
1>    Selected symbol:
1>        "public: virtual long __cdecl MiniportWaveRTStream::GetClockRegister(struct KSRTAUDIO_HWREGISTER *)" (?GetClockRegister@MiniportWaveRTStream@@UEAAJPEAUKSRTAUDIO_HWREGISTER@@@Z) from MiniportWaveRTStream.obj
1>    Replaced symbol(s):
1>        "public: virtual long __cdecl MiniportWaveRTStream::GetPositionRegister(struct KSRTAUDIO_HWREGISTER *)" (?GetPositionRegister@MiniportWaveRTStream@@UEAAJPEAUKSRTAUDIO_HWREGISTER@@@Z) from MiniportWaveRTStream.obj
1>
1>    Selected symbol:
1>        "public: virtual void __cdecl MiniportWaveRTStream::FreeAudioBuffer(struct _MDL *,unsigned long)" (?FreeAudioBuffer@MiniportWaveRTStream@@UEAAXPEAU_MDL@@K@Z) from MiniportWaveRTStream.obj
1>    Replaced symbol(s):
1>        "public: virtual void __cdecl MiniportWaveRTStream::FreeBufferWithNotification(struct _MDL *,unsigned long)" (?FreeBufferWithNotification@MiniportWaveRTStream@@UEAAXPEAU_MDL@@K@Z) from MiniportWaveRTStream.obj
1>
1>    Selected symbol:
1>        $unwind$?Init@AdapterCommon@@UEAAJPEAU_IRP@@PEAU_DEVICE_OBJECT@@@Z from AdapterCommon.obj
1>    Replaced symbol(s):
1>        $unwind$?FreeAudioBuffer@MiniportWaveRTStream@@UEAAXPEAU_MDL@@K@Z from MiniportWaveRTStream.obj
1>        $unwind$?FreeBufferWithNotification@MiniportWaveRTStream@@UEAAXPEAU_MDL@@K@Z from MiniportWaveRTStream.obj
1>        $unwind$?RtlStringCchCopyW@@YAJPEAG_KPEBG@Z from SubdeviceCache.obj
1>
1>    Selected symbol:
1>        $unwind$?Init@MiniportWaveRT@@UEAAJPEAUIUnknown@@PEAUIResourceList@@PEAUIPortWaveRT@@@Z from MiniportWaveRT.obj
1>    Replaced symbol(s):
1>        $unwind$?CreateAudioInterfaceWithProperties@SubdeviceHelper@@AEAAJPEBG0KPEBU_SYSVAD_DEVPROPERTY@@PEAU_DEVICE_OBJECT@@PEAU_UNICODE_STRING@@@Z from SubdeviceHelper.obj
1>
1>    Selected symbol:
1>        $unwind$?WriteEtwEvent@AdapterCommon@@UEAAJW4EPcMiniportEngineEvent@@_K111@Z from AdapterCommon.obj
1>    Replaced symbol(s):
1>        $unwind$?IsFormatSupported@MiniportWaveRT@@AEAAJKEPEATKSDATAFORMAT@@@Z from MiniportWaveRT.obj
1>        $unwind$?AllocateAudioBuffer@MiniportWaveRTStream@@UEAAJKPEAPEAU_MDL@@PEAK1PEAW4_MEMORY_CACHING_TYPE@@@Z from MiniportWaveRTStream.obj
1>        $unwind$?SetWritePacket@MiniportWaveRTStream@@UEAAJKKK@Z from MiniportWaveRTStream.obj
1>
1>    Selected symbol:
1>        $unwind$?ValidateStreamCreate@MiniportWaveRT@@AEAAJKE@Z from MiniportWaveRT.obj
1>    Replaced symbol(s):
1>        $unwind$?GetStreamChannelCount@MiniportWaveRTStream@@UEAAJW4eChannelTargetType@@PEAI@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?GetStreamChannelVolume@MiniportWaveRTStream@@UEAAJIPEAJ@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?GetStreamChannelMute@MiniportWaveRTStream@@UEAAJIPEAH@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?SetStreamChannelMute@MiniportWaveRTStream@@UEAAJIH@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?GetStreamChannelPeakMeter@MiniportWaveRTStream@@UEAAJIPEAJ@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?SetChannelVolume@MiniportWaveRTStream@@QEAAJIJ@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?GetChannelPeakMeter@MiniportWaveRTStream@@QEAAJIPEAJ@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?GetChannelMute@MiniportWaveRTStream@@QEAAJIPEAH@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?SetChannelMute@MiniportWaveRTStream@@QEAAJIH@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>
1>    Selected symbol:
1>        $unwind$?NonDelegatingQueryInterface@CUnknown@@UEAAJAEBU_GUID@@PEAPEAX@Z from stdunk.lib(stdunk.obj)
1>    Replaced symbol(s):
1>        $unwind$?NonDelegatingRelease@CUnknown@@UEAAKXZ from stdunk.lib(stdunk.obj)
1>        $unwind$__GSHandlerCheckCommon from libcntpr.lib(gshandler.obj)
1>        $unwind$__GSHandlerCheck from libcntpr.lib(gshandler.obj)
1>        $unwind$FxStubDriverMiniportUnload from WdfDriverEntry.lib(stub.obj)
1>        $unwind$FxStubDriverUnload from WdfDriverEntry.lib(stub.obj)
1>        $unwind$?FxStubDriverUnloadCommon@@YAXXZ from WdfDriverEntry.lib(stub.obj)
1>
1>    Selected symbol:
1>        $unwind$?DataRangeIntersection@MiniportTopology@@UEAAJKPEATKSDATAFORMAT@@0KPEAXPEAK@Z from MiniportTopology.obj
1>    Replaced symbol(s):
1>        $unwind$?DataRangeIntersection@MiniportWaveRT@@UEAAJKPEATKSDATAFORMAT@@0KPEAXPEAK@Z from MiniportWaveRT.obj
1>        $unwind$?GetStreamAttributeSteppings@MiniportWaveRTStream@@UEAAJW4eChannelTargetType@@PEAUKSPROPERTY_STEPPING_LONG@@I@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>
1>    Selected symbol:
1>        $unwind$??_GAdapterCommon@@UEAAPEAXI@Z from AdapterCommon.obj
1>    Replaced symbol(s):
1>        $unwind$??_GMiniportTopology@@UEAAPEAXI@Z from MiniportTopology.obj
1>        $unwind$??_GMiniportWaveRTStream@@UEAAPEAXI@Z from MiniportWaveRT.obj
1>        $unwind$??_GMiniportWaveRT@@UEAAPEAXI@Z from MiniportWaveRT.obj
1>
1>    Selected symbol:
1>        $unwind$??0IAdapterCommon@@QEAA@XZ from AdapterCommon.obj
1>    Replaced symbol(s):
1>        $unwind$??0IMiniport@@QEAA@XZ from MiniportTopology.obj
1>        $unwind$??0IMiniportTopology@@QEAA@XZ from MiniportTopology.obj
1>        $unwind$ExInitializeFastMutex from MiniportWaveRT.obj
1>        $unwind$??0IMiniportWaveRTStream@@QEAA@XZ from MiniportWaveRT.obj
1>        $unwind$??0IMiniportWaveRTStreamNotification@@QEAA@XZ from MiniportWaveRT.obj
1>        $unwind$??0IMiniportWaveRTInputStream@@QEAA@XZ from MiniportWaveRT.obj
1>        $unwind$??0IMiniportWaveRTOutputStream@@QEAA@XZ from MiniportWaveRT.obj
1>        $unwind$??0IMiniportWaveRT@@QEAA@XZ from MiniportWaveRT.obj
1>        $unwind$??0IMiniportStreamAudioEngineNode@@QEAA@XZ from MiniportWaveRT.obj
1>        $unwind$??0IMiniportStreamAudioEngineNode2@@QEAA@XZ from MiniportWaveRT.obj
1>        $unwind$RtlpCheckListEntry from MiniportWaveRTStream.obj
1>        $unwind$??0SubdeviceCache@@QEAA@XZ from SubdeviceCache.obj
1>        $unwind$?Clean@SubdeviceHelper@@QEAAXXZ from SubdeviceHelper.obj
1>
1>    Selected symbol:
1>        $unwind$?InstallVirtualCable@AdapterCommon@@AEAAJPEAU_IRP@@@Z from AdapterCommon.obj
1>    Replaced symbol(s):
1>        $unwind$DriverEntry from Driver.obj
1>
1>    Selected symbol:
1>        $unwind$?GetPinSupportedDeviceFormats@MiniportWaveRT@@AEAAKKPEAPEAUKSDATAFORMAT_WAVEFORMATEXTENSIBLE@@@Z from MiniportWaveRT.obj
1>    Replaced symbol(s):
1>        $unwind$?GetPinSupportedDeviceModes@MiniportWaveRT@@AEAAKKPEAPEAU_MODE_AND_DEFAULT_FORMAT@@@Z from MiniportWaveRT.obj
1>        $unwind$?StreamClosed@MiniportWaveRT@@QEAAJKPEAVMiniportWaveRTStream@@@Z from MiniportWaveRT.obj
1>        $unwind$?StreamCreated@MiniportWaveRT@@QEAAJKPEAVMiniportWaveRTStream@@@Z from MiniportWaveRT.obj
1>
1>    Selected symbol:
1>        $unwind$?AddRef@AdapterCommon@@UEAAKXZ from AdapterCommon.obj
1>    Replaced symbol(s):
1>        $unwind$?Release@AdapterCommon@@UEAAKXZ from AdapterCommon.obj
1>        $unwind$??1AdapterCommon@@UEAA@XZ from AdapterCommon.obj
1>        $unwind$?Cleanup@AdapterCommon@@UEAAXXZ from AdapterCommon.obj
1>        $unwind$WdfDriverMiniportUnload from Driver.obj
1>        $unwind$DriverUnload from Driver.obj
1>        $unwind$?AddRef@MiniportTopology@@UEAAKXZ from MiniportTopology.obj
1>        $unwind$?Release@MiniportTopology@@UEAAKXZ from MiniportTopology.obj
1>        $unwind$??1MiniportTopology@@UEAA@XZ from MiniportTopology.obj
1>        $unwind$?AddRef@MiniportWaveRTStream@@UEAAKXZ from MiniportWaveRT.obj
1>        $unwind$?Release@MiniportWaveRTStream@@UEAAKXZ from MiniportWaveRT.obj
1>        $unwind$?AddRef@MiniportWaveRT@@UEAAKXZ from MiniportWaveRT.obj
1>        $unwind$?Release@MiniportWaveRT@@UEAAKXZ from MiniportWaveRT.obj
1>        $unwind$??1MiniportWaveRT@@UEAA@XZ from MiniportWaveRT.obj
1>        $unwind$??1MiniportWaveRTStream@@UEAA@XZ from MiniportWaveRTStream.obj
1>        $unwind$RemoveHeadList from SubdeviceCache.obj
1>
1>    Selected symbol:
1>        $unwind$?InstallVirtualMic@AdapterCommon@@AEAAJPEAU_IRP@@PEAPEAUIUnknown@@@Z from AdapterCommon.obj
1>    Replaced symbol(s):
1>        $unwind$?InstallVirtualSpeaker@AdapterCommon@@AEAAJPEAU_IRP@@PEAPEAUIUnknown@@@Z from AdapterCommon.obj
1>        $unwind$?NonDelegatingQueryInterface@MiniportWaveRTStream@@UEAAJAEBU_GUID@@PEAPEAX@Z from MiniportWaveRTStream.obj
1>
1>    Selected symbol:
1>        $unwind$?GetPinTypeForPinNum@MiniportWaveRT@@AEAA?AW4PinType@@K@Z from MiniportWaveRT.obj
1>    Replaced symbol(s):
1>        $unwind$?IsSystemRenderPin@MiniportWaveRT@@QEAAHK@Z from MiniportWaveRT.obj
1>        $unwind$?IsSystemCapturePin@MiniportWaveRT@@QEAAHK@Z from MiniportWaveRT.obj
1>        $unwind$?IsBridgePin@MiniportWaveRT@@QEAAHK@Z from MiniportWaveRT.obj
1>        $unwind$?SetLfxState@MiniportWaveRTStream@@UEAAJH@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?SetStreamCurrentWritePosition@MiniportWaveRTStream@@UEAAJK@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?SetStreamLoopbackProtection@MiniportWaveRTStream@@UEAAJW4CONSTRICTOR_OPTION@@@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?SetStreamCurrentWritePositionForLastBuffer@MiniportWaveRTStream@@UEAAJK@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?SetCurrentWritePosition@MiniportWaveRTStream@@QEAAJK@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>
1>    Selected symbol:
1>        $unwind$?RtlStringCopyWorkerW@@YAJPEAG_KPEA_KPEBG1@Z from RegistryHelper.obj
1>    Replaced symbol(s):
1>        $unwind$?RtlStringCopyWorkerW@@YAJPEAG_KPEA_KPEBG1@Z from SubdeviceCache.obj
1>
1>    Selected symbol:
1>        $unwind$IoGetCurrentIrpStackLocation from Driver.obj
1>    Replaced symbol(s):
1>        $unwind$?IsRenderDevice@MiniportWaveRT@@AEAAHXZ from MiniportWaveRT.obj
1>        $unwind$IsListEmpty from MiniportWaveRTStream.obj
1>        $unwind$?IsCurrentWaveRTWritePositionUpdated@MiniportWaveRTStream@@QEAAHXZ from MiniportWaveRTStream.obj
1>
1>    Selected symbol:
1>        $unwind$?Create@AdapterCommon@@SAJPEAPEAUIUnknown@@AEBU_GUID@@PEAU2@W4_POOL_TYPE@@PEAU_DEVICE_OBJECT@@PEAU_IRP@@@Z from AdapterCommon.obj
1>    Replaced symbol(s):
1>        $unwind$?Create@MiniportTopology@@SAJPEAPEAUIUnknown@@AEBU_GUID@@PEAU2@W4_POOL_TYPE@@2PEAXPEAU_ENDPOINT_MINIPAIR@@@Z from MiniportTopology.obj
1>        $unwind$?MigrateDeviceInterfaceTemplateParameters@SubdeviceHelper@@AEAAJPEAU_UNICODE_STRING@@PEAU_DEVICE_OBJECT@@PEBG@Z from SubdeviceHelper.obj
1>        $unwind$?SysvadIoSetDeviceInterfacePropertyDataMultiple@SubdeviceHelper@@AEAAJPEAU_UNICODE_STRING@@KPEBU_SYSVAD_DEVPROPERTY@@@Z from SubdeviceHelper.obj
1>
1>    Selected symbol:
1>        $unwind$?GetPresentationPosition@MiniportWaveRTStream@@QEAAJPEAUKSAUDIO_PRESENTATION_POSITION@@@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>    Replaced symbol(s):
1>        $unwind$?CopyRegistryValues@RegistryHelper@@SAJPEAX0@Z from RegistryHelper.obj
1>
1>    Selected symbol:
1>        $unwind$?NonDelegatingQueryInterface@AdapterCommon@@UEAAJAEBU_GUID@@PEAPEAX@Z from AdapterCommon.obj
1>    Replaced symbol(s):
1>        $unwind$?QueryInterface@AdapterCommon@@UEAAJAEBU_GUID@@PEAPEAX@Z from AdapterCommon.obj
1>        $unwind$?NonDelegatingQueryInterface@MiniportTopology@@UEAAJAEBU_GUID@@PEAPEAX@Z from MiniportTopology.obj
1>        $unwind$?QueryInterface@MiniportTopology@@UEAAJAEBU_GUID@@PEAPEAX@Z from MiniportTopology.obj
1>        $unwind$?QueryInterface@MiniportWaveRTStream@@UEAAJAEBU_GUID@@PEAPEAX@Z from MiniportWaveRT.obj
1>        $unwind$?NonDelegatingQueryInterface@MiniportWaveRT@@UEAAJAEBU_GUID@@PEAPEAX@Z from MiniportWaveRT.obj
1>        $unwind$?QueryInterface@MiniportWaveRT@@UEAAJAEBU_GUID@@PEAPEAX@Z from MiniportWaveRT.obj
1>        $unwind$?GetVolumeSteppings@MiniportWaveRTStream@@QEAAJPEAUKSPROPERTY_STEPPING_LONG@@I@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?GetPeakMeterSteppings@MiniportWaveRTStream@@QEAAJPEAUKSPROPERTY_STEPPING_LONG@@I@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?GetMuteSteppings@MiniportWaveRTStream@@QEAAJPEAUKSPROPERTY_STEPPING_LONG@@I@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?Init@RingBuffer@@QEAAJ_K0@Z from RingBuffer.obj
1>
1>    Selected symbol:
1>        $unwind$?RtlStringValidateDestW@@YAJPEBG_K_K@Z from RegistryHelper.obj
1>    Replaced symbol(s):
1>        $unwind$?RtlStringValidateDestW@@YAJPEBG_K_K@Z from SubdeviceCache.obj
1>
1>    Selected symbol:
1>        $unwind$?Init@MiniportTopology@@UEAAJPEAUIUnknown@@PEAUIResourceList@@PEAUIPortTopology@@@Z from MiniportTopology.obj
1>    Replaced symbol(s):
1>        $unwind$?WriteAudioPacket@MiniportWaveRTStream@@AEAAJPEAEKH@Z from MiniportWaveRTStream.obj
1>
1>    Selected symbol:
1>        $unwind$WdfDriverCreate from Driver.obj
1>    Replaced symbol(s):
1>        $unwind$?Create@MiniportWaveRT@@SAJPEAPEAUIUnknown@@AEBU_GUID@@PEAU2@W4_POOL_TYPE@@2PEAXPEAU_ENDPOINT_MINIPAIR@@@Z from MiniportWaveRT.obj
1>        $unwind$?RtlStringCbCopyNW@@YAJPEAG_KPEBG1@Z from RegistryHelper.obj
1>        $unwind$?Get@SubdeviceCache@@QEAAJPEAGPEAPEAUIUnknown@@1@Z from SubdeviceCache.obj
1>
1>    Selected symbol:
1>        $unwind$?IsEqualGUID@@YAHAEBU_GUID@@0@Z from KsHelper.obj
1>    Replaced symbol(s):
1>        $unwind$??8@YA_NAEBU_GUID@@0@Z from KsHelper.obj
1>        $unwind$?GetDescription@MiniportTopology@@UEAAJPEAPEAUPCFILTER_DESCRIPTOR@@@Z from MiniportTopology.obj
1>        $unwind$?GetDescription@MiniportWaveRT@@UEAAJPEAPEAUPCFILTER_DESCRIPTOR@@@Z from MiniportWaveRT.obj
1>        $unwind$InsertTailList from MiniportWaveRTStream.obj
1>        $unwind$?SetFormat@MiniportWaveRTStream@@UEAAJPEATKSDATAFORMAT@@@Z from MiniportWaveRTStream.obj
1>        $unwind$?GetHWLatency@MiniportWaveRTStream@@UEAAXPEAUKSRTAUDIO_HWLATENCY@@@Z from MiniportWaveRTStream.obj
1>        $unwind$?GetPositionRegister@MiniportWaveRTStream@@UEAAJPEAUKSRTAUDIO_HWREGISTER@@@Z from MiniportWaveRTStream.obj
1>        $unwind$?GetClockRegister@MiniportWaveRTStream@@UEAAJPEAUKSRTAUDIO_HWREGISTER@@@Z from MiniportWaveRTStream.obj
1>        $unwind$?GetOutputStreamPresentationPosition@MiniportWaveRTStream@@UEAAJPEAUKSAUDIO_PRESENTATION_POSITION@@@Z from MiniportWaveRTStream.obj
1>        $unwind$?SetPairedStream@MiniportWaveRTStream@@QEAAXPEAV1@@Z from MiniportWaveRTStream.obj
1>        $unwind$?GetLfxState@MiniportWaveRTStream@@UEAAJPEAH@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?GetStreamPresentationPosition@MiniportWaveRTStream@@UEAAJPEAUKSAUDIO_PRESENTATION_POSITION@@@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?GetStreamLinearBufferPosition@MiniportWaveRTStream@@UEAAJPEA_K@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?GetVolumeChannelCount@MiniportWaveRTStream@@QEAAJPEAI@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?GetPeakMeterChannelCount@MiniportWaveRTStream@@QEAAJPEAI@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>        $unwind$?GetMuteChannelCount@MiniportWaveRTStream@@QEAAJPEAI@Z from MiniportWaveRTStreamAudioEngineNode.obj
1>
1>    Selected symbol:
1>        $unwind$?GetWaveFormatEx@KsHelper@@SAPEAUtWAVEFORMATEX@@PEATKSDATAFORMAT@@@Z from KsHelper.obj
1>    Replaced symbol(s):
1>        $unwind$RemoveEntryList from MiniportWaveRTStream.obj
1>
1>    Selected symbol:
1>        $unwind$?SetEtwHelper@AdapterCommon@@UEAAXPEAUIPortClsEtwHelper@@@Z from AdapterCommon.obj
1>    Replaced symbol(s):
1>        $unwind$?AddDevice@@YAJPEAU_DRIVER_OBJECT@@PEAU_DEVICE_OBJECT@@@Z from Driver.obj
1>        $unwind$?PropertyHandlerProposedFormat@MiniportWaveRT@@AEAAJPEAU_PCPROPERTY_REQUEST@@@Z from MiniportWaveRT.obj
1>        $unwind$?GetPosition@MiniportWaveRTStream@@UEAAJPEAUKSAUDIO_POSITION@@@Z from MiniportWaveRTStream.obj
1>        $unwind$?RegisterNotificationEvent@MiniportWaveRTStream@@UEAAJPEAU_KEVENT@@@Z from MiniportWaveRTStream.obj
1>        $unwind$?UnregisterNotificationEvent@MiniportWaveRTStream@@UEAAJPEAU_KEVENT@@@Z from MiniportWaveRTStream.obj
1>        $unwind$?GetPacketCount@MiniportWaveRTStream@@UEAAJPEAK@Z from MiniportWaveRTStream.obj
1>
1>    Selected symbol:
1>        $unwind$??0AdapterCommon@@QEAA@PEAUIUnknown@@@Z from AdapterCommon.obj
1>    Replaced symbol(s):
1>        $unwind$??0MiniportWaveRTStream@@QEAA@PEAUIUnknown@@@Z from MiniportWaveRT.obj
1>        $unwind$?SetPairedMiniport@MiniportWaveRT@@QEAAXPEAV1@@Z from MiniportWaveRT.obj
1>        $unwind$??3@YAXPEAX_K@Z from NewDelete.obj
1>        $unwind$??0SubdeviceHelper@@QEAA@PEAUIAdapterCommon@@@Z from SubdeviceHelper.obj
1>
1>    Selected symbol:
1>        $unwind$?CreateSpeaker@MinipairDescriptorFactory@@SAJPEAPEAU_ENDPOINT_MINIPAIR@@@Z from MinipairDescriptorFactory.obj
1>    Replaced symbol(s):
1>        $unwind$?CreateMicrophone@MinipairDescriptorFactory@@SAJPEAPEAU_ENDPOINT_MINIPAIR@@@Z from MinipairDescriptorFactory.obj
1>
1>    Selected symbol:
1>        $unwind$?GetAttributesFromAttributeList@KsHelper@@SAJPEBUKSMULTIPLE_ITEM@@_KPEAU_GUID@@@Z from KsHelper.obj
1>    Replaced symbol(s):
1>        $unwind$?Put@RingBuffer@@QEAAJPEAE_K@Z from RingBuffer.obj
1>
1>    Selected symbol:
1>        $unwind$?Init@MiniportWaveRTStream@@QEAAJPEAVMiniportWaveRT@@PEAUIPortWaveRTStream@@KEPEATKSDATAFORMAT@@U_GUID@@@Z from MiniportWaveRTStream.obj
1>    Replaced symbol(s):
1>        $unwind$?Take@RingBuffer@@QEAAJPEAE_KPEA_K@Z from RingBuffer.obj
1>
1>    Selected symbol:
1>        $pdata$?AddRef@AdapterCommon@@UEAAKXZ from AdapterCommon.obj
1>    Replaced symbol(s):
1>        $pdata$?AddRef@MiniportTopology@@UEAAKXZ from MiniportTopology.obj
1>        $pdata$?AddRef@MiniportWaveRT@@UEAAKXZ from MiniportWaveRT.obj
1>
1>    Selected symbol:
1>        $pdata$??0IMiniportTopology@@QEAA@XZ from MiniportTopology.obj
1>    Replaced symbol(s):
1>        $pdata$??0IMiniportWaveRTStreamNotification@@QEAA@XZ from MiniportWaveRT.obj
1>        $pdata$??0IMiniportWaveRT@@QEAA@XZ from MiniportWaveRT.obj
1>
1>    Selected symbol:
1>        $pdata$?QueryInterface@AdapterCommon@@UEAAJAEBU_GUID@@PEAPEAX@Z from AdapterCommon.obj
1>    Replaced symbol(s):
1>        $pdata$?QueryInterface@MiniportTopology@@UEAAJAEBU_GUID@@PEAPEAX@Z from MiniportTopology.obj
1>        $pdata$?QueryInterface@MiniportWaveRT@@UEAAJAEBU_GUID@@PEAPEAX@Z from MiniportWaveRT.obj
1>
1>    Selected symbol:
1>        $pdata$?FreeAudioBuffer@MiniportWaveRTStream@@UEAAXPEAU_MDL@@K@Z from MiniportWaveRTStream.obj
1>    Replaced symbol(s):
1>        $pdata$?FreeBufferWithNotification@MiniportWaveRTStream@@UEAAXPEAU_MDL@@K@Z from MiniportWaveRTStream.obj
1>
1>    Selected symbol:
1>        $pdata$?RtlStringCopyWorkerW@@YAJPEAG_KPEA_KPEBG1@Z from RegistryHelper.obj
1>    Replaced symbol(s):
1>        $pdata$?RtlStringCopyWorkerW@@YAJPEAG_KPEA_KPEBG1@Z from SubdeviceCache.obj
1>
1>    Selected symbol:
1>        $pdata$??0IAdapterCommon@@QEAA@XZ from AdapterCommon.obj
1>    Replaced symbol(s):
1>        $pdata$??0IMiniport@@QEAA@XZ from MiniportTopology.obj
1>        $pdata$??0IMiniportWaveRTStream@@QEAA@XZ from MiniportWaveRT.obj
1>        $pdata$??0IMiniportWaveRTInputStream@@QEAA@XZ from MiniportWaveRT.obj
1>        $pdata$??0IMiniportWaveRTOutputStream@@QEAA@XZ from MiniportWaveRT.obj
1>        $pdata$??0IMiniportStreamAudioEngineNode@@QEAA@XZ from MiniportWaveRT.obj
1>        $pdata$??0IMiniportStreamAudioEngineNode2@@QEAA@XZ from MiniportWaveRT.obj
1>
1>    Selected symbol:
1>        $pdata$?GetPositionRegister@MiniportWaveRTStream@@UEAAJPEAUKSRTAUDIO_HWREGISTER@@@Z from MiniportWaveRTStream.obj
1>    Replaced symbol(s):
1>        $pdata$?GetClockRegister@MiniportWaveRTStream@@UEAAJPEAUKSRTAUDIO_HWREGISTER@@@Z from MiniportWaveRTStream.obj
1>
1>    Selected symbol:
1>        $pdata$?Release@AdapterCommon@@UEAAKXZ from AdapterCommon.obj
1>    Replaced symbol(s):
1>        $pdata$?Release@MiniportTopology@@UEAAKXZ from MiniportTopology.obj
1>        $pdata$?Release@MiniportWaveRT@@UEAAKXZ from MiniportWaveRT.obj
1>
1>    Selected symbol:
1>        $pdata$?RtlStringValidateDestW@@YAJPEBG_K_K@Z from RegistryHelper.obj
1>    Replaced symbol(s):
1>        $pdata$?RtlStringValidateDestW@@YAJPEBG_K_K@Z from SubdeviceCache.obj
1>
1>    ICF total savings: 2977 bytes
1>
1>Starting pass 2
1>     SubdeviceHelper.obj
1>     SubdeviceCache.obj
1>     RingBuffer.obj
1>     RegistryHelper.obj
1>     NewDelete.obj
1>     MiniportWaveRTStreamAudioEngineNode.obj
1>     MiniportWaveRTStream.obj
1>     MiniportWaveRT.obj
1>     MiniportTopology.obj
1>     MinipairDescriptorFactory.obj
1>     KsHelper.obj
1>     Driver.obj
1>     AdapterCommon.obj
1>     portcls.lib(portcls.sys)
1>     portcls.lib(portcls.sys)
1>     portcls.lib(portcls.sys)
1>     portcls.lib(portcls.sys)
1>     portcls.lib(portcls.sys)
1>     portcls.lib(portcls.sys)
1>     portcls.lib(portcls.sys)
1>     portcls.lib(portcls.sys)
1>     portcls.lib(portcls.sys)
1>     portcls.lib(portcls.sys)
1>     portcls.lib(portcls.sys)
1>     stdunk.lib(stdunk.obj)
1>     libcntpr.lib(guard_dispatch.obj)
1>     libcntpr.lib(gshandler.obj)
1>     libcntpr.lib(guard_support.obj)
1>     libcntpr.lib(loadcfg.obj)
1>     libcntpr.lib(memcmp.obj)
1>     BufferOverflowFastFailK.lib(gs_report.obj)
1>     BufferOverflowFastFailK.lib(gs_support.obj)
1>     BufferOverflowFastFailK.lib(amdsecgs.obj)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     ntoskrnl.lib(ntoskrnl.exe)
1>     hal.lib(HAL.dll)
1>     hal.lib(HAL.dll)
1>     hal.lib(HAL.dll)
1>     WdfLdr.lib(WDFLDR.SYS)
1>     WdfLdr.lib(WDFLDR.SYS)
1>     WdfLdr.lib(WDFLDR.SYS)
1>     WdfLdr.lib(WDFLDR.SYS)
1>     WdfLdr.lib(WDFLDR.SYS)
1>     WdfLdr.lib(WDFLDR.SYS)
1>     WdfDriverEntry.lib(stub.obj)
1>     WdfDriverEntry.lib(classbind.obj)
1>     WdfDriverEntry.lib(inittypes.obj)
1>Finished pass 2
1>AudioMirror.vcxproj -> C:\Users\Elad\Desktop\AudioMirror\x64\Debug\AudioMirror.sys
1>Done Adding Additional Store
1>Successfully signed: C:\Users\Elad\Desktop\AudioMirror\x64\Debug\AudioMirror.sys
1>
1>Driver is 'Universal'.
1>........................
1>Signability test complete.
1>
1>Errors:
1>None
1>
1>Warnings:
1>None
1>
1>Catalog generation complete.
1>C:\Users\Elad\Desktop\AudioMirror\x64\Debug\AudioMirror\audiomirror.cat
1>Done Adding Additional Store
1>Successfully signed: C:\Users\Elad\Desktop\AudioMirror\x64\Debug\AudioMirror\audiomirror.cat
1>
1>Done building project "AudioMirror.vcxproj".
1>
1>Project Performance Summary:
1>        * ms  C:\Users\Elad\Desktop\AudioMirror\AudioMirror\AudioMirror.vcxproj   1 calls
1>        (* = timing was not recorded because of reentrancy)
1>
1>Target Performance Summary:
1>        0 ms  ComputeLinkImportLibraryOutputsForClean    1 calls
1>        0 ms  AfterResolveReferences                     1 calls
1>        0 ms  ImplicitlyExpandDesignTimeFacades          1 calls
1>        0 ms  ResolveReferences                          1 calls
1>        0 ms  ComputeCLCompileGeneratedSbrFiles          1 calls
1>        0 ms  BuildGenerateSourcesTraverse               1 calls
1>        0 ms  BeforeBuildGenerateSources                 1 calls
1>        0 ms  _BuildCompileAction                        1 calls
1>        0 ms  AfterBuildCompileEvent                     1 calls
1>        0 ms  PreBuildEvent                              1 calls
1>        0 ms  ResolveAssemblyReferences                  1 calls
1>        0 ms  GetCopyToOutputDirectoryXamlAppDefs        1 calls
1>        0 ms  SelectCustomBuild                          1 calls
1>        0 ms  _ResourceCompile                           1 calls
1>        0 ms  AfterResourceCompile                       1 calls
1>        0 ms  BeforeResourceCompile                      1 calls
1>        0 ms  _ClCompile                                 1 calls
1>        0 ms  _BscMake                                   1 calls
1>        0 ms  ComputeMIDLGeneratedCompileInputs          1 calls
1>        0 ms  AfterMidl                                  1 calls
1>        0 ms  AfterLink                                  1 calls
1>        0 ms  _SelectedFiles                             1 calls
1>        0 ms  CreateSatelliteAssemblies                  1 calls
1>        0 ms  BuildLinkTraverse                          1 calls
1>        0 ms  ResolveSDKReferences                       1 calls
1>        0 ms  SetLinkLibraryPathsForCX                   1 calls
1>        0 ms  _PrepareForBuild                           1 calls
1>        0 ms  _PrepareForReferenceResolution             1 calls
1>        0 ms  BeforeResolveReferences                    1 calls
1>        0 ms  CheckForCoinstallers                       1 calls
1>        0 ms  _ALink                                     1 calls
1>        0 ms  CreateCustomManifestResourceNames          1 calls
1>        0 ms  PrepareProjectReferences                   1 calls
1>        0 ms  ResolveProjectReferences                   1 calls
1>        0 ms  ComputeRCOutputs                           1 calls
1>        0 ms  GetFrameworkPaths                          1 calls
1>        0 ms  SetDriverVariables                         1 calls
1>        0 ms  ComputeManifestInputsTargets               1 calls
1>        0 ms  GetResolvedWinMD                           1 calls
1>        0 ms  _CheckWindowsSDKInstalled                  1 calls
1>        0 ms  ComputeCLGeneratedLinkInputs               1 calls
1>        0 ms  ComputeCLOutputs                           1 calls
1>        0 ms  BuildLink                                  1 calls
1>        0 ms  ComputeManifestGeneratedLinkerInputs       1 calls
1>        0 ms  ComputeRCGeneratedLinkInputs               1 calls
1>        0 ms  GetReferenceAssemblyPaths                  1 calls
1>        0 ms  BeforeClCompile                            1 calls
1>        0 ms  _Midl                                      1 calls
1>        0 ms  AfterClCompile                             1 calls
1>        0 ms  BeforeLink                                 1 calls
1>        0 ms  _Appverifier                               1 calls
1>        0 ms  _CopySourceItemsToOutputDirectory          1 calls
1>        0 ms  ComputeLinkSwitches                        1 calls
1>        0 ms  ComputeCLCompileGeneratedXDCFiles          1 calls
1>        0 ms  Build                                      1 calls
1>        0 ms  AfterBuild                                 1 calls
1>        0 ms  SetBuildDefaultEnvironmentVariables        1 calls
1>        0 ms  BuildGenerateSources                       1 calls
1>        0 ms  FixupCLCompileOptions                      1 calls
1>        0 ms  _CheckForCompileOutputs                    1 calls
1>        0 ms  _SplitProjectReferencesByFileExistence     1 calls
1>        0 ms  _GetProjectReferenceTargetFrameworkProperties   1 calls
1>        0 ms  SetTelemetryEnvironmentVariables           1 calls
1>        0 ms  AfterBuildGenerateSources                  1 calls
1>        0 ms  AddWppClDefinitions                        1 calls
1>        0 ms  AfterBuildGenerateSourcesEvent             1 calls
1>        0 ms  ExpandSDKReferences                        1 calls
1>        0 ms  SetCABuildNativeEnvironmentVariables       1 calls
1>        0 ms  SelectClCompile                            1 calls
1>        0 ms  ComputeReferenceCLInput                    1 calls
1>        0 ms  GetCopyToOutputDirectoryItems              1 calls
1>        1 ms  RunWpp                                     1 calls
1>        1 ms  ComputeCLInputPDBName                      1 calls
1>        1 ms  AssignProjectConfiguration                 1 calls
1>        1 ms  _Xsd                                       1 calls
1>        1 ms  _BuildGenerateSourcesAction                1 calls
1>        1 ms  SetLinkLibraryPaths                        1 calls
1>        1 ms  BuildCompileTraverse                       1 calls
1>        1 ms  _XdcMake                                   1 calls
1>        1 ms  PreLinkEvent                               1 calls
1>        1 ms  _BuildLinkAction                           1 calls
1>        1 ms  PrepareResourceNames                       1 calls
1>        1 ms  PrepareForRun                              1 calls
1>        1 ms  _Deploy                                    1 calls
1>        1 ms  MakeDirsForBscMake                         1 calls
1>        1 ms  MakeDirsForMidl                            1 calls
1>        1 ms  SplitResourcesByCulture                    1 calls
1>        1 ms  _HandlePackageFileConflicts                1 calls
1>        1 ms  ComputeCustomBuildOutput                   1 calls
1>        1 ms  MakeDirsForCl                              1 calls
1>        1 ms  _CheckForInvalidConfigurationAndPlatform   1 calls
1>        1 ms  Telemetry                                  1 calls
1>        1 ms  Telemetry_Packaging                        1 calls
1>        1 ms  ComputeLinkInputsFromProject               1 calls
1>        1 ms  CopyFileToFolders                          1 calls
1>        1 ms  DriverBuildNotifications                   1 calls
1>        1 ms  ResolvedXDCMake                            1 calls
1>        1 ms  BuildCompile                               1 calls
1>        1 ms  DoLinkOutputFilesMatch                     1 calls
1>        1 ms  MakeDirsForLink                            1 calls
1>        1 ms  PostBuildEvent                             1 calls
1>        1 ms  MakeDirsForXdcMake                         1 calls
1>        1 ms  CustomBuild                                1 calls
1>        1 ms  ValidateDriverProperties                   1 calls
1>        1 ms  InfVerif                                   1 calls
1>        2 ms  WarnCompileDuplicatedFilename              1 calls
1>        2 ms  _Manifest                                  1 calls
1>        2 ms  _GenerateSatelliteAssemblyInputs           1 calls
1>        2 ms  GetPackageFiles                            1 calls
1>        2 ms  ValidateNTTargetVersion                    1 calls
1>        2 ms  MakeDirsForResourceCompile                 1 calls
1>        2 ms  RegisterOutput                             1 calls
1>        2 ms  PrepareForBuild                            1 calls
1>        3 ms  AssignTargetPaths                          1 calls
1>        3 ms  InitializeBuildStatus                      1 calls
1>        3 ms  CopyFilesToOutputDirectory                 1 calls
1>        3 ms  FinalizeBuildStatus                        1 calls
1>        3 ms  StampInf                                   1 calls
1>        3 ms  _Link                                      1 calls
1>       12 ms  DriverPackageTarget                        1 calls
1>      240 ms  TestSign                                   2 calls
1>      763 ms  Link                                       1 calls
1>      989 ms  Inf2Cat                                    1 calls
1>     1815 ms  PackageTestSign                            1 calls
1>     1836 ms  DriverTestSign                             1 calls
1>     2813 ms  ApiValidator                               1 calls
1>     8756 ms  ClCompile                                  1 calls
1>
1>Task Performance Summary:
1>        0 ms  CallTarget                                 1 calls
1>        0 ms  GetOutOfDateItems                          3 calls
1>        0 ms  AssignCulture                              1 calls
1>        0 ms  ResolvePackageFileConflicts                1 calls
1>        0 ms  CheckVCToolsetVersion                      1 calls
1>        0 ms  ReadLinesFromFile                          1 calls
1>        0 ms  ValidateNTTargetVersion                    1 calls
1>        1 ms  AssignProjectConfiguration                 1 calls
1>        1 ms  DPVerifierTask                             1 calls
1>        1 ms  SetEnv                                    10 calls
1>        1 ms  Touch                                      2 calls
1>        1 ms  WriteLinesToFile                           1 calls
1>        1 ms  StampInf                                   1 calls
1>        1 ms  Telemetry                                  2 calls
1>        1 ms  ConvertToAbsolutePath                      1 calls
1>        1 ms  Delete                                     2 calls
1>        1 ms  AssignTargetPath                           6 calls
1>        3 ms  MakeDir                                    9 calls
1>        5 ms  Copy                                       2 calls
1>       10 ms  Message                                   16 calls
1>      230 ms  SignTask                                   2 calls
1>      757 ms  Link                                       1 calls
1>      988 ms  Inf2Cat                                    1 calls
1>     1940 ms  ApiValidator                               1 calls
1>     3647 ms  MSBuild                                    3 calls
1>     8754 ms  CL                                         1 calls
========== Build: 1 succeeded, 0 failed, 0 up-to-date, 0 skipped ==========
```

</details>

<hr/>
