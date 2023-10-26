## Adding a navigation bar 
* Update your `frontend/src/App.js` file. 

```javascript
import React from 'react';

function App() {
  return (
    <div className="App">
      <nav className="App-nav">
        <ul>
          <li><a href="/">Home</a></li>
          <li><a href="/about">About</a></li>
          <li><a href="/contact">Contact</a></li>
        </ul>
      </nav>
      <header className="App-header">
        <p>HealthCare</p>
      </header>
    </div>
  );
}

export default App;
```

In this revised version:

1. A `nav` element has been introduced which encloses an unordered list (`ul`) containing three list items (`li`).
2. Each list item contains an anchor tag (`a`) which represents a link to a different page on your website (in this example, the Home, About, and Contact pages).
3. The `className` attributes are used to allow for styling via CSS, which you can add to your `src/App.css` file to customize the appearance of the navbar and other elements on your page.