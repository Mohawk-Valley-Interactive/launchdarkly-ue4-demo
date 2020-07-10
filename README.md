# Notes
This repository has a submodule that links to the LaunchDarkly Client UE4 Plugin (https://github.com/launchdarkly-labs/launchdarkly-client-ue4-plugin). *Remember to initialize the submodule after cloning the repository.*

The LaunchDarkly client is initialized via the Mobile Key variable in the BP_GameInstance Blueprint.

The scenes assume the following LaunchDarkly flags are in place:
* cube-rotation-axis
  * Determines the rotation of the cubes.
  * Should be a JSON object with the following format: {'x': 1.0, 'y': 0.0, 'z': 0.0}
  * A zero vector will result in no rotation.
* background-color
  * Establishes the background color in the scene.
  * Should be a JSON object with the following format: {'a': 0.0, 'r': 1.0, 'g': 0.0, 'b': 0.0}
* show-options-menu
  * Determines if the "options" button in the main menu is visible.
  * Should return a boolean variation.

The following custom user attributes are used in the scenes (using the previously mentioned LD project) as follows:
* level-id
  * A numeric value of 0 or 1 to indicate which scene is being used.
* class-type
  * A string value with the following handled variations
    * Barbarian
    * Monk
    * Wizard
  * This is set using the "class" drop-down menu (top-right).