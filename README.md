PixelEXPRates
==============================
** It is a Sponge Plugin **. Make your Pixelmon players' Pokémon earn additional EXP ** in battles ** based on the level of Pokémon used. 4 It is a concept based on servers from other games, like Tibia.

Os comandos são:
- /rates - View server rates - No permission required
- /rates reload - Reloads plugin config - Permission `pixelexprates.reload`


How does this plugin work?
-------------------------------------------
The plugin creates a configuration in the `. / Config /` folder containing the server rates. For example, here is a configuration:
```
rates=[
    {
        expMultiplier=3.0
        minLevel=1
        maxLevel=30
    },
    {
        expMultiplier=2.0
        minLevel=31
        maxLevel=60
    },
    {
        expMultiplier=1.0
        minLevel=61
        maxLevel=100
    }
]
```

This means that between level 1 and 30, a Pokémon will earn 3x normal EXP in battles .

Between level 31 to 60, a Pokémon will earn 2x normal EXP in battles .

Between level 61 and 100, a Pokémon will earn normal EXP (since it is only 1x) in battles .

The plugin only affects battles.

🔨 How to turn the source into .jar
Have the Java Development Kit installed on your computer (Java Runtime Environment may not be enough);
Place the Pixelmon .jar inside the folder /jar-dependencies/
Open a terminal ( cmdfor example);
Navigate the terminal to the root folder of this project (in Windows, the command is used cd);
Run on this terminal gradlew buildand wait for completion;
Get the .jar file built into the folder /build/libs/
💻 How to install the sources to edit it in your IDE
See the Forge Documentation online for more detailed instructions: http://mcforge.readthedocs.io/en/latest/gettingstarted/

Step 1: Open your command-line and browse to the folder where you extracted the zip file.

Step 2: Once you have a command window up in the folder that the downloaded material was placed, type:

Windows: "gradlew setupDecompWorkspace" Linux/Mac OS: "./gradlew setupDecompWorkspace"

Step 3: After all that finished, you're left with a choice. For eclipse, run "gradlew eclipse" (./gradlew eclipse if you are on Mac/Linux)

If you prefer to use IntelliJ, steps are a little different.

Open IDEA, and import project.
Select your build.gradle file and have it import.
Once it's finished you must close IntelliJ and run the following command:
"gradlew genIntellijRuns" (./gradlew genIntellijRuns if you are on Mac/Linux)

Step 4: The final step is to open Eclipse and switch your workspace to /eclipse/ (if you use IDEA, it should automatically start on your project)

If at any point you are missing libraries in your IDE, or you've run into problems you can run "gradlew --refresh-dependencies" to refresh the local cache. "gradlew clean" to reset everything {this does not affect your code} and then start the processs again.

Should it still not work, Refer to #ForgeGradle on EsperNet for more information about the gradle environment.

Tip: If you do not care about seeing Minecraft's source code you can replace "setupDecompWorkspace" with one of the following: "setupDevWorkspace": Will patch, deobfuscate, and gather required assets to run minecraft, but will not generate human readable source code. "setupCIWorkspace": Same as Dev but will not download any assets. This is useful in build servers as it is the fastest because it does the least work.

Tip: When using Decomp workspace, the Minecraft source code is NOT added to your workspace in a editable way. Minecraft is treated like a normal Library. Sources are there for documentation and research purposes and usually can be accessed under the 'referenced libraries' section of your IDE.
