# Welcome to my dumpster

This is the place where I keep all my stuff related to Redmi Note 8T together. I know the website is kinda crappy, but I'm too lazy to create a proper one, so this one should do for now.

Right now I maintain one Android distribution, LineageOS 16.0 (Android Pie). I kinda explained my reasons behind maintaining this in its dedicated section.

I'm planning on maintaining SailfishOS on Redmi Note 8T too, so y'know, if you're really waiting for it, let me know, I guess.


## LineageOS 16
Long story short, it's just the LineageOS build I maintain for myself to use.

There were a few reasons why I took this "project" up. Right now it's just an upstreamed build of LineageOS 16.0 based on [Tarkzim](https://github.com/tarkzim)'s trees (or, maybe more correctly, [Xiaomi-trinket-dev](https://github.com/Xiaomi-trinket-dev)). The entire list of changes for now is below:

 * reverted to clang version provided by Google in Pie (literally commented out `TARGET_KERNEL_CLANG_VERSION` [here](https://github.com/Xiaomi-trinket-dev/android_device_xiaomi_sm6125-common/blob/lineage-16.0/BoardConfigCommon.mk)),
 * integrated [this patch](https://github.com/lineageos4microg/docker-lineage-cicd/blob/master/src/signature_spoofing_patches/android_frameworks_base-P.patch) to enable signature spoofing support, to make microG work out of the box.

Yes, this is all I made to it. That's why I'm not even pushing the source right now - because there is nothing interesting to be pushed.

My goal was to check if it's even building. I have a list of goals which I want to achieve before moving forward.

Ah, yes. I'm taking this up because I want to use it as a base for SailfishOS in the future. And also I wanted to have my own customized build of Lineage filling my needs, because I have to live on Android for some time anyway.

### Known bugs
 * sometimes SIM cards don't turn on after startup - usually a reboot fixes this
 * sometimes SIM2 indicator doesn't pop up - you need to turn off and on that SIM card, `or just ignore it`
 * wide and macro lens don't seem to work
 * selinux is permissive - not going to fix

### Roadmap
 * [x] build tarkzim's tree as is
 * [ ] fix a few bugs found
 * [ ] maybe change the default dns servers to dns.watch?
 * [ ] reconfigure the tree to use Linaro GCC toolchain to build the kernel
 * [ ] disable dm-verity and force-encrypt out of the box
 * [ ] try to create common builds for ginkgo and willow
 * [ ] do some extreme blob updates
 * [ ] prepare the tree to be used as SailfishOS base


## Downloads
All the downloads are held at the [CodeBucket mirror](https://mirror.codebucket.de/mattroot/willow/).


## Contact
There are two ways for you to contact me right now, Telegram and Matrix. I'm not really anxious about PMs, as long as you know what you're doing and you're not forcing me to guide you by hand. I didn't really make a group for my development, because... why, lol.

 * Telegram: [@MattRoot](https://t.me/MattRoot)
 * Matrix: `@mattroot:matrix.org`
 