####  Add the remote video stream to your UI

````javascript
pc.onaddstream = function (e) {
    video.src = URL.createObjectURL(e.stream);
}
````
