###  Get the local stream and send it

````javascript
navigator.getUserMedia({ "audio": true, "video": true },
  function (stream) {
      selfView.src = URL.createObjectURL(stream);
      pc.addStream(stream);

      if (isCaller) {
          pc.createOffer(gotDesc);
      } else {
          pc.createAnswer(pc.remoteDescription, gotDesc);
      }

      function gotDesc(desc) {
        pc.setLocalDescription(desc);
        signallingChannel.send(JSON.stringify({ "sdp": desc }));
      }
});
````

note:
    - So now we need to get the local stream and send it
