### Step 1: Setting up Flask

1. Create a new directory for your project and navigate to it in your terminal:
    ```bash
    mkdir healthcare && cd healthcare
    ```

2. Set up a virtual environment and activate it:
    ```bash
    python -m venv venv
    venv\Scripts\activate
    ```

3. Install Flask:
    ```bash
    pip install Flask
    ```

4. Create a new file named `app.py` and input the following code:
    ```python
    from flask import Flask, render_template

    app = Flask(__name__, static_folder="../frontend/build", static_url_path='/')

    @app.route('/')
    def index():
        return app.send_static_file('index.html')

    if __name__ == '__main__':
        app.run()
    ```

### Step 2: Setting up ReactJS

1. Outside the `healthcare` directory, generate a new React app:
    ```bash
    cd..
    npx create-react-app frontend
    ```

2. Move to the `frontend` directory:
    ```bash
    cd frontend
    ```

3. Replace the existing code in `src/App.js` with the following:
    ```javascript
    import React from 'react';

    function App() {
      return (
        <div className="App">
          <header className="App-header">
            <p>Health Care</p>
          </header>
        </div>
      );
    }

    export default App;
    ```

4. Build your React app:
    ```bash
    npm run build
    ```

### Step 3: Running the Application

1. Return to the `healthcare` directory:
    ```bash
    cd..
    cd healthcare
    ```

2. Initiate the Flask application:
    ```bash
    python app.py
    ```

Now, your Flask server should be active at `http://127.0.0.1:5000/`.