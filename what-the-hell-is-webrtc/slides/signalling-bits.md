###  Signalling bits

````javascript
signallingChannel.onmessage = function (e) {
    if (!pc) {
        call(false);
    }

    var signal = JSON.parse(e.data);
    if (signal.sdp) {
        pc.setRemoteDescription(
            new RTCSessionDescription(signal.sdp)
        );
    } else {
        pc.addIceCandidate(
            new RTCIceCandidate(signal.candidate)
        );
    }
};
````

note:
    Put your speaker notes here.
    You can see them pressing 's'.
