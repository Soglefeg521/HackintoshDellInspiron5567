# HackintoshDellInspiron5567
My attempts to install macOS on Dell Inspiron 15-5567 (i3-7100u, Intel HD620)

#### Currently not working
- 32-bit color (proper EDID inject may be needed)
- WiFi (Need to replace PCI card, currently using external)
- Card Reader (Will never work)

#### Applied DSDT Patches
##### General Patches
- [sys] Fix _WAK Arg0 v2
- [sys] Fix Mutex with non-zero SyncLevel
- [sys] Shutdown Fix v2
##### I2C Patches
- [Windows] Windows 10 Patch
- [GPIO] GPIO Controller Enable [SKL+]
- [TPD0] TPD0 _CRS patch
  ```
  into method label _CRS parent_label TPD0 replace_content begin
  
  Return (ConcatenateResTemplate (SBFB, SBFG))
  
  end;
  ```

#### Current EDID
```
00ffffffffffff0030e4250500000000001a0104902213780a42e59158558f281e505400000001010101010101010101010101010101d01d56f4500016303020350058c21000001ad91756f4500016303020350058c21000001a000000fe004839374831803135365748550a0000000000004131940010000009010a20200092
```

#### Original EDID
```
00ffffffffffff0030e4250500000000001a0104952213780a42e59158558f281e505400000001010101010101010101010101010101d01d56f4500016303020350058c21000001ad91756f4500016303020350058c21000001a000000fe004839374831803135365748550a0000000000004131940010000009010a2020008d
```
