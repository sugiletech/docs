# JavaScript Tech Dictionary

## A

---

### Assertion Library

- Verifies test results
- Eg: Chai, Should, Expect

## B

---

## C

---

### CheerIO

- Implements a subset of jQuery core
- Used to query DOM

## D

---

### `describe`

- Used to write **test suit**

## E

---

### Enzyme

- Testing utility for ReactJs
- Make it easier to assert, manipulate, traverse React Component's output

### `except`

- Part of assertion library **exposed by Jest**

## F

---

## G

---

## H

---

## I

---

### `it`

- Tags: #UnitTesting
- Used to define a test

## J

---

### Jest

- JavaScript **unit testing framework**
- Used by Facebook to test services and React application
- Test Runner + Assertion Library + Mocking Support
- Snapshot testing
- Looks for tests in a folder called \_\_tests\_\_
- Requires the `react-test-renderer` package to     render the component to JSON
- Execute `jest` command to run tests
- APIs: `describe`, `it`, `beforeEach`, `expect`, `jest.fn`
- Methods: `toEqual`, `toBe`, `toBeDefined`, `toContain`, `toBeCalled`
- Mock Methods: `mockImplementation`, `mockReturnValue`

### `jest.fn()`

- Creates mock function

### JSOM

- JavaScript implementation of DOM

## K

---

## L

---

## M

---

### Mocks

- Stub+
- Allows to inspect/verify calls to mock objects

### `mount`

- Tags: #UnitTesting #Enzyme #BehaviorTesting
- Full Rendering: renders nested component as well
- **Behavior Testing** is best perfomed by mounting the component

```js
const props = {onSubmit = jest.fn()}
const component = mount(<Welcome {...props} />);
const input = component.find('button').first();
const button = component.find('button').first();
input.simulate('change')({target: {value: 'sample'}});
button.simulate('click'); // Use native event for native elements. It does not work for custom components
expect(props.onSubmit).toBeCalledWith('sample');
```

## N

---

## O

---

## P

---

## Q

---

## R

---

### `react-test-renderer`

- Required by Jest to render component to JSON

```js
const renderer = require('react-test-renderer');
const component = renderer.create(<Link page="http://temp.org">Temp</Link>);
expect(component.toJSON()).toMatchSnapshot();
```

### React TestUtils

- Enable to render a react component, simulate an event

## S

---

### Shallow Rendering `shallow`

- Tags: #Enzyme #UnitTesting
- Does not render nested components so performant
- Used to isolate the component for unit testing
- Eg: `shallow(<Welcome />)`

### Snapshot Testing

- Alternate way to write tests without any assertions

### Stub

- Simulates dependencies

## T

---

### Test Runner (Tool)

- Picks-up unit test files
- Executes test cases
- Publish test results
- Eg: Mocha, Jasmine, Jest

## U

---

## V

---

## W

---

## X

---

## Y

---

## Z

---
