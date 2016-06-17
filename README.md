# Threex.chromakey
A ThreeJS extension for live "Green Screening" of video. Simply include this extension and then use the THREEx.ChromaKeyMaterial(videoName, chromaKeyColor) as your material.

### Example Usage

```javascript
//0xd432 is the green screen color, insert yours, if different, below
var myGreenScreenMaterial = new THREEx.ChromaKeyMaterial("images/myVideo.mp4", 0xd432); 
var myGeometry = new THREE.PlaneBufferGeometry( 5, 5);
var myGreenScreenVideoObject = new THREE.Mesh( myGeometry, myGreenScreenMaterial );
scene.add( myGreenScreenVideoObject );
```
