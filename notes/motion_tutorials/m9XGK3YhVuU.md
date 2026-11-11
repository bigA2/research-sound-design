# m9XGK3YhVuU
(source: transcript)

**Recipe for the After Effects Animation:**

1. **Gradient Background:**
	* Create a white solid (Ctrl + Y) and rename it to "Background".
	* Select the Pen Tool and set the color to the purple color (copy from the color palette).
	* Use the Pen Tool to create a gradient background.
2. **Text Animation:**
	* Create a new text layer and set the text to "Give your team super pars".
	* Apply a gradient to the text.
	* Animate the text to appear and move across the screen.
3. **Background Animation:**
	* Create a new solid layer and set the color to the background color (copy from the color palette).
	* Use the Pen Tool to create a brush stroke effect on the background.
	* Animate the background to move across the screen.
4. **Match Cut:**
	* Create a new solid layer and set the color to the background color (copy from the color palette).
	* Use the Pen Tool to create a rectangular shape.
	* Animate the rectangular shape to appear and move across the screen.
5. **Rectangular Rings:**
	* Create a new solid layer and set the color to the background color (copy from the color palette).
	* Use the Pen Tool to create a series of rectangular shapes.
	* Animate the rectangular shapes to appear and move across the screen.

**Keyframe Timings:**

* Background animation: 0-10 seconds (move across the screen)
* Text animation: 10-20 seconds (appear and move across the screen)
* Match Cut animation: 20-30 seconds (appear and move across the screen)
* Rectangular Rings animation: 30-40 seconds (appear and move across the screen)

**Easing/Graph Editor Values:**

* Background animation: Ease In (0-10 seconds), Ease Out (10-20 seconds)
* Text animation: Ease In (10-20 seconds), Ease Out (20-30 seconds)
* Match Cut animation: Ease In (20-30 seconds), Ease Out (30-40 seconds)
* Rectangular Rings animation: Ease In (30-40 seconds), Ease Out (40-50 seconds)

**Text Animator Setup:**

* Text layer: "Give your team super pars"
* Font: [insert font name]
* Font size: [insert font size]
* Color: [insert color]
* Gradient: [insert gradient]

**Masks:**

* None

**Camera/Null Moves:**

* None

**Motion Blur:**

* Enable motion blur on all layers

**Glow:**

* Enable glow on the text layer

**Transitions:**

* None

**UI Mockup Handling:**

* None

**Typography Sizes/Fonts:**

* Text layer: [insert font name], [insert font size]

**Background Animation:**

* Create a new solid layer and set the color to the background color (copy from the color palette).
* Use the Pen Tool to create a brush stroke effect on the background.
* Animate the background to move across the screen.

**Sound:**

* None

**Reproducing in Remotion:**

To reproduce this animation in Remotion, you will need to write code to achieve the same effects. Here is a possible implementation:

```jsx
import { interpolate, spring } from 'remotion';

const background = {
  x: 0,
  y: 0,
  width: 100,
  height: 100,
  color: '#ffffff',
};

const text = {
  x: 0,
  y: 0,
  width: 100,
  height: 100,
  color: '#000000',
  font: 'Arial',
  fontSize: 24,
  text: 'Give your team super pars',
};

const matchCut = {
  x: 0,
  y: 0,
  width: 100,
  height: 100,
  color: '#000000',
  font: 'Arial',
  fontSize: 24,
  text: 'Potential',
};

const rectangularRings = {
  x: 0,
  y: 0,
  width: 100,
  height: 100,
  color: '#000000',
  font: 'Arial',
  fontSize: 24,
  text: '10X Better Feedback',
};

function Background() {
  const frame = useCurrentFrame();
  const x = spring(background.x, frame / 10);
  const y = spring(background.y, frame / 10);
  const width = spring(background.width, frame / 10);
  const height = spring(background.height, frame / 10);
  const color = interpolate(frame, [0, 10], ['#ffffff', '#000000']);

  return (
    <div
      style={{
        position: 'absolute',
        top: y,
        left: x,
        width,
        height,
        backgroundColor: color,
      }}
    />
  );
}

function Text() {
  const frame = useCurrentFrame();
  const x = spring(text.x, frame / 10);
  const y = spring(text.y, frame / 10);
  const width = spring(text.width, frame / 10);
  const height = spring(text.height, frame / 10);
  const color = interpolate(frame

**Recipe for the Gradient Stroke Animation in After Effects:**

1. **Color Palette:**
	* Copy the color palette from the given source.
	* Paste it into the color palette in After Effects.
2. **Stroke Animation:**
	* Draw a stroke with the Pen tool.
	* Disable the fill completely.
	* Add a trim path to the stroke.
	* Set the end amount to animate the stroke.
	* Apply keyframes to the start and end of the stroke.
	* Ease the animation to make it faster in the beginning.
3. **Stroke Width Animation:**
	* Duplicate the stroke layer.
	* Name the duplicate layer "Gradient Stroke Two".
	* Paste a new color into the stroke.
	* Remove the keyframes for the stroke width.
	* Animate the start of the trim path instead of the end.
	* Apply keyframes to the start and end of the trim path.
	* Ease the animation to make it smooth.
4. **Blur Effect:**
	* Use the Fast Box Blur effect in the FX Console.
	* Increase the blur radius to achieve the desired effect.
	* Reduce the stroke width to make the blur visible.
5. **Animation:**
	* Duplicate the stroke layer to create a second gradient.
	* Animate the start of the second gradient to create a smooth transition.
	* Adjust the position of the second gradient to achieve the desired effect.

**Reproducing the Animation in Remotion:**

To reproduce the animation in Remotion, you can use the following code:

```jsx
import { spring } from 'remotion';
import { interpolate } from 'remotion';

const strokeStart = spring(0, { mass: 1, damping: 100 });
const strokeEnd = spring(100, { mass: 1, damping: 100 });

const strokeWidth = interpolate(strokeStart, [0, 100], [10, 50]);

const blurRadius = interpolate(strokeStart, [0, 100], [0, 50]);

const gradientStrokeTwoStart = spring(0, { mass: 1, damping: 100 });
const gradientStrokeTwoEnd = spring(100, { mass: 1, damping: 100 });

const gradientStrokeTwoWidth = interpolate(gradientStrokeTwoStart, [0, 100], [10, 50]);

return (
  <div>
    <svg>
      <path
        d="M 0 0 L 100 100"
        stroke="#ff0000"
        strokeWidth={strokeWidth}
        fill="none"
        strokeMiterlimit="10"
        strokeDasharray="10 10"
        strokeDashoffset={strokeEnd}
        strokeLinecap="round"
      />
      <path
        d="M 0 0 L 100 100"
        stroke="#00ff00"
        strokeWidth={gradientStrokeTwoWidth}
        fill="none"
        strokeMiterlimit="10"
        strokeDasharray="10 10"
        strokeDashoffset={gradientStrokeTwoEnd}
        strokeLinecap="round"
      />
    </svg>
  </div>
);
```

This code uses the `spring` function from Remotion to animate the start and end of the stroke, and the `interpolate` function to animate the stroke width and blur radius. The `strokeDashoffset` property is used to animate the stroke dash offset, creating the gradient effect.

**Recipe for the After Effects SaaS Tutorial**

**Layer 1: "cramble this layer"**

* Keyframe 1: 
  - Time: 0s
  - Position: (0, 0)
  - Ease: 0%
* Keyframe 2: 
  - Time: 10s
  - Position: (0, 100)
  - Ease: 0%
* Keyframe 3: 
  - Time: 20s
  - Position: (0, 0)
  - Ease: 0%

**Layer 2: "Let's do it from here"**

* Keyframe 1: 
  - Time: 0s
  - Position: (0, 0)
  - Ease: 0%
* Keyframe 2: 
  - Time: 30s
  - Position: (100, 0)
  - Ease: 0%
* Keyframe 3: 
  - Time: 40s
  - Position: (0, 0)
  - Ease: 0%

**Layer 3: "Let's push it down a little bit"**

* Keyframe 1: 
  - Time: 0s
  - Position: (0, 0)
  - Ease: 0%
* Keyframe 2: 
  - Time: 50s
  - Position: (0, -100)
  - Ease: 0%
* Keyframe 3: 
  - Time: 60s
  - Position: (0, 0)
  - Ease: 0%

**Layer 4: "Over here"**

* Keyframe 1: 
  - Time: 0s
  - Position: (0, 0)
  - Ease: 0%
* Keyframe 2: 
  - Time: 70s
  - Position: (200, 0)
  - Ease: 0%
* Keyframe 3: 
  - Time: 80s
  - Position: (0, 0)
  - Ease: 0%

**Layer 5: "Let's push this forward a little bit"**

* Keyframe 1: 
  - Time: 0s
  - Position: (0, 0)
  - Ease: 0%
* Keyframe 2: 
  - Time: 90s
  - Position: (0, 100)
  - Ease: 0%
* Keyframe 3: 
  - Time: 100s
  - Position: (0, 0)
  - Ease: 0%

**Text Layer**

* Font: Arial
* Font Size: 24
* Color: Black
* Text: "Let's type give"
* Animation:
  - Keyframe 1: 
    - Time: 0s
    - Position: (0, 0)
    - Ease: 0%
  - Keyframe 2: 
    - Time: 110s
    - Position: (0, -100)
    - Ease: 0%
  - Keyframe 3: 
    - Time: 120s
    - Position: (0, 0)
    - Ease: 0%

**Background Animation**

* Layer: "Background"
* Animation:
  - Keyframe 1: 
    - Time: 0s
    - Position: (0, 0)
    - Ease: 0%
  - Keyframe 2: 
    - Time: 130s
    - Position: (200, 0)
    - Ease: 0%
  - Keyframe 3: 
    - Time: 140s
    - Position: (0, 0)
    - Ease: 0%

**Sound**

* Layer: "Sound"
* Audio File: "music.mp3"
* Animation:
  - Keyframe 1: 
    - Time: 0s
    - Volume: 0
    - Ease: 0%
  - Keyframe 2: 
    - Time: 150s
    - Volume: 100
    - Ease: 0%
  - Keyframe 3: 
    - Time: 160s
    - Volume: 0
    - Ease: 0%

**Reproducing in Remotion**

```javascript
import { spring } from 'remotion';

const animation = () => {
  const x = spring(0, { mass: 1, tension: 300, friction: 40 });
  const y = spring(0, { mass: 1, tension: 300, friction: 40 });

  const keyframes = [
    { time: 0, x: 0, y: 0 },
    { time: 10, x: 0, y: 100 },
    { time: 20, x: 0, y: 0 },
    { time: 30, x: 100, y: 0 },
    { time: 40, x: 0, y: 0 },
    { time: 50, x: 0, y: -100 },
    { time:

**Recipe for the After Effects Animation:**

1. **Text Animation:**
	* Font: Helvetica
	* Text size: varies (not specified)
	* Text animator setup:
		+ Position animator: ramp up animation
		+ Keyframe offset: 100%
		+ Advance: more options
		+ Shape: select the shape and animate from one point to another
	* Keyframe offset: -100 to complete the offset
2. **Scale Animation:**
	* Keyframe timings: 0s, 10s, 20s, 30s
	* Easing/graph editor values: ease-in, ease-out
	* Text animator setup:
		+ Scale animator: apply keyframe to scale
		+ Keyframe timings: 0s, 10s, 20s, 30s
		+ Easing/graph editor values: ease-in, ease-out
3. **Motion Blur:**
	* Motion blur: enabled
	* Blur type: radial
	* Blur amount: 50%
4. **Glow:**
	* Glow: enabled
	* Glow color: white
	* Glow amount: 50%
5. **Transitions:**
	* None specified
6. **UI Mockup Handling:**
	* None specified
7. **Background Animation:**
	* None specified
8. **Sound:**
	* None specified

**Reproducing the Animation in Remotion:**

To reproduce the animation in Remotion, you can use the following code:

```jsx
import { spring } from 'remotion';

const textAnimator = spring({
  from: 0,
  to: 100,
  duration: 10,
  easing: spring.easing.easeInOut,
});

const scaleAnimator = spring({
  from: 0,
  to: 100,
  duration: 10,
  easing: spring.easing.easeInOut,
});

const motionBlur = spring({
  from: 0,
  to: 50,
  duration: 10,
  easing: spring.easing.easeInOut,
});

const glow = spring({
  from: 0,
  to: 50,
  duration: 10,
  easing: spring.easing.easeInOut,
});

const text = (
  <Text
    text="Hello World"
    style={{
      fontSize: 24,
      fontFamily: 'Helvetica',
      textShadow: '0px 0px 10px rgba(0, 0, 0, 0.5)',
    }}
  />
);

const scale = (
  <Scale
    scale={scaleAnimator}
    style={{
      transition: 'all 0.1s ease-in-out',
    }}
  />
);

const motionBlurEffect = (
  <MotionBlur
    blurAmount={motionBlur}
    style={{
      transition: 'all 0.1s ease-in-out',
    }}
  />
);

const glowEffect = (
  <Glow
    glowAmount={glow}
    style={{
      transition: 'all 0.1s ease-in-out',
    }}
  />
);

const background = (
  <Background
    style={{
      transition: 'all 0.1s ease-in-out',
    }}
  />
);

const uiMockup = (
  <UI
    style={{
      transition: 'all 0.1s ease-in-out',
    }}
  />
);

const sound = (
  <Sound
    style={{
      transition: 'all 0.1s ease-in-out',
    }}
  />
);

const animation = (
  <Group>
    {text}
    {scale}
    {motionBlurEffect}
    {glowEffect}
    {background}
    {uiMockup}
    {sound}
  </Group>
);

export default function HelloWorld() {
  return (
    <RemotionCanvas>
      {animation}
    </RemotionCanvas>
  );
}
```

Note that this code is a simplified version of the original animation and may not exactly replicate the original animation. You may need to adjust the code to match the specific requirements of your animation.
