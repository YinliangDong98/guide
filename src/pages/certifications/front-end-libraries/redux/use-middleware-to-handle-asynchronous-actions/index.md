---
title: Use Middleware to Handle Asynchronous Actions
---
## Use Middleware to Handle Asynchronous Actions

Dispatch the `requestingData()` actioncreater before `setTimeout()`,dispatch the `receivedData()` actioncreater and incoming data after you received data simulated.
  
```react.js
const handleAsync = () => {
  return function(dispatch) {
    dispatch(requestingData());
    setTimeout(function() {
      let data = {
        users: ['Jeff', 'William', 'Alice']
      }
      dispatch(receivedData(data));
    }, 2500);
  }
};
```


<!-- The article goes here, in GitHub-flavored Markdown. Feel free to add YouTube videos, images, and CodePen/JSBin embeds  -->
