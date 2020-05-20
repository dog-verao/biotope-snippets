# biotope-snippets

This is a simple Biotope Snippets VS Code Extension, this is an unrelased package that will be published soon.

To start using this extension with Visual Studio Code copy it into the `<user home>/.vscode/extensions` folder and restart Code.

## Features

| Snippet       | Renders                             |
| ------------- |:-----------------------------------:|
| `bioel`       | Import Biotope/ Component           |
| `biop`        | Partial                             |
| `bioraw`      | Create Component with createRaw     |
| `bioattr`     | Attributes                          |
| `bioprops`    | Default props                       |
| `biostate`    | Define setState                     |
| `bioacc`      | Create attributeChangedCallback hook|
| `biocc`       | Create connectedCallback hook       |
| `bioren`      | Create rendered hook                |
| `biorea`      | Create ready hook                   |
| `biodcb`      | Create disconnectedCallback hook    |
| `bioatc`      | Create Attribute with converter     |
| `bioref`      | Create createRef hook               |

## Full Expansion

### bioel - Import Biotope/ Component   

```javascript
import Component from '@biotope/element';


export class ComponentName extends Component {
    render() {
        return this.html`

        `;
    }
}
ComponentName.componentName = 'custom-component';
ComponentName.register();
```

### biop - Partial
```javascript
const partial = () => this.html`

`; 
```

### bioraw - Create Component with createRaw
```javascript
import Component, { createRaw } from '@biotope/element';


export class ComponentName extends Component {
    render() {
        return this.html`
            this.createRaw()
        `;
    }
}
ComponentName.componentName = 'custom-component';
ComponentName.register();
```

### bioattr - Attributes 
```javascript
ComponentName.attributes = []
```

### bioprops - Default props 
```javascript
this.defaultProps = {
    props: 'My default props',
};
```

### biostate -  Define setState  
```javascript
this.setState({
    state: '',
});
```

### bioacc -  Create attributeChangedCallback hook 
```javascript
attributeChangedCallback(name, previous, current) {

};
```

### biocc -  Create connectedCallback hook
```javascript
connectedCallback() {

};
```

### biren -  Create rendered hook
```javascript
rendered() {

};
```

### birea -  Create ready hook
```javascript
ready() {

};
```

### biodcb -  Create disconnectedCallback hook
```javascript
disconnectedCallback() {

};
```

### bioatc -  Create Attribute with converter
```javascript
import Component, { toBoolean } from '@biotope/element';

ComponentName.attributes = [
    Attribute,
    {
        name: name,
        converter: (prop) => {
            return toBoolean(prop);
        },
    },
];
```
### bioref -  Create createRef hook
```javascript
this.refs = {
    ref: createRef(),
};
```