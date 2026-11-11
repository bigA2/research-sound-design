# u302hpxNDFs
(source: transcript)

**Recipe for the After Effects SaaS Tutorial**

**Background Animation**

1. Add a solid color background layer (white color)
2. Add a four-color gradient effect to the background layer
3. Change the pink color to a darker color (hex code: #333333)
4. Increase the darkness of the background color

**Text Animation**

1. Copy the first text layer
2. Create a new text layer and change its color to black
3. Apply the Europa font to the new text layer
4. Add a blur effect to the text layer
5. Increase the blur effect to create a smooth animation

**Null Layer and Keyframe Animation**

1. Create a null layer and parent the text layer to it
2. Add a scale keyframe to the null layer (start at 0, end at 100%)
3. Add a position keyframe to the null layer (start at 0, end at 100%)
4. Increase the scale value and adjust the position keyframe
5. Remove unnecessary keyframes
6. Add new keyframes to create a smooth animation

**Sequence Animation**

1. Create another null layer and parent the first null layer to it
2. Add a position and scale keyframe to the second null layer (start at 0, end at 100%)
3. Zoom out the scale keyframe and adjust the animation at the center
4. Use the flow plug-in to create a smoother animation

**Settings and Easing**

1. Use easy ease easing for the keyframes
2. Set the keyframe timings to:
	* 0-10 frames: 0% scale and position
	* 10-20 frames: 100% scale and position
	* 20-30 frames: 100% scale and position (zoom out)
3. Use the graph editor to adjust the easing and timing of the keyframes

**Typography and UI Mockup**

1. Use the Europa font for the text layer
2. Set the font size to 24pt
3. Use a white color for the text layer
4. Create a UI mockup with a white background and a dark gray color for the text

**Background Animation and Sound**

1. Add a background animation with a smooth transition
2. Use a sound effect to enhance the animation (e.g. a gentle whoosh sound)

**Reproducing the Animation in Remotion**

To reproduce the animation in Remotion, you can use the following code:

```jsx
import { spring } from 'remotion';

const animation = () => {
  const textLayer = new TextLayer({
    text: 'Say no to cluttered docs.',
    fontSize: 24,
    color: 'white',
    font: 'Europa',
  });

  const backgroundLayer = new SolidColorLayer({
    color: '#333333',
  });

  const nullLayer = new NullLayer();

  const scaleKeyframe = spring({
    from: 0,
    to: 1,
    duration: 10,
  });

  const positionKeyframe = spring({
    from: 0,
    to: 100,
    duration: 10,
  });

  const sequenceKeyframe = spring({
    from: 0,
    to: 100,
    duration: 10,
  });

  return (
    <Group>
      {backgroundLayer}
      {textLayer}
      {nullLayer}
      <Group>
        {scaleKeyframe}
        {positionKeyframe}
        {sequenceKeyframe}
      </Group>
    </Group>
  );
};
```

Note that this is a simplified version of the code and may require additional adjustments to match the exact animation and settings of the After Effects tutorial.

**Recipe for the Animation**

1. **Text Animation**
	* Create a text layer with the text "Say no to cluttered docks. Craft is all."
	* Duplicate the text layer and add a fast box blur with a radius of 7-10
	* Remove the black part of the blur and keep only the purple part
	* Place the blurred text layer below the original text layer
	* Set the opacity of the blurred text layer to 30-35
2. **Folder Animation**
	* Create a folder layer and add a tint effect with a second color of a dark purple/pinkish color
	* Change the first color to white
	* Rotate the folder layer slightly
	* Add more folders and copy the tint effect to each one
	* Add a fast box blur to each folder with an intensity of 10-15%
	* Parent all the folders to a null layer
	* Add position and rotation keyframes to each folder to create a subtle animation
	* Apply the flow plug-in to the keyframes to slow down the animation
3. **Cloud Animation**
	* Create a cloud layer and add a rotation keyframe to create a subtle animation
	* Increase the gap between the keyframes to slow down the animation
	* Apply the flow plug-in to the keyframes to slow down the animation
4. **Fade In Effect**
	* Add an opacity keyframe to the text layer to create a fade in effect
	* Move the second text animation to a null layer and merge it with the main text layer
	* Add a position and scale keyframe to the null layer to create a zoom in effect
	* Apply the flow plug-in to the keyframes to slow down the animation
5. **Background Animation**
	* Add a keyframe to the background layer to change the color to a dark purple/pinkish color
	* Move the keyframe to the middle of the animation
6. **Craft Logo**
	* Add a craft logo to the composition
	* Remove the logo later in the tutorial

**Settings**

* Keyframe timings:
	+ Folder animation: 10-15% intensity, 10-15 frame gap between keyframes
	+ Cloud animation: 10-15% intensity, 10-15 frame gap between keyframes
	+ Fade in effect: 30-35 opacity, 10-15 frame gap between keyframes
	+ Background animation: 10-15 frame gap between keyframes
* Easing/graph editor values:
	+ Folder animation: easy ease
	+ Cloud animation: easy ease
	+ Fade in effect: easy ease
* Text animator setup:
	+ Duplicate the text layer and add a fast box blur
	+ Remove the black part of the blur and keep only the purple part
	+ Place the blurred text layer below the original text layer
	+ Set the opacity of the blurred text layer to 30-35
* Masks:
	+ None
* Camera/null moves:
	+ None
* Motion blur:
	+ None
* Glow:
	+ Add a fast box blur to the text layer with a radius of 7-10
	+ Remove the black part of the blur and keep only the purple part
	+ Place the blurred text layer below the original text layer
	+ Set the opacity of the blurred text layer to 30-35
* Transitions:
	+ None
* UI mockup handling:
	+ None
* Typography sizes/fonts:
	+ None
* Background animation:
	+ Add a keyframe to the background layer to change the color to a dark purple/pinkish color
	+ Move the keyframe to the middle of the animation
* Sound:
	+ None

**Reproducing the Animation in Remotion**

To reproduce the animation in Remotion, you can use the following code:
```jsx
import { interpolate, spring } from 'remotion';

const folderAnimation = () => {
  const folder = new Folder();
  const keyframes = [
    { time: 0, position: [0, 0], rotation: 0 },
    { time: 10, position: [10, 10], rotation: 10 },
    { time: 20, position: [20, 20], rotation: 20 },
  ];

  return (
    <div>
      {keyframes.map((keyframe, index) => (
        <div
          key={index}
          style={{
            position: 'absolute',
            top: keyframe.position[1],
            left: keyframe.position[0],
            transform: `rotate(${keyframe.rotation}deg)`,
            opacity: spring(index / keyframes.length, {
              mass: 1,
              damping: 20,
              stiffness: 100,
            }),
          }}
        >
          <Folder />
        </div>
      ))}
    </div>
  );
};

const cloudAnimation = () => {
  const cloud = new Cloud();
  const keyframes = [
    { time: 0, rotation: 0 },
    { time: 10, rotation: 10 },
    { time: 20, rotation: 20 },
  ];

  return (
    <div>
      {keyframes.map((keyframe, index) => (

**Recipe for the Animation**

1. **Text Layer Setup**
	* Create a text layer with the text "Say no to cluttered docks. Craft is your all-in-one workspace for ideas."
	* Duplicate the text layer and move it to the top
	* Increase the length of the duplicated text layer
	* Adjust the text layer to fit the screen
2. **Text Animation**
	* Add a blinking cursor effect to the text layer
	* Customize the cursor to match the animation
	* Add keyframes to the text layer to create a typing effect
3. **Color Animation**
	* Change the color of the text layer to a purple color
	* Add a gradient effect to the text layer
	* Use a black and white color scheme with a gray tone to create a premium look
4. **Brain PNG Animation**
	* Add a brain PNG to the text layer
	* Parent the brain PNG to the text layer
	* Trim out the extra part of the brain PNG
	* Add a scale keyframe to the brain PNG
	* Use the bounce expression to create a bouncy animation
5. **Inner Glow Animation**
	* Add an inner glow effect to the brain PNG
	* Change the color of the inner glow to a pink color
	* Increase the glow value of the inner glow
6. **Tab Animation**
	* Create two rectangle shapes to represent the tabs
	* Duplicate the rectangle shape and rename it to "back layer"
	* Increase the scale value of the back layer
	* Add a roundness effect to the rectangle shape

**Settings**

* Keyframe timings:
	+ 0s: Text layer setup
	+ 1s: Text animation
	+ 2s: Color animation
	+ 3s: Brain PNG animation
	+ 4s: Inner glow animation
	+ 5s: Tab animation
* Easing/graph editor values:
	+ Bounce expression: 0.5, 0.5, 0.5, 0.5
* Text animator setup:
	+ Blinking cursor effect: 0.5, 0.5, 0.5, 0.5
* Masks:
	+ None
* Camera/null moves:
	+ None
* Motion blur:
	+ 0.5
* Glow:
	+ Inner glow effect: 0.5, 0.5, 0.5, 0.5
* Transitions:
	+ None
* UI mockup handling:
	+ None
* Typography sizes/fonts:
	+ Font size: 24
	+ Font family: Arial
* Background animation:
	+ None
* Sound:
	+ None

**Reproducing the Animation in Remotion**

To reproduce the animation in Remotion, you can use the following code:
```jsx
import { interpolate, spring } from 'remotion';

const textLayer = {
  x: 0,
  y: 0,
  text: 'Say no to cluttered docks. Craft is your all-in-one workspace for ideas.',
  fontSize: 24,
  fontFamily: 'Arial',
};

const brainPNG = {
  x: 0,
  y: 0,
  width: 100,
  height: 100,
  src: 'brain.png',
};

const innerGlow = {
  x: 0,
  y: 0,
  width: 100,
  height: 100,
  color: '#FF69B4',
  glowValue: 0.5,
};

const tabLayer = {
  x: 0,
  y: 0,
  width: 100,
  height: 100,
  roundness: 0.5,
};

const animation = () => {
  const time = interpolate(0, 5, 0, 1);

  const textX = spring(textLayer.x, time);
  const textY = spring(textLayer.y, time);
  const brainX = spring(brainPNG.x, time);
  const brainY = spring(brainPNG.y, time);
  const innerGlowX = spring(innerGlow.x, time);
  const innerGlowY = spring(innerGlow.y, time);
  const tabX = spring(tabLayer.x, time);
  const tabY = spring(tabLayer.y, time);

  return (
    <div>
      <text
        x={textX}
        y={textY}
        text={textLayer.text}
        fontSize={textLayer.fontSize}
        fontFamily={textLayer.fontFamily}
      />
      <image
        x={brainX}
        y={brainY}
        width={brainPNG.width}
        height={brainPNG.height}
        src={brainPNG.src}
      />
      <div
        x={innerGlowX}
        y={innerGlowY}
        width={innerGlow.width}
        height={innerGlow.height}
        style={{
          backgroundColor: innerGlow.color,
          opacity: innerGlow.glowValue,
        }}
      />
      <div
        x={tabX}
        y={tabY}
        width={tabLayer.width}
        height={tabLayer.height}
        style={{
          borderRadius: tabLayer.roundness

**Recipe:**

1. **Layer Settings:**
	* Scale: 100% (at 0s)
	* Opacity: 50% (at 0s)
	* Parent the back layer to the white main layer
2. **Text Animator Setup:**
	* Select the text layer
	* Add a text animator
	* Set the text animator to "Scale"
	* Set the scale value to 100% (at 0s)
	* Set the scale value to 50% (at 10s)
3. **Masks:**
	* Create a new mask
	* Set the mask to "Rectangle"
	* Set the rectangle to have a roundness of 50%
	* Set the anchor point to the center
4. **Camera/Null Moves:**
	* Create a new null layer
	* Parent the null layer to the main layer
	* Add a position keyframe to the null layer at 0s
	* Set the position to (0, 0)
	* Add a position keyframe to the null layer at 10s
	* Set the position to (100, 100)
5. **Motion Blur:**
	* Enable motion blur on the main layer
	* Set the motion blur to 10 frames
6. **Glow:**
	* Add a glow effect to the main layer
	* Set the glow size to 10
	* Set the glow color to white
7. **Transitions:**
	* Add a transition to the main layer
	* Set the transition to "Fade In"
	* Set the transition duration to 2 seconds
8. **UI Mockup Handling:**
	* Create a new layer for the UI mockup
	* Parent the UI mockup layer to the main layer
	* Add a position keyframe to the UI mockup layer at 0s
	* Set the position to (0, 0)
	* Add a position keyframe to the UI mockup layer at 10s
	* Set the position to (100, 100)
9. **Typography Sizes/Fonts:**
	* Set the font to "SF Pro Display"
	* Set the font size to 24
10. **Background Animation:**
	* Create a new layer for the background animation
	* Parent the background animation layer to the main layer
	* Add a position keyframe to the background animation layer at 0s
	* Set the position to (0, 0)
	* Add a position keyframe to the background animation layer at 10s
	* Set the position to (100, 100)
11. **Sound:**
	* Add a sound effect to the main layer
	* Set the sound effect to a fade-in sound

**Reproducing in Remotion:**

To reproduce this animation in Remotion, you will need to write code to achieve the same effects. Here is a possible implementation:

```jsx
import { interpolate, spring } from 'remotion';

const animation = () => {
  const scale = spring(0.5, {
    mass: 1,
    tension: 100,
    friction: 20,
  });

  const opacity = spring(0.5, {
    mass: 1,
    tension: 100,
    friction: 20,
  });

  const position = spring(100, {
    mass: 1,
    tension: 100,
    friction: 20,
  });

  return (
    <div
      style={{
        position: 'absolute',
        top: 0,
        left: 0,
        width: '100%',
        height: '100%',
        backgroundColor: 'white',
        opacity: opacity.value,
      }}
    >
      <div
        style={{
          position: 'absolute',
          top: 0,
          left: 0,
          width: '100%',
          height: '100%',
          backgroundColor: 'gray',
          opacity: 0.5,
        }}
      >
        <div
          style={{
            position: 'absolute',
            top: 0,
            left: 0,
            width: '100%',
            height: '100%',
            backgroundColor: 'pink',
            opacity: 0.5,
          }}
        >
          <div
            style={{
              position: 'absolute',
              top: 0,
              left: 0,
              width: '100%',
              height: '100%',
              backgroundColor: 'white',
              opacity: 0.5,
            }}
          />
        </div>
      </div>
      <div
        style={{
          position: 'absolute',
          top: 0,
          left: 0,
          width: '100%',
          height: '100%',
          fontSize: 24,
          fontFamily: 'SF Pro Display',
          opacity: 0.5,
        }}
      >
        <div
          style={{
            position: 'absolute',
            top: 0,
            left: 0,
            width: '100%',
            height: '100%',
            fontSize: 24,
            fontFamily: 'SF Pro Display',
            opacity: 0.5,
          }}
        />
      </div>
    </div>
  );
