# React Confetti Explosion

<!-- [![npm version](https://img.shields.io/npm/v/@reonomy/styles.svg?style=flat-square)](https://www.npmjs.com/package/@reonomy/styles) -->


This is inspired by [this](https://codepen.io/Gthibaud/pen/ENzXbp) beautiful and oft-used confetti which uses canvas, but equally inspired by how many bad looking CSS examples there are out there. The goal was to create a super lightweight confetti component that would not require canvas, and could also be controlled as an explosion (rather than raining confetti), without the need to write a full-blown particle generator.


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

Optional Props:

```js
{
  particleCount?: number; // total number of particles used
  particleSize?: number; // size of particles in pixels
  duration?: number; // full length of explosion in ms
  colors?: string[]; // array of colors for particles
  force?: number; // 0-1 roughly the vertical force at which particles initially explode
  floorHeight?: number; // pixels the particles will vertically spread from initial explosion point
  floorWidth?: number; // pixels the particles will horizontally spread from initial explosion point
}
```

Although the duration of the explosion is controlled, it is up to the consumer how and when the `ConfettiExplosion` is rendered and positioned (and, hey, maybe even faded out?).

To keep the library as little as possible much of the physics have been estimated, cheapened, and downright mutilated. There are certainly prop combinations that will not look realistic, due to the limitations of CSS animations. But there should be enough options to fit your needs.

## Example Screenshots


## Author

[Reonomy Team](https://github.com/reonomy)

## License

MIT
