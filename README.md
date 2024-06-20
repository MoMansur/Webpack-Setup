# My First Webpack Setup

Welcome to my first Webpack setup! This repository contains the basic configuration and folder structure I used to get started with Webpack.

## Introduction

Webpack is a powerful module bundler for JavaScript applications. It helps in bundling all your scripts, styles, and assets into a single package, making your development process smoother and more efficient.

This project demonstrates my initial setup and configuration of Webpack, providing a simple example to help others get started.

## Folder Structure

- **dist/**: This folder contains the output files generated by Webpack. The `index.html` file is where the bundled scripts are injected.
- **src/**: This folder contains the source files for the project.
  - `index.js`: The main JavaScript file.
  - `style.css`: The main CSS file.
- **package.json**: This file contains the project's metadata and dependencies.
- **webpack.config.js**: This file contains the configuration settings for Webpack.
- **README.md**: This file contains information about the project.

## Setup Instructions

To get started with this Webpack setup, follow these steps:

1. **Clone the repository:**
    ```sh
    git clone  https://github.com/MoMansur/Webpack-Setup
    cd my-webpack-project
    ```

2. **Install dependencies:**
    ```sh
    npm install
    ```

3. **Run Webpack:**
    ```sh
    npm run build
    ```

## Webpack Configuration

Below is a simple example of the `webpack.config.js` file used in this project:

```js
const path = require('path');

module.exports = {
    entry: './src/index.js',
    output: {
        filename: 'bundle.js',
        path: path.resolve(__dirname, 'dist'),
    },
    module: {
        rules: [
            {
                test: /\.css$/i,
                use: ['style-loader', 'css-loader'],
            },
        ],
    },
    mode: 'development',
};
