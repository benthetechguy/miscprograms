## Step 1: Run the launcher

`minecraft-launcher`

## Step 2: Edit the profile

Click "Edit Profile"

![Edit Profile](https://i.imgur.com/6jHH6Nw.png)

Select "Use Version", choose the version you require

![UseVersion](https://i.imgur.com/8QYHpnQ.png)

## Step 3: Change the launch settings

Tick "Executable"

Replace the OpenJDK path with the Oracle JDK path:

`/opt/jdk/jdk1.8.0_251/bin/java`

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
![Launch Settings](https://i.imgur.com/FTq8eYW.png)
*Ignore the *`/home/pi/lwjgl3arm32`* in the image, this is from a different tutorial using a different directory*

Click "Save Profile"

### 64 Bit

Tick "JVM Arguments"

Add the following to the beginning of the arguments to specify lwjgl3:

1.14.2 and earlier will not run on 64 Bit ARM.

1.14.3 to 1.16.5:

`-Dorg.lwjgl.librarypath=/opt/minecraft/lwjgl3arm64`

All releases and snapshots past 1.16.5 will not run.

Click "Save Profile"

![Save Profile](https://i.imgur.com/2xYmYb5.png)

## Step 4: Install and Play Minecraft

Click "Play" to install and launch Minecraft.

![Play](https://i.imgur.com/8jIVqxW.png)

If everything went correctly Minecraft should be up and running!
