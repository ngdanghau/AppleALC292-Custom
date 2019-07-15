AppleALC292-Custom
==================
AppleALC292 custom for DELL E6540
#### Installation
- Download [Lilu.kext](https://github.com/acidanthera/Lilu).
- Download [AppleALC.kext](https://github.com/acidanthera/AppleALC).
- Mount your EFI Partition.
- Navigate to EFI/CLOVER/kexts/Other and place the kext here.
- Open config.plist Set <code>Devices</code> → <code>Audio</code> → <code>Inject</code> = <code>NO</code>
- Add argument alcid=layout-id (layout-id = 12, 18 or 28)

#### Fix Audio 
- Install Lilu + AppleALC with 3 layout above, you will have a audio, without you can use AppleALC292 custom for DELL E6540 of me instead of AppleALC.kext above.
- Replace <code>layout-id = 14</code>

#### Fix Audio Distortion when using Headphones on Laptops
<strong>Note</strong>: If you'd installed AppleALC patch for ALC292, you can skip this step.
- Download latest version of [CodecCommander.kext](https://bitbucket.org/RehabMan/os-x-eapd-codec-commander/downloads/)
- Install the kext to S/L/E or L/E, 
- Rebuild kernel cache
<code>sudo touch /System/Library/Extensions && sudo kextcache -u /</code>
