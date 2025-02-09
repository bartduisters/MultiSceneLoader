<h1 align="center">MultiSceneLoader</h1>

Simple project that helps in managing scenes existing of multiple scenes.

Usecase:

You or your team with members working on a level. One does level and environment design, the other is doing the programming, etc..
Instead of placing each developer in a prefab within a single scene, you can each assign them a dedicated scene to work on their part.

The MultiSceneObject will reference those scenes.

Instead of using the scenemanager to load a single scene, you can create a MultiSceneObject in your asset folder and assign each scene-file (by string name) 
that should form a singular scene. Placing the Multiscene manager script in your scene allows you to load this object which will then 
use unity's scenemanager to load each contained scene. You call the load methods through a singleton static instance, but it looks similar to the
scenemanagers "LoadScene" syntax.


Note:

- All the scenes that you want to load do have to be present in your build list.
- The multiscenes that you are using should also be present in the LoadManager's build list.
- Working with this method also prevents/reduces merge conflicts within unity projects as developers are not touching eachothers scenes.


Instalation:

- Either clone the complete project.
- Or if you are only interested in the system, download the MultiScene_loader folder inside the script folder and import it.
  Then create an Empty GameObject and attach the MultiSceneManager to it.
 
- Create a MultiSceneObject by right clicking in your Asset folder, go to ScriptableObjects and click on MultiSceneObject.
