# 3z8BhwTy_Ls
(source: transcript)

**Recipe for the Animation:**

1. **Initial Circle:**
	* Create a new composition with a white solid background.
	* Add an ellipse tool to create a circle.
	* Change the color to a greenish color.
	* Keep the stroke as nil.
	* Add a keyframe at frame 5 for the circle's position.
	* Move the circle to the center of the composition.
	* Select both keyframes and ease them using the graph editor.
	* Add a radial blur effect with an amount of 100 and an angle of 45 degrees.
	* Add a deep glow effect.
2. **Second Circle:**
	* Duplicate the initial circle layer by pressing Command + D.
	* Change the direction of the second circle to come from the opposite side.
	* Delete the original circle layer.
3. **Main Circle:**
	* Create a new circle layer.
	* Add a keyframe at frame 5 for the circle's scale.
	* Increase the scale to 240 at frame 5.
	* Add another keyframe at frame 10 and decrease the scale to 200.
	* Turn off motion blur for all layers.

**Settings:**

* Frame rate: 30fps
* Composition size: 1920x1080
* Initial circle:
	+ Position: (0, 0) at frame 5, (100, 100) at frame 10
	+ Scale: 100 at frame 5, 240 at frame 5, 200 at frame 10
	+ Color: #33CC33 (greenish color)
	+ Stroke: nil
	+ Radial blur: amount 100, angle 45 degrees
	+ Deep glow: enabled
* Second circle:
	+ Position: (100, 100) at frame 5, (0, 0) at frame 10
	+ Scale: 100 at frame 5, 240 at frame 5, 200 at frame 10
	+ Color: #33CC33 (greenish color)
	+ Stroke: nil
	+ Radial blur: amount 100, angle 45 degrees
	+ Deep glow: enabled
* Main circle:
	+ Position: (0, 0) at frame 5, (100, 100) at frame 10
	+ Scale: 100 at frame 5, 240 at frame 5, 200 at frame 10
	+ Color: #FFFFFF (white color)
	+ Stroke: nil
	+ Motion blur: disabled

**Remotion Code:**

```jsx
import { spring } from 'remotion';

const initialCircle = {
  x: 0,
  y: 0,
  scale: 100,
  color: '#33CC33',
  stroke: 'none',
  radialBlur: {
    amount: 100,
    angle: 45,
  },
  deepGlow: true,
};

const secondCircle = {
  x: 100,
  y: 100,
  scale: 100,
  color: '#33CC33',
  stroke: 'none',
  radialBlur: {
    amount: 100,
    angle: 45,
  },
  deepGlow: true,
};

const mainCircle = {
  x: 0,
  y: 0,
  scale: 100,
  color: '#FFFFFF',
  stroke: 'none',
  motionBlur: false,
};

const animation = () => {
  const t = spring(0.5);
  const x = t.interpolate({
    start: 0,
    end: 100,
    duration: 10,
  });
  const y = t.interpolate({
    start: 0,
    end: 100,
    duration: 10,
  });
  const scale = t.interpolate({
    start: 100,
    end: 240,
    duration: 5,
  });
  const color = t.interpolate({
    start: '#33CC33',
    end: '#FFFFFF',
    duration: 10,
  });

  return (
    <div>
      <div
        style={{
          position: 'absolute',
          left: x,
          top: y,
          transform: `scale(${scale})`,
          backgroundColor: color,
          border: 'none',
          width: 100,
          height: 100,
        }}
      />
      <div
        style={{
          position: 'absolute',
          left: 100 + x,
          top: 100 + y,
          transform: `scale(${scale})`,
          backgroundColor: color,
          border: 'none',
          width: 100,
          height: 100,
        }}
      />
      <div
        style={{
          position: 'absolute',
          left: x,
          top: y,
          transform: `scale(${scale})`,
          backgroundColor: '#FFFFFF',
          border: 'none',
          width: 100,
          height: 100,
        }}
      />
    </div>
  );
};

export default animation;
```

Note that this code uses the `spring` function from `remotion` to create a smooth animation. The `interpolate` function is used to create a smooth transition between the start and end values of each property. The animation

**Recipe for the After Effects Animation**

1. **Background Animation**
	* Add a simple ellipse to the background
	* Add a Gaussian blur to the ellipse
	* Create a keyframe for the scale and opacity of the ellipse
	* Set the keyframe to increase the size and decrease the opacity over time
2. **Light Effect**
	* Add a simple circle to the background
	* Add a Gaussian blur to the circle
	* Create a keyframe for the scale and opacity of the circle
	* Set the keyframe to increase the size and decrease the opacity over time
3. **Middle Circle**
	* Add a middle circle to the animation
	* Animate the middle circle using the popping animation
	* Set the scale of the middle circle to 29% at the start and 79% at the end
4. **Blue Patch**
	* Add a blue patch to the animation
	* Rotate the blue patch over time
	* Use a track mat to ensure the blue patch is inside the circle
	* Set the opacity of the blue patch to 50%
5. **Radial Blur**
	* Add a radial blur to the blue patch
	* Set the blur to a low value
6. **Shape Morphing**
	* Add a shape morphing effect to the animation
	* Create a keyframe for the shape morphing effect
	* Set the keyframe to change the shape of the circle over time

**Settings and Values**

* Keyframe timings:
	+ 0-100 frames: increase size and decrease opacity of ellipse and circle
	+ 100-200 frames: increase size and decrease opacity of middle circle
	+ 200-300 frames: rotate blue patch
	+ 300-400 frames: shape morphing effect
* Easing and graph editor values:
	+ Use a linear easing for the keyframes
	+ Use a graph editor to fine-tune the keyframes
* Text animator setup:
	+ Use a simple text animator to animate the text
	+ Set the text animator to follow the animation
* Masks:
	+ Use a track mat to ensure the blue patch is inside the circle
* Camera/null moves:
	+ Use a null object to move the animation
	+ Set the null object to follow the animation
* Motion blur:
	+ Use a motion blur effect to blur the animation
	+ Set the motion blur to a low value
* Glow:
	+ Use a glow effect to add a glow to the animation
	+ Set the glow to a low value
* Transitions:
	+ Use a transition effect to transition between the different parts of the animation
	+ Set the transition to a fade-in/fade-out effect
* UI mockup handling:
	+ Use a UI mockup to handle the animation
	+ Set the UI mockup to follow the animation
* Typography sizes/fonts:
	+ Use a font size of 24pt for the text
	+ Use a font family of Arial for the text
* Background animation:
	+ Use a background animation to animate the background
	+ Set the background animation to follow the animation
* Sound:
	+ Use a sound effect to add sound to the animation
	+ Set the sound effect to follow the animation

**Reproducing the Animation in Remotion**

To reproduce the animation in Remotion, you can use the following code:

```jsx
import { interpolate, spring } from 'remotion';

const animation = () => {
  const { frames } = useRemotion();

  const ellipseScale = spring(0.1, {
    fps: 60,
    mass: 1,
    tension: 300,
    friction: 40,
  });

  const circleScale = spring(0.2, {
    fps: 60,
    mass: 1,
    tension: 300,
    friction: 40,
  });

  const middleCircleScale = spring(0.3, {
    fps: 60,
    mass: 1,
    tension: 300,
    friction: 40,
  });

  const bluePatchRotation = spring(0.4, {
    fps: 60,
    mass: 1,
    tension: 300,
    friction: 40,
  });

  const shapeMorphing = spring(0.5, {
    fps: 60,
    mass: 1,
    tension: 300,
    friction: 40,
  });

  return (
    <div>
      <div
        style={{
          width: '100%',
          height: '100%',
          backgroundColor: 'black',
          position: 'absolute',
          top: 0,
          left: 0,
        }}
      >
        <div
          style={{
            width: '100%',
            height: '100%',
            backgroundColor: 'white',
            position: 'absolute',
            top: 0,
            left: 0,
            transform: `scale(${ellipseScale})`,
          }}
        />
        <div
          style={{
            width: '100%',
            height: '100%',
            backgroundColor: 'white',
            position: 'absolute',
            top: 0,
            left: 0,
            transform: `scale(${circleScale})`,
          }}

**Recipe:**

1. **Opacity Animation**
	* Set the opacity to 0 at frame 100
	* Add a keyframe at frame 1 and set the opacity to 100
	* Use easing: 0% at frame 0, 100% at frame 1
2. **Rotation Animation**
	* Set the rotation to 0 at frame 0
	* Add a keyframe at frame 160 and set the rotation to 360
	* Use easing: 0% at frame 0, 100% at frame 160
3. **Morphing Animation**
	* Create a shape with the rounded rectangle tool
	* Set the size to 186 at frame 0
	* Add a keyframe at frame 15 and set the size to 186
	* Use easing: 0% at frame 0, 100% at frame 15
	* Change the color to black at frame 0
	* Add a keyframe at frame 15 and change the color to green
	* Use easing: 0% at frame 0, 100% at frame 15
4. **Bounce Effect**
	* Add multiple keyframes to the size animation
	* Increase the size at frame 0
	* Add a keyframe at frame 15 and decrease the size
	* Use easing: 0% at frame 0, 100% at frame 15
	* Add another keyframe at frame 30 and increase the size again
	* Use easing: 0% at frame 15, 100% at frame 30

**Settings:**

* Frame rate: 30fps
* Duration: 30 seconds
* Easing: ease-in, ease-out
* Motion blur: enabled
* Glow: enabled
* Transitions: enabled
* UI mockup handling: enabled
* Typography sizes/fonts: Arial, 24pt
* Background animation: enabled
* Sound: enabled

**Remotion Code:**

```javascript
import { interpolate, spring } from 'remotion';

const opacity = spring(0, { mass: 1, tension: 300, friction: 40 });
const rotation = spring(0, { mass: 1, tension: 300, friction: 40 });
const size = spring(186, { mass: 1, tension: 300, friction: 40 });
const color = spring('black', { mass: 1, tension: 300, friction: 40 });

const morphing = () => {
  const t = interpolate(0, 15, 1);
  const sizeValue = spring(size, { mass: 1, tension: 300, friction: 40 });
  const colorValue = spring(color, { mass: 1, tension: 300, friction: 40 });

  return (
    <div>
      <div
        style={{
          opacity: opacity(),
          rotation: rotation(),
          width: sizeValue(),
          height: sizeValue(),
          backgroundColor: colorValue(),
        }}
      />
    </div>
  );
};

const bounceEffect = () => {
  const t = interpolate(0, 15, 1);
  const sizeValue = spring(size, { mass: 1, tension: 300, friction: 40 });
  const colorValue = spring(color, { mass: 1, tension: 300, friction: 40 });

  return (
    <div>
      <div
        style={{
          opacity: opacity(),
          rotation: rotation(),
          width: sizeValue(),
          height: sizeValue(),
          backgroundColor: colorValue(),
        }}
      />
    </div>
  );
};

const animation = () => {
  return (
    <div>
      <div
        style={{
          opacity: opacity(),
          rotation: rotation(),
          width: size(),
          height: size(),
          backgroundColor: color(),
        }}
      />
      <div
        style={{
          opacity: opacity(),
          rotation: rotation(),
          width: bounceEffect(),
          height: bounceEffect(),
          backgroundColor: bounceEffect(),
        }}
      />
    </div>
  );
};
```

Note: This code is a simplified version of the recipe and may need to be adjusted to fit your specific use case.

**Recipe for Shape Morphing in After Effects**

1. **Shape Morphing from Circle to Square**
	* Create a circle shape and name it "middle circle".
	* Add keyframes for position and scale.
	* Create a new shape and name it "arc".
	* Use the pen tool to create a line with rounded corners.
	* Set the line cap to rounded.
	* Add keyframes for the arc's position and scale.
2. **Color Change**
	* Create a new shape and name it "color shape".
	* Use the shape morphing technique to change the color from green to black.
	* Add keyframes for the color shape's position and scale.
3. **Light Animation**
	* Create a new light layer and name it "light layer".
	* Use the light layer to focus on the arc.
	* Add keyframes for the light layer's position and scale.
4. **Text Animation**
	* Create two text layers and name them "text layer 1" and "text layer 2".
	* Use the text tool to write the text "ISS flyover" and "14 minutes".
	* Add keyframes for the text layers' position and scale.
5. **Satellite Animation**
	* Create a new shape and name it "satellite".
	* Use the shape morphing technique to change the satellite's size and color.
	* Add keyframes for the satellite's position and scale.
6. **Shape Morphing for Satellite**
	* Create a new shape and name it "satellite shape".
	* Use the shape morphing technique to change the satellite shape's size and roundness.
	* Add keyframes for the satellite shape's position and scale.
7. **Connected Text Animation**
	* Create a new text layer and name it "connected text".
	* Use the text tool to write the text "connected".
	* Add keyframes for the connected text's position and scale.

**Settings:**

* Keyframe timings:
	+ Position and scale keyframes: 0-100 frames
	+ Color shape keyframes: 50-100 frames
	+ Light layer keyframes: 50-100 frames
	+ Text layers keyframes: 50-100 frames
	+ Satellite keyframes: 50-100 frames
	+ Satellite shape keyframes: 50-100 frames
	+ Connected text keyframes: 50-100 frames
* Easing and graph editor values:
	+ Position and scale keyframes: ease-in-out
	+ Color shape keyframes: ease-in-out
	+ Light layer keyframes: ease-in-out
	+ Text layers keyframes: ease-in-out
	+ Satellite keyframes: ease-in-out
	+ Satellite shape keyframes: ease-in-out
	+ Connected text keyframes: ease-in-out
* Text animator setup:
	+ Text tool settings: font size 24, font family Arial
	+ Text layer 1 settings: text "ISS flyover", font size 24, font family Arial
	+ Text layer 2 settings: text "14 minutes", font size 24, font family Arial
* Masks:
	+ None
* Camera/null moves:
	+ None
* Motion blur:
	+ Enabled
* Glow:
	+ Enabled
* Transitions:
	+ None
* UI mockup handling:
	+ None
* Typography sizes/fonts:
	+ Font size 24, font family Arial
* Background animation:
	+ None
* Sound:
	+ None

**Reproducing in Remotion:**

To reproduce this animation in Remotion, you can use the following code:

```jsx
import { interpolate, spring } from 'remotion';

const shapeMorphing = (t) => {
  const circle = spring(t, { mass: 1, damping: 20 });
  const square = spring(t, { mass: 1, damping: 20 });
  const color = interpolate(t, [0, 1], ['green', 'black']);
  const light = spring(t, { mass: 1, damping: 20 });
  const text = spring(t, { mass: 1, damping: 20 });
  const satellite = spring(t, { mass: 1, damping: 20 });
  const satelliteShape = spring(t, { mass: 1, damping: 20 });
  const connectedText = spring(t, { mass: 1, damping: 20 });

  return {
    circle,
    square,
    color,
    light,
    text,
    satellite,
    satelliteShape,
    connectedText,
  };
};

export default function Comp() {
  const { circle, square, color, light, text, satellite, satelliteShape, connectedText } = shapeMorphing(0);

  return (
    <div>
      <div style={{ position: 'absolute', top: circle, left: circle, width: square, height: square, backgroundColor: color }} />
      <div style={{ position: 'absolute', top: light, left: light, width: 100, height: 100, backgroundColor: 'white' }} />
      <div style={{ position: 'absolute', top: text, left: text, width: 100, height: 100, backgroundColor:
