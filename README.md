While working on one of my games for Live Pixel Games I needed to create a custom node that would teleport the object to a specfic location. Below is a picture and the script you can use or download to use this in your game. 

![ea53d3fee3a893ef10d13700e87d3fa8](https://github.com/djware/Buildbox-Teleport-node/assets/85318457/2ab22445-abc6-47ec-a92c-497c11526061)


```
function init() { 
}
function update(dt) { 
} 
function signal(name, value) { 
if (value) {
 let assetName = this.attribute('Asset Name'); 
  let ent = this.entity(); 
 if (ent == null) { 
  error('Asset "' + assetName + '" does not exist'); 
  } 
  let pos = this.attribute('Teleport Position'); 
  ent.setPosition(pos.x, pos.y, pos.z); 
 } 
}
```
Make sure to add the custom attributes 

![ce75958de414f36edc2cd7abd2d569cb](https://github.com/djware/Buildbox-Teleport-node/assets/85318457/22717234-fa4a-4c37-a532-3c0240bfe21f)


If your object collides with the object of your choice it will teleport to the cordinates you have typed down in "Teleport Position". 
