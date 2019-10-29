# Zombie Brains Collector
 
In this Workshop, we will be going over seveeral aspects of creating a game, from using Mixamo to choose and download a model, link the model to it's Animations, and have control of when/how the model activates the Animations.

### What this Workshop covers
    1. Mixamo (Search & Download)
    2. Importing Mixamo model into Unity with Animations
    3. Using Animator and Animation Transitions to control the Model

### What you will need: 
    1. Unity Game Engine installed with supporting packages
    2. VS-Code / Visual Studio
    3. Mouse
    4. Internet Connection

---

## **Mixamo**

Head to www.mixamo.com
When you get into the website, feel free to log in using your UNC credentials, since Mixamo is linked to your Adobe account.

From there, search for "zombie" in the Characters tab, and download the character.

#### Remember to download the Format as "FBX for Unity" and Pose as "Original Pose (.fbx)".

After that, switch to the Animations tab, and search for "Zombie Idle" and "Zombie Run" and download them both.

#### Again, remember to switch the Format to "FBX for Unity".

Now, head to www.poly.google.com
Search for "Brain" in the top and download the Brain low-poly model as an OBJ file.

##### Note: Files we be included in this Repo.

---

## Importing into Unity

Create a new 3D project in Unity.

Drag the downloaded Zombie into Unity, together with both animations that you also downloaded. In total, you should have three files to bring in.

Now, if you try to import your Zombie into the scene, it will be T-posed and it will have no Material texture associated to it (the Zombie will look "white").

To fix this, click on the Zombie prefab in the Project tab, and, on the Inspector window, click on the Materials tab.

Change the following dropdown menus:
`Location:` Use Embedded Materials -> Use External Materials (Legacy)
(Changing the above will give you these new options)
`Naming:` By Base Texture Name -> Model Name + Model's Materials
`Search:` Recusive-Up -> Local Materials Folder

When a pop-up Window appears, select `"Fix Now"`.

Then, proceed to Reimport the entire Zombie into Unity (drag the downloaded file into Unity again).

The new Zombie should have it's materials correctly applied to it.

Drag the new Zombie (named Zombie (1) in your Assets) into the scene and reset it's position to (0, 0, 0).

---

## Animation and Animator Control

Create a new Animator Controller via right-clicking the Project tab, and name it however you want.

Double-click it to open the Animator window.

Drag both the Idle and Running animation to the Animator window, and set the Idle animation to "Default State" by right-clicking it and selecting "Set as Layer Default State".

Now, create transitions between Zombie Idle and Zombie Running by right-clicking one of them, selecting "Make Transition" and left-clicking on the other. Now repeat the process, but right-clicking the other one and making a transition.

On the left-side of the Animator, under Parameters, create a new boolean (by pressing the small plus sign near the search bar) called "moving".

Select the transition FROM idle TO running, and look at the Inspector window.

Beneath CONDITIONS, click on the Plus sign and add "moving" (or whatever you named the Boolean) as a condition being True.

(If Preview says: "No model is available for preview", just drag your Zombie (1) model into that part of the Inspector)

Also make sure to UNCHECK "Exit Time" on the transition.

> Do the same for the transition FROM running TO idle, with the only difference being that the conditional has to be "False" now.

Also, make sure you click on the assets for Idle Animation and Running Animation (on the Projects folder) and make sure you have both "Loop Time" and "Loop Pose" checked.

---

### Some changes to make on the Assets
  1. Select the Brain in the Assets folder and change it's scaling to 0.005 in all axis. (because it's originally imported as a gigantic thing)
  2. Create a pink material and attach it to the Brain in order to give it a nice coloration.
  3. Make sure to add a Box Collider to the Zombie and set it's parameters as:
    `Is Trigger: Yes`
    `Center: 0, 0.9, 0`
    `Scale: 1.9, 1.8, 1`
  4. Also, add a Rigid Body to the Zombie, and uncheck the Gravity box on it.
  5. Make sure to add a Box Collider to the Brain (specifically, to the Default object "inside" the Brain prefab) and set it's parameters as follows:
    `Is Trigger: Yes`
    `Center: 0, 0, 0`
    `Scale: 1, 1, 1`
  6. Reset the Camera's transform, and change it's parameters to such:
    ![](/imgs/cameraParam.png)

---

## Coding

(Shaik, please)

---

## ???

Placeholder

---

## Lets Get Coding


 CARVR - Zombie Big Brain workshop
