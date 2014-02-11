###The world of NAT and TURN or
###[WebRTC and the ocean of acronyms](https://hacks.mozilla.org/2013/07/webrtc-and-the-ocean-of-acronyms/)

<span class="highlight">NAT</span> - Network Address Translation<br>
<span class="highlight">ICE</span> - Interactive Connectivity Establishment<br>
<span class="highlight">SDP</span> - Session Description Protocol<br>
<span class="highlight">STUN</span> - Session Traversal Utilities for NAT<br>
<span class="highlight">TURN</span> - Traversal Using Relays around NAT<br>

note:
    - And with that, I ahve to introduce you to WebRTC and the ocean of acronyms
    - Most users are behind a NAT, causes problems for P2P connectivity
    - Some NATs we can traverse, use Google's STUN server to find ICE candidates
    - Some NATs can't be traversed, we use a relay server
    - Currently not possible to create super nodes like what Skype has
