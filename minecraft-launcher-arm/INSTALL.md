## Step 1: Run the launcher

`minecraft-launcher`

## Step 2: Edit the profile

Click "Edit Profile"

![Edit Profile](https://github.com/benthetechguy/miscprograms/raw/master/minecraft-launcher-arm/EditProfile.png)

Select "Use Version", choose the version you require

![Use Version](https://github.com/benthetechguy/miscprograms/raw/master/minecraft-launcher-arm/UseVersion.png)

## Step 3: Change the launch settings

Tick "Executable"

Replace the OpenJDK path with the Oracle JDK path:

`/usr/lib/jvm/java-8-jdk/bin/java`

The next step differs depending on if you're using 32 or 64 bit ARM:

### 32 Bit

Tick "JVM Arguments"

Add the following to the beginning of the arguments to specify lwjgl2 or lwjgl3 depending on minecraft version:

1.12.2 and earlier:

`-Dorg.lwjgl.librarypath=/opt/minecraft/lwjgl2arm32`

1.13 to 1.14.2 will not run on 32 Bit ARM.

1.14.3 to 1.16.5:

`-Dorg.lwjgl.librarypath=/opt/minecraft/lwjgl3arm32`

All releases and snapshots past 1.16.5 will not run.

Example:

![Launch Settings](https://github.com/benthetechguy/miscprograms/raw/master/minecraft-launcher-arm/LaunchSettings.png)

Click "Save Profile"

### 64 Bit

Tick "JVM Arguments"

Add the following to the beginning of the arguments to specify lwjgl3:

1.14.2 and earlier will not run on 64 Bit ARM.

1.14.3 to 1.16.5:

`-Dorg.lwjgl.librarypath=/opt/minecraft/lwjgl3arm64`

All releases and snapshots past 1.16.5 will not run.

Click "Save Profile"

![Save Profile](https://github.com/benthetechguy/miscprograms/raw/master/minecraft-launcher-arm/SaveProfile.png)

## Step 4: Install and Play Minecraft

Click "Play" to install and launch Minecraft.

![Play](https://github.com/benthetechguy/miscprograms/raw/master/minecraft-launcher-arm/Play.png)

If everything went correctly Minecraft should be up and running!
