# IBrgDq_96vA
(source: transcript)

**Recipe for the After Effects Animation**

1. **Composition Settings**
	* Resolution: 1920x1080
	* Title and Action Safe Guides: On
2. **Main Background Shape Layer**
	* Rounded Rectangle Tool: Draw a large rounded rectangle
	* Center Anchor Point: On
	* Align Shape Layer: Vertically and Horizontally
	* Roundness Value: 30
	* Fill Color: Dark Blue
	* Stroke Color: Brighter Dark Blue
	* Stroke Width: 2
	* Rename Shape Layer: Main Background
3. **Glow Effect**
	* Duplicate Main Background Shape Layer
	* Turn Off Fill Option
	* Add Glow Effect
	* Glow Radius Amount: 50
	* Add Second Glow Effect
	* Glow Amount: 30
	* Add Third Glow Effect
	* Glow Radius Amount: 20
4. **Trim Pads**
	* Add Trim Pads to Main Background Shape Layer
	* End Value: 12%
	* Offset Value: 16
5. **Rectangle One Settings**
	* Line Join: Round
	* Line Cap: Round
	* Taper Settings: Both Start and End Length to 50%, Start to 25%
6. **Color Gradient Effect**
	* Add Four Color Gradient Effect to Main Background Shape Layer
	* First Color Point: Dark Blue
	* Second and Third Color Points: Same as First Color Point
	* Fourth Color Point: Brighter Dark Blue
7. **Duplicate Main Background Layer**
	* Duplicate Main Background Layer
	* Move Anchor Point to Left Side
	* Scale Settings: First Scale Value to 96, Second Scale Value to 95
8. **Section of the Scene**
	* Duplicate Main Background Layer
	* Move Anchor Point to Left Side
	* Scale Settings: First Scale Value to 19
9. **Different Color**
	* Delete Four Color Gradient Effect
	* Fill Color: Dark High Contrast Blue
10. **Pen Tool**
	* Create a Straight Line from Here to Here in the Scene
	* Stroke Color: White
	* Stroke Width: 1
	* Rename Shape Layer: Line
	* Move Line to Right Side in Timeline
	* Opacity Settings: 30

**Reproducing the Animation in Remotion**

To reproduce the animation in Remotion, we need to write code that achieves the same effects. Here's a possible implementation:

```jsx
import { interpolate, spring } from 'remotion';

const MainBackground = () => {
  const [x, y] = usePosition();

  const mainBackgroundStyle = {
    position: 'absolute',
    top: `${y}px`,
    left: `${x}px`,
    width: '100%',
    height: '100%',
    borderRadius: '30px',
    backgroundColor: '#1a1d23',
    border: '2px solid #2f343f',
  };

  const glowStyle = {
    position: 'absolute',
    top: `${y}px`,
    left: `${x}px`,
    width: '100%',
    height: '100%',
    borderRadius: '30px',
    backgroundColor: '#2f343f',
    opacity: 0.3,
  };

  const trimPadStyle = {
    position: 'absolute',
    top: `${y}px`,
    left: `${x}px`,
    width: '100%',
    height: '100%',
    borderRadius: '30px',
    backgroundColor: '#2f343f',
    opacity: 0.3,
  };

  return (
    <div style={mainBackgroundStyle}>
      <div style={glowStyle}>
        <div style={trimPadStyle} />
      </div>
    </div>
  );
};

const SectionOfTheScene = () => {
  const [x, y] = usePosition();

  const sectionStyle = {
    position: 'absolute',
    top: `${y}px`,
    left: `${x}px`,
    width: '100%',
    height: '100%',
    borderRadius: '30px',
    backgroundColor: '#1a1d23',
    border: '2px solid #2f343f',
  };

  return (
    <div style={sectionStyle}>
      <div style={{ position: 'absolute', top: '0px', left: '0px', width: '100%', height: '100%', borderRadius: '30px', backgroundColor: '#2f343f', opacity: 0.3 }} />
    </div>
  );
};

const Line = () => {
  const [x, y] = usePosition();

  const lineStyle = {
    position: 'absolute',
    top: `${y}px`,
    left: `${x}px`,
    width: '100%',
    height: '1px',
    backgroundColor: '#ffffff',
    opacity: 0.3,
  };

  return (
    <div style={lineStyle} />
  );
};
```

This code uses the `remotion` library to create a composition with multiple layers, each with its own style and animation. The `usePosition` hook is used to get the current position of the composition, and the `interpolate` and `spring` functions are used to animate the

**Recipe for the Search Bar and Icons**

1. **Search Bar**
	* Create a rounded rectangle using the rounded rectangle tool.
	* Center the anchor point and zoom in on the search bar.
	* Add a gradient ram effect to the search bar:
		+ Set the first color to high contrast turquoise.
		+ Set the second color to dark low contrast blue.
	* Add a light sweep effect to the search bar:
		+ Set the sweep intensity to zero.
		+ Set the edge intensity to 40.
		+ Set the edge thickness to four.
		+ Set the width to 1,400.
	* Rename the layer to "search bar".
2. **Magnifier Icon**
	* Import the magnifier icon into the timeline.
	* Change the color of the icon to light purple using the change color effect:
		+ Set the first color to black.
		+ Set the second color to light purple.
		+ Set the hue amount to 100.
		+ Change the change by settings to transform into color.
		+ Set the option to hue, brightness, and saturation.
	* Mask the icon using the rectangle tool.
	* Center the anchor point and set the scale value to 22.
	* Place the icon on the left side of the search bar.
	* Rename the layer to "search icon".
3. **Search Text**
	* Select the type tool and change the font to inter light.
	* Set the font size to 14.
	* Change the color to light blue.
	* Write "search" in the scene.
	* Center the anchor point of the text and place it inside the search bar.

**Recipe for the Circle Shape Layers**

1. **Create Circle Shape Layers**
	* Create a small circle shape layer using the ellipse tool.
	* Select the darker blue color.
	* Duplicate the circle shape layer two more times and place them side by side.
	* Rename the layers to "top right one", "top right two", and "top right three".
2. **Add Gradient Rub Effect**
	* Copy the gradient rub effect from the search bar.
	* Paste it onto the circle shape layer.
	* Reposition the color points.
3. **Add Icons Inside Circle Shape Layers**
	* Select the magnifier icon created for the search bar.
	* Duplicate it and place it at the top of the timeline.
	* Zoom in and see which icon fits best for the new shape layers.
	* Select the icon using the rectangle tool.
	* Change its color to white and center the anchor point.
	* Place the icon inside the first circle shape layer.
	* Repeat the process for the second and third circle shape layers.

**Recipe for the Icons**

1. **Create Icons**
	* Duplicate the magnifier icon and remove the current mask.
	* Select the message icon using the rectangle tool.
	* Center the anchor point and place it inside the circle shape layer.
	* Duplicate one of the icons one more time.
	* Remove the current mask.
	* Grab the rectangle tool and mask the bell icon for the third button.
	* Place it inside the third shape layer.
2. **Rename Icons**
	* Rename the icons to "top right icon one", "top right icon two", and "top right icon three".

**Reproducing in Remotion**

To reproduce this design in Remotion, you can use the following code:

```jsx
import { interpolate, spring } from 'remotion';

const searchBar = () => {
  const [x, y] = spring([0, 0], { damping: 100 });
  const [width, height] = spring([100, 50], { damping: 100 });

  return (
    <g>
      <rect
        x={x}
        y={y}
        width={width}
        height={height}
        fill="linear-gradient(to bottom, #00bfff, #00008b)"
        rx={10}
      />
      <text
        x={x + 10}
        y={y + 20}
        fill="#ffffff"
        fontSize={14}
        textAnchor="start"
      >
        Search
      </text>
      <image
        x={x + 10}
        y={y + 30}
        width={20}
        height={20}
        src="magnifier-icon.png"
        fill="#ffffff"
      />
    </g>
  );
};

const circleShapeLayer = () => {
  const [x, y] = spring([0, 0], { damping: 100 });
  const [radius] = spring([10], { damping: 100 });

  return (
    <circle
      cx={x}
      cy={y}
      r={radius}
      fill="linear-gradient(to bottom, #00008b, #00008b)"
      rx={10}
    />
  );
};

const icons = () => {
  const [x, y] = spring([0, 0], { damping: 100 });
  const [width, height] = spring([20, 20], { damping: 100 });

  return (
    <g>
      <image
        x={x}
        y={y}
        width

**Recipe for the Main Part of the Scene:**

1. **Text Layer 1:**
	* Font: Inter Semibold
	* Font Size: 40
	* Tracking: -40
	* Text: "Welcome Alex"
	* Vertically aligned with the search bar
2. **Text Layer 2:**
	* Font: Inter Semibold
	* Font Size: 40
	* Tracking: -40
	* Text: "What can I do for you?"
	* Gradient Ramp Effect:
		+ First Color Point: Left side
		+ Second Color Point: Right side
		+ First Color: Bright Turquoise
		+ Second Color: More Saturated Turquoise
3. **Shape Layer 1:**
	* Rounded Rectangle Tool
	* Centered Anchor Point
	* Opacity: 60%
	* Drop Shadow Effect:
		+ Opacity: 100%
		+ Distance: 2
		+ Softness: 8
4. **Shape Layer 2:**
	* Duplicate Shape Layer 1
	* Place to the left of Shape Layer 1
	* Duplicate Shape Layer 2
	* Place to the right of Shape Layer 1
	* Shorten Shape Layer 2 by decreasing the first size value
5. **Icon Layers:**
	* Duplicate Magnifier Icon
	* Place on top of the timeline
	* Remove current mask
	* Change color to white
	* Mask icon with rectangle tool
	* Center anchor point
	* Place on third shape layer
	* Duplicate icon layers for second and third shape layers
	* Place icons inside shape layers
6. **Gut Lines:**
	* Create two gut lines to align icons
	* Place gut lines in the scene
7. **Button Names:**
	* Grab type tool
	* Select Intermedium font
	* Set font size to 15
	* Type "Profile" on shape layer
	* Center anchor point
	* Place text layer on shape layer

**Reproducing in Remotion:**

To reproduce this in Remotion, you would need to write code that achieves the same visual effects. Here's a possible implementation:

```jsx
import { spring } from 'remotion';

const textLayer1 = {
  font: 'Inter Semibold',
  fontSize: 40,
  tracking: -40,
  text: 'Welcome Alex',
  verticalAlign: 'center',
};

const textLayer2 = {
  font: 'Inter Semibold',
  fontSize: 40,
  tracking: -40,
  text: 'What can I do for you?',
  gradientRampEffect: {
    firstColorPoint: 'left',
    secondColorPoint: 'right',
    firstColor: '#1ABC9C',
    secondColor: '#03A9F4',
  },
};

const shapeLayer1 = {
  roundedRectangleTool: true,
  centeredAnchorPoint: true,
  opacity: 0.6,
  dropShadowEffect: {
    opacity: 1,
    distance: 2,
    softness: 8,
  },
};

const shapeLayer2 = {
  ...shapeLayer1,
  size: {
    width: 100,
    height: 100,
  },
};

const iconLayers = [
  {
    icon: 'magnifier',
    color: '#FFFFFF',
    mask: {
      type: 'rectangle',
      x: 0,
      y: 0,
      width: 100,
      height: 100,
    },
  },
  {
    icon: 'cloud',
    color: '#FFFFFF',
    mask: {
      type: 'rectangle',
      x: 0,
      y: 0,
      width: 100,
      height: 100,
    },
  },
];

const gutLines = [
  {
    x: 0,
    y: 0,
    width: 100,
    height: 1,
  },
  {
    x: 0,
    y: 0,
    width: 1,
    height: 100,
  },
];

const buttonNames = [
  {
    text: 'Profile',
    fontSize: 15,
    font: 'Inter Medium',
  },
];

export default function MainPartOfScene() {
  return (
    <div>
      <TextLayer1 {...textLayer1} />
      <TextLayer2 {...textLayer2} />
      <ShapeLayer1 {...shapeLayer1} />
      <ShapeLayer2 {...shapeLayer2} />
      {iconLayers.map((icon, index) => (
        <IconLayer key={index} {...icon} />
      ))}
      {gutLines.map((gutLine, index) => (
        <GutLine key={index} {...gutLine} />
      ))}
      {buttonNames.map((button, index) => (
        <ButtonName key={index} {...button} />
      ))}
    </div>
  );
}
```

Note that this is a simplified implementation and you may need to adjust the code to fit your specific use case. Additionally, you will need to define the `TextLayer1`, `TextLayer2`, `ShapeLayer1`, `Shape

**Recipe for the UI Design in After Effects:**

1. **Button Design:**
	* Create a text layer with the text "Settings"
	* Duplicate the text layer and place it inside the second shape layer
	* Rename the second shape layer and change the text to "Settings"
	* Duplicate the text layer again and place it in the scene, typing "Cloud" inside the button
	* Position the text layer carefully
	* Use gradient rum effects and apply it to the first button's shape layer
	* Place the gradient color points at the top left and bottom right
	* Select the first color (black) and change it to a bright turquoise color
	* Keep the second color as white
	* Set the shape layer's opacity to 100%
2. **Menu Section:**
	* Create a rounded rectangle shape layer with a roundness of 10 and center the anchor point
	* Import a profile picture into the composition
	* Place the profile picture inside the shape layer
	* Set the scale to 6 and move it to the left side of the shape layer
	* Remove the guideline
	* Fill in the shape layer with the type tool, setting the font size to 14 and changing the font to Interbolt
	* Type "Alex Walker" inside the shape layer
	* Adjust the position of the text layer
	* Create a new text layer with the text "Business Account" and set the font size to 10
	* Type the text inside the shape layer
	* Reposition the text layer to align it with the shape layer
3. **Open Button:**
	* Create a new shape layer using the pen tool
	* Set the stroke width to 2 and draw a small triangle shaped layer
	* Set the scale to 50 and place it in the scene
4. **Dashboard Button:**
	* Duplicate the shape layer and move it to the top of the scene
	* Make the duplicated shape layer thinner by reducing the first size value by 30%
	* Reposition the shape layer
	* Fill in the shape layer with the type tool, setting the font size to 15 and changing the color to white
	* Type "Home" inside the shape layer
	* Duplicate the text layer and add 50 to its second position value
	* Rename the duplicated text layer to "Dashboard" and change its color to blue
5. **Marketing, CRM, Integration, and Subscription Buttons:**
	* Repeat the process of duplicating the text layer, adding 50 to its second position value, and renaming it to the corresponding button name
6. **Preference Button:**
	* Duplicate the subscription text layer and move it slightly to the left
	* Type "Preference" in all caps
	* Set the font size to 10
	* Rename the text layer to "Preference"
7. **Settings and Filtering Buttons:**
	* Duplicate the text layer and add 50 to its second position value
	* Rename the duplicated text layer to "Settings" and "Filtering"
8. **Icons:**
	* Find the icon set layer in the timeline
	* Duplicate it and move it to the top of the scene
	* Grab the rectangle tool and mask the home icon
	* Place the icon to the left of the text layer
	* Rename the icon layer to the corresponding button name

**Reproducing the UI Design in Remotion:**

To reproduce the UI design in Remotion, you can use the following code:

```jsx
import { spring } from 'remotion';
import { interpolate } from 'remotion';

const homeIcon = {
  x: 0,
  y: 0,
  width: 100,
  height: 100,
};

const dashboardIcon = {
  x: 0,
  y: 0,
  width: 100,
  height: 100,
};

const marketingIcon = {
  x: 0,
  y: 0,
  width: 100,
  height: 100,
};

const crmIcon = {
  x: 0,
  y: 0,
  width: 100,
  height: 100,
};

const integrationIcon = {
  x: 0,
  y: 0,
  width: 100,
  height: 100,
};

const subscriptionIcon = {
  x: 0,
  y: 0,
  width: 100,
  height: 100,
};

const preferenceIcon = {
  x: 0,
  y: 0,
  width: 100,
  height: 100,
};

const settingsIcon = {
  x: 0,
  y: 0,
  width: 100,
  height: 100,
};

const filteringIcon = {
  x: 0,
  y: 0,
  width: 100,
  height: 100,
};

const homeText = {
  x: 0,
  y: 0,
  text: 'Home',
  fontSize: 14,
  color: 'white',
};

const dashboardText = {
  x: 0,
  y: 0,
  text: 'Dashboard',
  fontSize: 15,
  color: 'blue',
