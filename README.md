# Threex.chromakey
A ThreeJS extension for live "Green Screening" of video. Simply include this extension and then use the `THREEx.ChromaKeyMaterial(videoName, chromaKeyColor)` as your material. Then in your "animate" loop, update your material with the latest frame from your video using `myGreenScreenMaterial.update()`.

### Example Usage

Creating an object
```javascript
//0xd432 is the green screen color, insert yours, if different, below
var myGreenScreenMaterial = new THREEx.ChromaKeyMaterial("images/myVideo.mp4", 0xd432); 
var myGeometry = new THREE.PlaneBufferGeometry( 5, 5);
var myGreenScreenVideoObject = new THREE.Mesh( myGeometry, myGreenScreenMaterial );
scene.add( myGreenScreenVideoObject );
```

Updating the video frame
```javascript
myGreenScreenMaterial.update();
```

Make sure you remember to start your video as well! Autoplaying should work fine.
