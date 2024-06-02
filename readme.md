# mongo-oid



[![NPM](https://img.shields.io/npm/v/react-swipeable-button.svg)](https://www.npmjs.com/package/react-swipeable-button)
[![install size](https://packagephobia.com/badge?p=react-swipeable-button)](https://packagephobia.com/result?p=react-swipeable-button)
[![npm bundle size](https://img.shields.io/bundlephobia/minzip/react-swipeable-button?style=flat-square)](https://bundlephobia.com/package/react-swipeable-button@latest)[![npm downloads](https://img.shields.io/npm/dm/react-swipeable-button.svg?style=flat-square)](https://npm-stat.com/charts.html?package=react-swipeable-button)

### A package to generate 12 bytes Hex String for MongoDB Object Id

 `Updates:`
* Typescript Support Added

## Install

```bash
npm install mongo-oid
```

or

```bash
yarn add mongo-oid
```

## Usage

### Just import oid() function from 'mongo-oid'

 Below is the Example use case for upserting Data. (Update if id exists or create with the following Object Id)

```tsx
import { oid } from "mongo-oid";

function From({user}:{user?:UserType}) {

  const [doc, setDoc] = useState<{
    id: string;
    name: string;
    }>({
    id: user ? user.id : oid(),
    name:user ? user.name : ''
    })

console.log(oid())
// "f2a1b3c4d5e6a7b8c9d0e1f2"

  return (
       <button onClick={Upsert}>
        Update Or Create
        </button>
  );
}

export default Form;
```

## Contribution

Contributing on this project is always welcome! Just fork, update, push to your respective branch and make a pull request after testing. Make sure to open an issue before contribute.


## License

MIT © [Abdur Rahman](https://github.com/abdurrahman720)
