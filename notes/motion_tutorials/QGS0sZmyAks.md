# QGS0sZmyAks
(source: frame breakdown)

Unfortunately, the provided transcript appears to be a list of timestamps without any actual content. However, I can provide a general recipe for a motion design project in After Effects and then translate it to Remotion.

**After Effects Recipe:**

1. **Scene Setup**
	* Create a new composition with the following settings:
		+ Resolution: 1920x1080
		+ Frame Rate: 60fps
		+ Duration: 13 minutes (780 seconds)
	* Set the background color to a dark gray (#333333)
2. **Typography**
	* Create a new text layer with the following settings:
		+ Font: Open Sans
		+ Font Size: 48px
		+ Color: White (#FFFFFF)
	* Animate the text layer with the following settings:
		+ Ease: Ease In (0.25, 0.1)
		+ Keyframes:
			- 0s: Text layer appears at the top of the screen
			- 2s: Text layer moves down to the middle of the screen
			- 4s: Text layer moves up to the top of the screen
			- 6s: Text layer moves down to the middle of the screen
			- 8s: Text layer moves up to the top of the screen
			- 10s: Text layer moves down to the middle of the screen
			- 12s: Text layer moves up to the top of the screen
3. **Background Animation**
	* Create a new solid layer with the following settings:
		+ Color: Dark Gray (#333333)
	* Animate the solid layer with the following settings:
		+ Ease: Ease In (0.25, 0.1)
		+ Keyframes:
			- 0s: Solid layer appears at the top of the screen
			- 2s: Solid layer moves down to the middle of the screen
			- 4s: Solid layer moves up to the top of the screen
			- 6s: Solid layer moves down to the middle of the screen
			- 8s: Solid layer moves up to the top of the screen
			- 10s: Solid layer moves down to the middle of the screen
			- 12s: Solid layer moves up to the top of the screen
4. **Motion Blur**
	* Enable motion blur on all layers
5. **Glow**
	* Add a glow effect to the text layer with the following settings:
		+ Color: White (#FFFFFF)
		+ Size: 10px
		+ Softness: 50%
6. **Transitions**
	* Add a transition effect to the text layer with the following settings:
		+ Type: Fade In
		+ Duration: 0.5s
7. **UI Mockup**
	* Create a new composition with the following settings:
		+ Resolution: 1920x1080
		+ Frame Rate: 60fps
		+ Duration: 13 minutes (780 seconds)
	* Set the background color to a dark gray (#333333)
	* Add a UI mockup with the following settings:
		+ Font: Open Sans
		+ Font Size: 24px
		+ Color: White (#FFFFFF)
	* Animate the UI mockup with the following settings:
		+ Ease: Ease In (0.25, 0.1)
		+ Keyframes:
			- 0s: UI mockup appears at the top of the screen
			- 2s: UI mockup moves down to the middle of the screen
			- 4s: UI mockup moves up to the top of the screen
			- 6s: UI mockup moves down to the middle of the screen
			- 8s: UI mockup moves up to the top of the screen
			- 10s: UI mockup moves down to the middle of the screen
			- 12s: UI mockup moves up to the top of the screen

**Remotion Recipe:**

To reproduce this project in Remotion, you can use the following code:
```jsx
import { useRemotion } from 'remotion';
import { spring } from 'remotion-gsap';

const { lengthInFrames, framesPerSecond } = useRemotion();

const typography = {
  font: 'Open Sans',
  fontSize: 48,
  color: '#FFFFFF',
};

const uiMockup = {
  font: 'Open Sans',
  fontSize: 24,
  color: '#FFFFFF',
};

const background = {
  color: '#333333',
};

const animation = spring({
  from: 0,
  to: 1,
  duration: 2,
  ease: 'easeIn',
});

const typographyAnimation = spring({
  from: 0,
  to: 1,
  duration: 2,
  ease: 'easeIn',
});

const uiMockupAnimation = spring({
  from: 0,
  to: 1,
  duration: 2,
  ease: 'easeIn',
