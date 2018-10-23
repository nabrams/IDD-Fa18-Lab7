# Video Doorbell, Lab 7

*A lab report by Natalie B. Abrams*

### In This Report

1. Upload a video of your version of the camera lab to your lab Github repository
1. As usual, update your class Hub repository to add your [forked IDD-Fa18-Lab7](/FAR-Lab/IDD-Fa18-Lab7) repository.
1. Answer the questions in-line below on your README.md.

## Part A. HelloYou from the Raspberry Pi

**a. Link to a video of your HelloYou sketch running.**

[HelloYou](https://youtu.be/dGKOFror4ds)

## Part B. Web Camera

**a. Compare `helloYou/server.js` and `IDD-Fa18-Lab7/pictureServer.js`. What elements had to be added or changed to enable the web camera? (Hint: It might be good to know that there is a UNIX command called `diff` that compares files.)**

First, I notice that in server.js the variables are initialized as constants(const) where in pictureServer.js they are initialized as variables(var). There is also an additional variable in pictureServer (var NodeWebcam) which loads the webcam module. There is also a whole section in the picureserver that sets up the webcam:

```
//----------------------------WEBCAM SETUP------------------------------------//
//Default options
var opts = { //These Options define how the webcam is operated.
    //Picture related
    width: 1280, //size
    height: 720,
    quality: 100,
    //Delay to take shot
    delay: 0,
    //Save shots in memory
    saveShots: true,
    // [jpeg, png] support varies
    // Webcam.OutputTypes
    output: "jpeg",
    //Which camera to use
    //Use Webcam.list() for results
    //false for default device
    device: false,
    // [location, buffer, base64]
    // Webcam.CallbackReturnTypes
    callbackReturn: "location",
    //Logging
    verbose: false
};
var Webcam = NodeWebcam.create( opts ); //starting up the webcam
//----------------------------------------------------------------------------//

```

There is websocket and serial communication in both files, but in the picureServer file, there is an added function takepicure that uses the button to trigger taking the picture, where as before the button changed the color of the screen from black to white.

**b. Include a video of your working video doorbell**

[![Watch the video](./viddoor.jpg)](https://youtu.be/06Eys4E5WHk)

## Part C. Make it your own

**a. Find, install, and try out a node-based library and try to incorporate into your lab. Document your successes and failures (totally okay!) for your writeup. This will help others in class figure out cool new tools and capabilities.**

**b. Upload a video of your working modified project**

[gifShot](https://youtu.be/T7Zji9jaLKU)

![Alt Text](https://media.giphy.com/media/vFKqnCdLPNOKc/giphy.gif)

