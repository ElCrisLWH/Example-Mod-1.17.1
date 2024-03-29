This README will present the repository and how to use it.

# Example Mod

This is an empty example mod to begin your own mod for [Minecraft Java Edition](https://minecraft.fandom.com/wiki/Java_Edition) using [Minecraft Forge](https://mcforge.readthedocs.io/).

Java basic knowledge might help understanding and developing.

This project uses [Gradle](https://gradle.org/) as its build automation tool, but no prior knowledge is required.

## Setup

Before modding, make sure to setup your environment and personalize your proyect.

### Environment

1. Download [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/downloads/).
2. Download an IDE: [Visual Studio Code](https://code.visualstudio.com/) (or [Eclipse](https://www.eclipse.org/downloads/) or [IntelliJ](https://www.jetbrains.com/idea/download/#section=windows)).
3. Open the project from your IDE and download Java and Gradle extensions.
4. Run `init`.

### Mod

1. Replace this README by your own.
2. Modify `build.gradle`:

    1. Replace `version`, `group` and `archivesBaseName`:

        ```java
        version = '1.17.1-0.0.0' // recommended: 'minecraft_version-mod_version'
        group = 'net.yourname.modid' // recommended: 'net.yourname.modid'
        archivesBaseName = 'modid' // your modid
        ```

    2. Replace `'examplemod'` by your `'modid'` everywhere in the file.
    3. Run `genVSCodeRuns` (or `genEclipseRuns` or `genIntellijRuns`).

3. Modify `ExampleMod.java`:

    1. Refactor `ExampleMod` by your `ModName` (or Rename ensuring file name changes too).
    2. Replace package by the `group` variable on `build.gradle`, then move `ModName.java` to the corresponding folder. Erase the empty folder `com.example.examplemod`.
    3. Replace your `modid`:

        ```java
        public static final String MOD_ID = "modid";
        ```

4. Modify `mods.toml`:

    1. `modId="modid"`.
    2. `version="0.0.0"`.
    3. `displayName="Mod Name"`.
    4. Replace `credits`, `authors` and `description`.
    5. Replace your `"modid"` on dependencies.

## Versions

To declare a new release of your mod:

1. Update your mod version in `build.gradle` and `mods.toml`.
2. Run `genVSCodeRuns` (or `genEclipseRuns` or `genIntellijRuns`).

## Run Project

1. Run `runClient`.

Minecraft is now running with your mod.

## Additional Notes

-   `init` Gradle Task should be always run when opening your IDE to generate other Gradle Tasks.
-   `genVSCodeRuns` (or `genEclipseRuns` or `genIntellijRuns`) Gradle Task should be always run after modifying `build.gradle` to load changes.
-   Those tasks might be run by default by your IDE based on your configurations and extensions.
