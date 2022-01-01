This README will present the repository, how to set it up and how to run it.

## Example Mod

This is an empty example mod to begin your own.

## Setup

### Environment

1. Download [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/downloads/).
2. Download an IDE: [Visual Studio Code](https://code.visualstudio.com/) (Recommended: [Eclipse](https://www.eclipse.org/downloads/) and [IntelliJ](https://www.jetbrains.com/idea/download/#section=windows)).
3. Open the project from your IDE and download Java and Gradle extensions.
4. Run `init` Gradle Task to generate other Gradle Taks.

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
    3. Run `genVSCodeRuns` (or `genEclipseRuns` or `genIntellijRuns`) Gradle Task to load changes.

3. Modify `ExampleMod.java`:

    1. Refactor `ExampleMod` by your `ModName` (or Rename ensuring file name changes too).
    2. Replace package by the `group` variable on `build.gradle`, then move `ModName.java` to the corresponding folder. Erase the empty folder `com.example.examplemod`.
    3. Replace your `modid`:

        ```java
        public static final String MOD_ID = "modid";
        ```

4. Modify `mods.toml`:

    1. `modId="modid"`.
    2. `displayName="Mod Name"`.
    3. Replace `credits`, `authors` and `description`.
    4. Replace your `"modid"` on dependencies.

## Run Project

1. Update your mod version if needed in `build.gradle` and `mods.toml`.
2. Run `genVSCodeRuns` (or `genEclipseRuns` or `genIntellijRuns`) Gradle Task to load changes.
3. Run `runClient` Gradle Task.

Minecraft is now running with your Mod.

## Comments

-   `init` should be always run when opening your IDE.
-   `genVSCodeRuns` (or `genEclipseRuns` or `genIntellijRuns`) should be always run after modifying `build.gradle`
-   Those tasks might be run by default by your IDE based on your configurations and extensions.
