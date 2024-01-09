# DragNDrop in Unreal and Unity 3D Editors
## Introduction
DragNDrop is a common feature of game engine editors, that allows us to easily manipulate assets inside our game environment. This guide aims to introduce DragNDrop functionality to new users, in both Unreal and Unity 3D. 
## Motivation
DragNDrop is the preferred method of asset manipulation in game development due to its intuitive and visual nature, allowing users, especially those new to the field like Junior Artists, to effortlessly interact with and position assets within the scene. This method reduces the learning curve and enhances productivity by providing a direct and tactile means of arranging and organizing elements, fostering a more user-friendly and efficient workflow.
### Unreal Engine
#### Unreal UI Components
In order to understand how DragNDrop works in Unreal Engine Editor, we need to familiarize ourselves with its UI. The breakdown of the UI components in Unreal Engine can be seen below:
![unity_3d_ui](https://github.com/Klinch994/dragndrop/assets/156119593/8f54b2e2-2250-49be-b279-0248b808fd09)
1.	Viewport: Provides a visual representation of the game world or level, allowing users to see and interact with the scene, manipulate objects, and observe gameplay elements.
2.	World Outliner: Displays a hierarchical list of all the actors (entities) in the current level or scene, allowing users to manage, organize, and manipulate these entities.
3.	Details Panel: Offers comprehensive information and editable properties of the selected actor or asset, enabling users to fine-tune and configure their characteristics.
4.	Content Browser: Serves as a central hub for all project assets, containing meshes, textures, materials, blueprints, and other resources used in the game development process.
#### DragNDrop Use Cases
##### Asset Importing
Drag and Drop simplifies the process of importing assets (textures, models, audio files) into the Unreal Engine content browser by dragging them from the file explorer directly into the content folder, as can be seen in the GIF below:
