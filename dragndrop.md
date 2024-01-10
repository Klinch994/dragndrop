# DragNDrop in Unreal and Unity 3D Editors
## Introduction
DragNDrop is a common feature of game engine editors, that allows us to easily manipulate assets inside our game environment. This guide aims to introduce DragNDrop functionality to new users, in both Unreal and Unity 3D. 
## Motivation
DragNDrop is the preferred method of asset manipulation in game development due to its intuitive and visual nature, allowing users, especially those new to the field like Junior Artists, to effortlessly interact with and position assets within the scene. This method reduces the learning curve and enhances productivity by providing a direct and tactile means of arranging and organizing elements, fostering a more user-friendly and efficient workflow.
### Unity 3D
#### Unity 3D UI Components
In order to understand how DragNDrop works in Unity 3d Engine Editor, we need to familiarize ourselves with its UI. The breakdown of the UI components in Unity 3D can be seen below:
![unity_3d_ui](https://github.com/Klinch994/dragndrop/assets/156119593/8f54b2e2-2250-49be-b279-0248b808fd09)
1.	Hierarchy: Displays a list of all the GameObjects in the current scene, showcasing the parent-child relationships and allowing users to organize and manage their entities.
2.	Scene: Offers a visual representation of the game world, showcasing all the GameObjects and their placements, allowing users to manipulate and design the environment.
3.	Inspector: Provides detailed information and properties of the selected GameObject, allowing users to modify and configure its components, scripts, and attributes.
4.	Project: Serves as a hub for all project assets, containing files, resources, scripts, and other elements used in the game development process.
#### DragNDrop Use Cases
##### UI and Editor Customization
DragNDrop is applied in creating user interfaces or customizing the Unity Editor layout by dragging and dropping windows or panels as can be seen in the GIF below:
![unity-3d-ui-gif](https://github.com/Klinch994/dragndrop/assets/156119593/4112bef0-b2cc-4a4d-8283-6ffd114112e3)
##### Scene Building
DragNDrop allows for easy placement of assets (like models, prefabs, or UI elements) into the scene view to build the game environment, as can be seen in the GIF below:
![unity-3d-scene-gif](https://github.com/Klinch994/dragndrop/assets/156119593/9bd5e451-38cc-4412-937f-c3afbbfbc4b8)
##### Asset Importing
DragNDrop simplifies importing assets (textures, models, audio files) into the Unity project by dragging them from the file explorer directly into the project folder, as can be seen in the GIF below:
![unity-3d-import-gif](https://github.com/Klinch994/dragndrop/assets/156119593/6191a274-c43b-4096-ba4e-eef790c82f62)
##### Component Assignment
DragNDrop is used to assign components (scripts, materials, shaders) to game objects, as can be seen in the GIF below:
![unity-3d-component-gif](https://github.com/Klinch994/dragndrop/assets/156119593/6e1c94aa-e9f6-4610-9a7e-1bcb7dd5b574)
##### Surface Snapping
Surface snapping involves aligning and adjusting the position, rotation, or scale of objects to seamlessly fit and adhere to surfaces within the game world, enhancing the accuracy of object placement and alignment.
To toggle surface snapping, hold Ctrl (Cmd on Mac) and Shift while clicking on an object with a translation tool selected. This can be seen in the GIF below:

WIP

To toggle vertex snapping, hold V while clicking on an object with a translation tool selected. This can be seen in the GIF below:

WIP

To toggle grid snapping, please refer to the image below:

WIP

#### Video Guide
You can find the video guide for this tutorial here:

WIP

### Unreal Engine
#### Unreal UI Components
Unreal Engine Editor UI components are given below:
![unreal_ui](https://github.com/Klinch994/dragndrop/assets/156119593/ba663940-1b1a-4adf-a8bb-b7d467423c0c)
1.	Viewport: Provides a visual representation of the game world or level, allowing users to see and interact with the scene, manipulate objects, and observe gameplay elements.
2.	World Outliner: Displays a hierarchical list of all the actors (entities) in the current level or scene, allowing users to manage, organize, and manipulate these entities.
3.	Details Panel: Offers comprehensive information and editable properties of the selected actor or asset, enabling users to fine-tune and configure their characteristics.
4.	Content Browser: Serves as a central hub for all project assets, containing meshes, textures, materials, blueprints, and other resources used in the game development process.
##### UI and Editor Customization
DragNDrop is used to customize the layout of the Unreal Editor, such as arranging panels, tabs, or windows to create a personalized workspace, as can be seen in the GIF below:

WIP

##### Scene Building
DragNDrop allows for easy placement of assets (like models, prefabs, or UI elements) into the scene view to build the game environment, as can be seen in the GIF below:

WIP

##### Asset Importing
Drag and Drop simplifies the process of importing assets (textures, models, audio files) into the Unreal Engine content browser by dragging them from the file explorer directly into the content folder, as can be seen in the GIF below:

WIP

##### Component Assignment
DragNDrop is employed to assign components (materials, blueprints, particle systems) to actors or objects within the Details panel, as can be seen in the GIF below:

WIP

##### Surface Snapping
Surface snapping involves aligning and adjusting the position, rotation, or scale of objects to seamlessly fit and adhere to surfaces within the game world, enhancing the accuracy of object placement and alignment.

WIP

##### Blueprint Functionality
DragNDrop is utilized within Blueprints by showcasing examples of connecting nodes, variables, or functions using Drag and Drop functionalities. For more information, please refer to the video guide for this section.

#### Video Guide

WIP

### Summary

WIP

### Appendix
DragNDrop is so intuitive, we often don't realize how much time it saves compared to writing code to achieve the same result. Below is a Python script to demonstrate how basic DragNDrop works “under the hood”:

``` python
import tkinter as tk

def on_drag_start(event):
    # Store the starting position of the drag
    event.widget.startX = event.x
    event.widget.startY = event.y

def on_drag_motion(event):
    # Calculate the distance moved since the drag started
    x_delta = event.x - event.widget.startX
    y_delta = event.y - event.widget.startY

    # Move the dragged widget by the calculated deltas
    event.widget.place(x=event.widget.winfo_x() + x_delta, y=event.widget.winfo_y() + y_delta)

def create_draggable_label(root, text, x, y):
    label = tk.Label(root, text=text, bg='lightblue')
    label.place(x=x, y=y)

    # Bind events to enable dragging
    label.bind('<ButtonPress-1>', on_drag_start)
    label.bind('<B1-Motion>', on_drag_motion)

root = tk.Tk()
root.geometry('400x300')

# Create draggable labels
create_draggable_label(root, 'Drag me', 50, 50)

root.mainloop()
```
Note that our script is very rudimentary – we didn’t have to worry about objects overlapping, types of objects or drop locations – all the things readily implemented in both engines.
