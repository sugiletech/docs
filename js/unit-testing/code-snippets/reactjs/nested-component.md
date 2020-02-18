# ReactJS Nested Components Testing

```js
const component = shallow(<Parent />);

except(component.find('Child1').length).toEqual();
except(component.find('Child2').length).toEqual();

const child1 = component.find('Child').first();
child1.props().onAction('data 1'); //Trigger event from child
component.update();
const child2 = component.find('Child2').first();
expect(child2.props().date.length).toEqual(1);
except(child2.props().date[0].toEqual('data 1'); //Child updates data in state used by Child2
```