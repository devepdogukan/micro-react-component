# micro-react-component

## Description
`micro-react-component` is a project designed to create modular React components based on a micro frontend architecture. This project allows different parts of applications to come together to form a flexible and scalable structure.

[![NPM](https://img.shields.io/npm/v/micro-react-component)](https://www.npmjs.com/package/micro-react-component) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/devepdogukan/micro-react-component)

## Features
- Modular structure: Components can be developed and deployed independently.
- React-based: Optimized for modern React applications.
- Micro Frontend compatible: Enables collaboration between different teams and projects.
- **Tailwind CSS support**: Tailwind CSS is used to style user interface components.
- **TypeScript support**: The project is written in TypeScript, providing type safety and an improved development experience.
- **Testing environment**: The project is tested using Jest, ensuring the accuracy and reliability of components.

## Installation
To run the project in your local environment, follow the steps below:

1. Clone this repository:
   ```bash
   git clone https://github.com/devepdogukan/micro-react-component.git
   ```

2. Navigate to the project directory:
   ```bash
   cd micro-react-component
   ```

3. Install the necessary dependencies:
   ```bash
   pnpm install
   ```

4. Start the development server:
   ```bash
   pnpm start
   ```

## Configuration
In the `webpack.config.js` file, you can update the following settings for the `ModuleFederationPlugin` configuration:

| Setting       | Description                                                                                              |
|------------|-------------------------------------------------------------------------------------------------------|
| `name`     | Specifies the name of the application. This name will be used by other micro frontend applications.   |
| `port`     | Specifies the port number on which the application will run. It should be unique to avoid conflicts with other micro frontend applications. |
| `filename` | Specifies the name of the file to be exposed by the application. Other micro frontend applications can use this file to access components. |
| `exposes`  | An object that defines the components that can be used by other micro frontend applications. Each component is specified with a key and the corresponding file path. |

```javascript
new ModuleFederationPlugin({
  name: 'microReactComponent',
  filename: 'remoteEntry.js',
  exposes: {
    './Component': './src/Component',
  },
}),
```

