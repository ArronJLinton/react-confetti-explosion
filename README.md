# React Confetti Explosion

[![npm version](https://img.shields.io/npm/v/@reonomy/react-confetti-explosion.svg?style=flat-square)](https://www.npmjs.com/package/@reonomy/react-confetti-explosion)


This is inspired by [this](https://codepen.io/Gthibaud/pen/ENzXbp) beautiful and oft-used confetti which uses canvas, but equally inspired by how many bad looking CSS examples there are out there. The goal was to create a super lightweight confetti component that would not require canvas, use only CSS for animation, and could also be controlled as an explosion (rather than raining confetti), without the need to write a full-blown particle generator.


Install:

```bash
$ yarn add @reonomy/react-confetti-explosion
```


## Usage

```jsx
import ConfettiExplosion from '@reonomy/react-confetti-explosion';

function App() {
  const [isExploding, setIsExploding] = React.useState(false);
  return (
    <>
      {isExploding && <ConfettiExplosion />}
    </>
  );
}
```

## Optional Props:

```js
{
  particleCount?: number; // total number of particles used
  particleSize?: number; // size of particles in pixels (both squares and circles are generated)
  duration?: number; // duration of explosion in ms
  colors?: string[]; // array of any css-readable colors for particles
  force?: number; // 0-1 roughly the vertical force at which particles initially explode
  floorHeight?: number; // pixels the particles will vertically spread from initial explosion point
  floorWidth?: number; // pixels the particles will horizontally spread from initial explosion point
}
```

Although the duration of the explosion is controlled, it is up to the consumer how and when the `ConfettiExplosion` is rendered and positioned (and, hey, maybe even faded out?).

To keep the library as little as possible much of the physics have been estimated, cheapened, and downright mutilated. There are certainly prop combinations that will not look realistic, due to the limitations of CSS animations. But there should be enough options to fit most needs.

## Example Screenshots

### Big explosion:

![confetti-large-edit](https://user-images.githubusercontent.com/5460067/111782964-0c6bed80-8890-11eb-8a8b-0a4fdbc30cbd.gif)


### Little explosion:

![confetti-small-edit](https://user-images.githubusercontent.com/5460067/111782909-f8c08700-888f-11eb-9a90-4ef0931de730.gif)


### Tiny explosion:

![confetti-tiny](https://user-images.githubusercontent.com/5460067/111792596-c6685700-889a-11eb-8daf-7b234726041a.gif)


## Author

[herrethan](https://github.com/herrethan) and the [Reonomy Team](https://github.com/reonomy)

## License

MIT
