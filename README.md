# react-common-interview-questions
I'll provide common ReactJS interview questions in major areas of developing Single Page Applications (SPA) for a senior developer, along with answers and code examples. I'll also translate it into Urdu.

### 1. **Architecture:**

#### Q: Explain the concept of virtual DOM in React.

A: Virtual DOM is a lightweight copy of the real DOM that React keeps in memory. React uses it to efficiently update the UI by minimizing direct manipulation of the actual DOM. Changes are first made to the virtual DOM, and then React calculates the difference (diffing) between the virtual DOM and the real DOM, updating only the necessary parts.

```jsx
// Example
const element = <h1>Hello, World!</h1>;
const container = document.getElementById('root');
ReactDOM.render(element, container);
```

#### Urdu Translation:
ری ایکٹ میں ورچوئل ڈوم کا تصورکیا ہے؟؟

**جواب:**
ویرچوآل ڈوم ایک وزن کم نسخہ ہے جو ریئل ڈوم کی اصل کاپی ہے جو ری ایکٹ میں یاد رکھا جاتا ہے۔ ری ایکٹ اسے یوآئی کو فعالانے کیلئے ایک نفع بخش طریقے سے استعمال کرتا ہے۔ تبدیلیاں پہلے ورچوآل ڈوم میں ہوتی ہیں، اور پھر ری ایکٹ ورچوآل ڈوم اور ریئل ڈوم کے درمیان فرق (ڈفنگ) کا حساب لگاتا ہے، صرف ضروری حصوں کو اپ ڈیٹ کرتا ہے۔

```jsx
// مثال
const element = <h1>ہیلو، ورلڈ!</h1>;
const container = document.getElementById('root');
ReactDOM.render(element, container);
```

### 2. **Development Life Cycle:**

#### Q: Describe the React component lifecycle methods.

A: React component lifecycle methods are methods that get called at different stages of a component's life. They include `componentDidMount`, `componentDidUpdate`, and `componentWillUnmount`. For example, `componentDidMount` is called after the component is rendered to the DOM.

```jsx
class MyComponent extends React.Component {
  componentDidMount() {
    console.log('Component is mounted!');
  }

  componentDidUpdate() {
    console.log('Component is updated!');
  }

  componentWillUnmount() {
    console.log('Component is unmounted!');
  }

  render() {
    return <div>Hello, World!</div>;
  }
}
```

#### Urdu Translation:
Q: ری ایکٹ کمپوننٹ لائف سائیکل میتھڈز کو تفصیل سے بیان کریں۔

**جواب:**
ری ایکٹ کمپوننٹ لائف سائیکل میتھڈز وہ میتھڈز ہیں جو کسی کمپوننٹ کے زندگی کے مختلف مراحل میں بلایے جاتے ہیں۔ ان میں `componentDidMount`، `componentDidUpdate`، اور `componentWillUnmount` شامل ہیں۔ مثال کے طور پر، `componentDidMount` وہ وقت ہے جب کمپوننٹ ڈوم پر رینڈر ہو جاتا ہے۔

```jsx
class MyComponent extends React.Component {
  componentDidMount() {
    console.log('Component is mounted!');
  }

  componentDidUpdate() {
    console.log('Component is updated!');
  }

  componentWillUnmount() {
    console.log('Component is unmounted!');
  }

  render() {
    return <div>ہیلو، ورلڈ!</div>;
  }
}
```

### 3. **Integration with AWS DB and Backend Lambda APIs:**

#### Q: How do you integrate React with AWS Lambda for backend functionality?

A: You can use the `fetch` API or libraries like `axios` to make HTTP requests to AWS Lambda functions. Here's an example using `fetch`:

```jsx
async function fetchData() {
  const response = await fetch('YOUR_AWS_LAMBDA_API_ENDPOINT');
  const data = await response.json();
  console.log('Data from AWS Lambda:', data);
}

fetchData();
```

#### Urdu Translation:
Q: ری ایکٹ کو ای ڈبلیو ایس لیمبڈا کے ساتھ بیکینڈ فعلیت کے لیے انٹیگریٹ کیسے کریں؟

**جواب:**
آپ `fetch` API یا `axios` جیسی لائبریریوں کا استعمال کرکے AWS لیمبڈا فعلوں کے لیے ایچ ٹی ٹی پی درخواستیں بنا سکتے ہیں۔ یہاں `fetch` کا استعمال کرکے ایک مثال ہے۔

```jsx
async function fetchData() {
  const response = await fetch('آپکا_AWS_LAMBDA_API_ENDPOINT');
  const data = await response.json();
  console.log('AWS لیمبڈا سے ڈیٹا:', data);
}

fetchData();
```

### 4. **Authentication and Authorization:**

#### Q: How can you implement user authentication in a React SPA?

A: You can use libraries like `Firebase` or `Auth0` for authentication. Here's an example using `Firebase`:

```jsx
import { useState } from 'react';
import firebase from '
````
## In Urdu
Here are common interview questions for a senior React developer, translated into Urdu, covering core concepts such as architecture, development lifecycle, integration with AWS, authentication and authorization, data flow, controlled and pure functions, and state management. 

### 1. React Architecture کیا ہے؟
**سوال:** React کی آرکیٹیکچر کیا ہے؟

**جواب:** React کی آرکیٹیکچر بنیادی طور پر کمپوننٹس پر مبنی ہے۔ ہر کمپوننٹ اپنی حالت (state) اور پراپرٹیز (props) کو منظم کرتا ہے۔ React میں، "Virtual DOM" کا استعمال کیا جاتا ہے تاکہ ویب ایپلیکیشن کی کارکردگی بہتر بنائی جا سکے۔ یہاں ایک سادہ مثال ہے:

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

### 2. React Development Life Cycle کیا ہے؟
**سوال:** React Development Life Cycle کیا ہے؟

**جواب:** React کا Development Life Cycle تین اہم مراحل میں تقسیم ہوتا ہے: Mounting, Updating, اور Unmounting۔ ہر مرحلے میں مخصوص لائف سائیکل میتھڈز ہوتے ہیں۔ مثال کے طور پر:

```jsx
class MyComponent extends React.Component {
  componentDidMount() {
    // Code to run after the component mounts
  }

  componentDidUpdate(prevProps, prevState) {
    // Code to run after the component updates
  }

  componentWillUnmount() {
    // Code to run before the component unmounts
  }
}
```

### 3. AWS DB اور Backend Lambda APIs کے ساتھ React کی Integration کیسے کی جاتی ہے؟
**سوال:** React کو AWS DB اور Lambda APIs کے ساتھ کیسے جوڑا جا سکتا ہے؟

**جواب:** React ایپلیکیشن میں AWS Lambda APIs کے ساتھ بات چیت کرنے کے لیے آپ `fetch` یا `axios` کا استعمال کر سکتے ہیں۔ مثال کے طور پر:

```jsx
import axios from 'axios';

function fetchData() {
  axios.get('https://example.com/api/data')
    .then(response => {
      console.log(response.data);
    })
    .catch(error => {
      console.error('There was an error!', error);
    });
}
```

### 4. Authentication اور Authorization کو React میں کیسے Implement کیا جاتا ہے؟
**سوال:** React میں Authentication اور Authorization کو کیسے Implement کیا جاتا ہے؟

**جواب:** Authentication اور Authorization کے لیے آپ JWT ٹوکن یا کسی دوسرے طریقے کا استعمال کر سکتے ہیں۔ یہاں ایک سادہ مثال ہے:

```jsx
// Login function
function loginUser(credentials) {
  return axios.post('https://example.com/api/login', credentials)
    .then(response => {
      localStorage.setItem('token', response.data.token);
    });
}

// Checking authentication
function isAuthenticated() {
  return !!localStorage.getItem('token');
}
```

### 5. Data Flow React میں کیسے کام کرتا ہے؟
**سوال:** React میں Data Flow کیسے کام کرتا ہے؟

**جواب:** React میں Data Flow ہمیشہ Parent سے Child کمپوننٹس کی طرف ہوتا ہے، جسے One-Way Data Binding کہا جاتا ہے۔ Parent کمپوننٹ Child کمپوننٹ کو props کے ذریعے ڈیٹا بھیجتا ہے۔

```jsx
function ParentComponent() {
  const data = 'Hello from Parent';
  return <ChildComponent data={data} />;
}

function ChildComponent(props) {
  return <h1>{props.data}</h1>;
}
```

### 6. Controlled اور Pure Functions کیا ہیں؟
**سوال:** Controlled اور Pure Functions کیا ہیں؟

**جواب:** Controlled Components وہ ہیں جن میں فارم کے انپوٹ کی حالت کو React کے ذریعہ منظم کیا جاتا ہے۔ Pure Functions ایسی فنکشنز ہیں جو ہمیشہ ایک ہی انپوٹ کے لیے ایک ہی آؤٹ پٹ دیتی ہیں اور ان کے پاس کوئی سائیڈ افیکٹس نہیں ہوتے۔

**Controlled Component Example:**

```jsx
class MyForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = { value: '' };
  }

  handleChange = (event) => {
    this.setState({ value: event.target.value });
  };

  render() {
    return <input type="text" value={this.state.value} onChange={this.handleChange} />;
  }
}
```

**Pure Function Example:**

```jsx
function add(a, b) {
  return a + b;
}
```

### 7. State Management React میں کیسے کیا جاتا ہے؟
**سوال:** React میں State Management کیسے کیا جاتا ہے؟

**جواب:** State Management کے لیے آپ React کی داخلی state، Context API، یا کسی state management لائبریری جیسے Redux کا استعمال کر سکتے ہیں۔ Redux کی مثال:

```jsx
// Redux action
const increment = () => ({
  type: 'INCREMENT'
});

// Redux reducer
const counter = (state = 0, action) => {
  switch (action.type) {
    case 'INCREMENT':
      return state + 1;
    default:
      return state;
  }
};

// Redux store
const store = createStore(counter);

// React component connected to Redux store
function Counter() {
  const count = useSelector(state => state);
  const dispatch = useDispatch();
  
  return (
    <div>
      <h1>{count}</h1>
      <button onClick={() => dispatch(increment())}>Increment</button>
    </div>
  );
}
```

یہ سوالات اور جوابات آپ کو senior React developer کے انٹرویو کی تیاری میں مدد دیں گے۔
