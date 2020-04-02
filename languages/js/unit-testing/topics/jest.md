# Jest

- Unit Testing Framework
- Jest will set `process.env.NODE_ENV` to `'test'`
- `babel-jest` is automatically installed when installing Jest and automatically transform files if a babel configuration exists in project
- Jest supports TypeScript via Babel
- To run only one test with Jest, change `test` to `test.only`
- Jest executes all `describe` handlers in a test file before it executes any of the actual tests

## Jest Environment

- Jest + Babel
- Jest + Webpack

## Setup

- Install using `npm install --save-dev jest`
- Initialize jest configuration using `jest --init`
- Create simple test file under `root/__tests__/util.test.js`
- Execute test using `jest`

> - Jest looks for test files under `__tests__` folder
> - You might need to install jest globally if jest is not found

## Using Babel

- Install dependencies `npm install babel-jest @babel/core @babel/preset-env @babel/preset-typescript`
- Configure Babel

```js
presets: [
  "@babel/preset-env",
  {
    targets: {
      node: "current"
     }
   }
  ]
```
  
## Run jest on files matching pattern

> `jest my-file --notify --config==config.json`

- `--notify` is used to show popup when test execution is completed.
- `--config=config.json` is used to point to custom configuration files to override jest defaults.

## Testing Asynchronous Code

- Return the promise in case of asynchronous operations
  
### Callbacks

```js
test(`asynchronous test case`, done => {
  function callback(data) {
    try {
        except(data).toBe(`expected data`);
        done();
    }catch(error) {
        done(error);
    }
  }
  fetchData(callback);
  // The test does not complete until done is called
}));
```

### Promises

```js
test(`async Promise test case`, () => {
    return fetchData().then(data => { // return promise object
        expect(data).toBe('expected data');
    });
});

test(`async Promise reject test case`, () => {
    expect.assertions(1); // Important when expecting error
    return fetchData().catch(e => expect(e).toMatch(`error`));
});
```

### `.resolves` / `.rejects`

```js
test("resolves the response", () => {
    // return is important
    return expect(fetchData()).resolves.toBe('expected data');
});

test("fails with an error", () => {
    // return is important
    return expect(fetchData()).rejects.toBe('error');
});
```

### Async / Await

```js
test("async test case", async () => {
    const data = await fetchData();
    expect(data).toBe('expected data');;

    // OR
    await expect(fetchData()).resolves.toBe('expected data');
});

test("async test case fails", async () => {
    expect.assertions(1);
    try {
        await fetchData();
    } catch (e) {
        expect(e).toMatch('error');
    }

    // OR
    await expect(fetchData()).rejects.toThrow('error');
});
```

## Setup and Teardown

- `before...` / `after...` applies to file/describe scope
- `describe` is used to create test suit with a new scope

```js
beforeAll(() => {});
beforeEach(() => {});
afterEach(() => {});
afterAll(() => {});

describe('test suit', () => {
    test("test case", () => {

    })
});
```

## Mock Functions

- **Stub** creates dummy implementation
- **Mock** (Stub+) Helps to verify the method calls

Create mock `const mockFun = jest.fn(param => param * 2);`

> Reference: https://jestjs.io/docs/en/getting-started