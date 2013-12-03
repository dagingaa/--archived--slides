###  Get access to the webcam through `getUserMedia()`

````javascript
navigator.getUserMedia({video: true, audio: true},
  function (localMediaStream) {
      var video = document.querySelector("video");
      video.src = window.URL.createObjectURL(localMediaStream);
});
````

note:
    Put your speaker notes here.
    You can see them pressing 's'.
