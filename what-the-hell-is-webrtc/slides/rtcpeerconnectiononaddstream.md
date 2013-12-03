####  `RTCPeerConnection.onaddstream()`

````javascript
// once the remote stream arrives, show it in the remote
// video element
pc.onaddstream = function (e) {
    remoteView.src = URL.createObjectURL(e.stream);
}
````

note:
    Put your speaker notes here.
    You can see them pressing 's'.
