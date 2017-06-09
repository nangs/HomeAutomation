# HomeAutomation
> A project to turn your lights on/off from your android phone with voice control abilities 

> Find video demonstration here https://www.youtube.com/watch?v=AuKCVxZyc6w

## [Cross compile C client on ARMv7]

**Environment Variables**(These are set in ~/.bashrc)**:**

`export NDK="/home/anthony/android-ndk-r13b"`

`export TOOLCHAIN="/home/anthony/android-toolchain"`

`export SYSROOT="/home/anthony/android-ndk-r13b/platforms/android-21/arch-arm"`

`export CC="/home/anthony/android-ndk-r13b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/bin/arm-linux-androideabi-gcc-4.9 --sysroot=$SYSROOT"`


**Note:** You can unset the exported variable by running unset CC(or name of exported here)

  
  <dt>Programs needed on top of the NDK and SDK:</dt>
    <dd>sudo apt-get install android-tools-adb android-tools-fastboot</dd>
  
  <dt>Building the standalone toolchain:</dt>
    <dd>$NDK/build/tools/make_standalone_toolchain.py --arch arm --api 21 --install-dir /home/anthony/android-toolchain</dd>

<dd>Cross compile with pie flag => $CC client.c -fPIE -pie -o client</dd>
</dl>
