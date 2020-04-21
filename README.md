# Agora switch device demo

[Demo link](https://agora-switch-device.netlify.app/)

Switching devices in mobile devices on the web is not straight forward. 
This is because the web browsers in mobile don't have access to more than one camera at the same time. 
To fix this issue, you need to first stop the previous track and then switch the device.



### The relevant parts: 
```javascript
switchBtn.onclick=()=>{
    localStream.getVideoTrack().stop();
    localStream.switchDevice("video",devices.value);
};
```
(line `68 - 71` in script.js)