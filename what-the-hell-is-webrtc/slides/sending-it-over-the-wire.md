###  Sending it over the wire with `RTCPeerConnection()`

*Caveat: You need a signalling server*

````javascript
var signallingChannel = createSignallingChannel();
var pc;
var configuration = {...};

function call(isCaller) {
    pc = new RTCPeerConnection(configuration);

    // Send ICE candidates to the other peer
    pc.onicecandidate = function (e) {
        signallingChannel.send(JSON.stringify({"candidate": evt.candidate}));
    }
    // contd...
}
````

note:
    Put your speaker notes here.
    You can see them pressing 's'.
