# Enzyme

- Testing utility for ReactJs
- Make it easier to assert, manipulate, traverse React Component's output
- React TestUtils + JSON + CheerIO
- **NOT** a unit testing framework 
- Excludes Test Runner, Assertion Library
- not opinionated
- can be used within Jest
- Quite useful to write tests using assertions
- Does not allow to change the value of input elements. The `simulate` method is useful to simulate user actions.
- APIs: `shallow`, `mount`, `render`
- Querying Nodes: `find`, `findWhere`, `some`, `someWhere`, `first`, `at`, `html`, `text`
- Interaction: `simulate`, `setProps`, `setState`, `setContext`, `props()`, `props(key)`, `state(key)`, `context(key)`

```js
import { shallow} from 'enzyme'
const component = shallow(<Welcome />);
except(welcome.find('div').text()).toEqual("Hello world");
```
