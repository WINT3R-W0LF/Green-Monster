# How to be unreal

## https://dev.epicgames.com/community/learning/tutorials/9k9B/unreal-engine-begin-play-world-building
### World Building
- All building happens in "Levels"
- Level houses all of the content for that space
- "Actors" are placed in there
   - Lights, volume types, level instances, etc..
   - Most actors placed in a scene will come from a content browser
   - All assets get imported into the content browser
     - EVERYTHING
   - There are a suite of tools baked in to create your own content. 3D tools. (Modeling and audio)

- To customize the instance of an actor inside of a level can be customized through the details panel
  - If one file per actor is enabled, the actor is stored as its own file to control individual elements

 - Placeable world building has foliage, water, and placeable shit

 - Level controls handle streaming distances, cutscene tools like sequencer

 - Rebuilding tools, sounds like compilers for mesh and shit. Can be automated with a build machine

 - Everything is built from scratch to start with all kinds of shit.
   - Do we NEED to customize this

- Volumes = effects and status to player
- Blueprints = gameplay events and triggers (can be used to build the level)

- Place actors panel (square with +)
  - Lights and stuff that have already been built
  - This is a searchable field "cube"
  - There is an unreal marketplace and bridge for assets
 
- Content drawer = ctrl+space
  - Most can be dragged and dropped
  - Textures must be assigned to a material which needs to be assigned to a mesh or detail or similar
  - Details on the right after you place is where you make the changes.  (Physics, all, etc..)
  - Each actor has different options
 
- Settings, plugins, modeling tools editor mode, enable
- modeling mode, add box, polydeform, all kinds of stuff
- Bottom tab, makes a default folder and places it in there. Then you can dupe

- Speed tools
- Foliage, misnamed can be used for instance meshes. Spawn large quanities of meshes.
- Grass to spawn small non-collidable meshes. Runs on the GPU
- Landscape, can select components with the manage tab, can import stuff. EVERYTHING IS PICKED UP BY LANDSCAPE
- Water, similar. Search the type such as lake
- Sky and atmosphere, clouds like volumetric or static. CROSS PLATFORM REQUIRES BOTH

- ctrl + L for lighting. Sun source light
- Skylight = base luminence
  - MUST FOR CLOUDS
 
- Material editor
  - Quickly smoke test
 
- Level Controls
  - Raw properties, specific parameters, within world window
    - Game mode which will template like grass and light and shit
   
- World partition
  - Control content that is loaded in where    
  
  - Blueprints is like content browser but limited to the level
    - Good for lots of different levels

- Variance can change states quickly
- Sequencer is scripted events, cutscenes, cinematics, tracks for camera controls

- Pre-processing content before ship
  - Light maps or volumetric light maps
  - Limited traversal opportunities helps
  - AI nav mesh
  - World partition proxies on distance
  - Can be automated through an automation server
  - Another machine would be required
 
- We will need to profile to debug
  - Scalability, optiomize
  - View port is needed for shader complexity, overdraw, lumen, surface cache, rendering
  - Actors should not be manually drawn and can assign to assets for max draw distance
  - Can be set per platform
 
- Console commands
  - Stats GPU shows max, min for each gpu pass
    - This is also important for ensuring it runs smooth       
