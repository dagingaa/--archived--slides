###  Get access to the webcam through `getUserMedia()`

````javascript
navigator.getUserMedia({video: true, audio: true},
  function (localMediaStream) {
      var video = document.querySelector("video");
      video.src = window.URL.createObjectURL(localMediaStream);
});
````

note:
    - Let's start with the easy part, getUserMedia
    - Allows you to stream webcam and microphone output to a video element
    - THis example is a bit cheating, we also need the HTML
