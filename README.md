# 🦙 Alpaca Image Generator

A fun, interactive React web app that lets users customize and download their own alpaca avatar. Mix and match different alpaca features to create a unique character, then save it as an image.

![Alpaca Image Generator Screenshot](https://user-images.githubusercontent.com/84178696/201708267-3ff9089f-d2e1-4fcb-89e5-d21b7700c49d.png)

🔗 **[Live Demo](https://alpaca-image-generator-beta.vercel.app/)**

---

## Features

- Customize your alpaca across multiple feature categories (accessories, hair, backgrounds, and more)
- Combine layered images in real time to compose a unique avatar
- Download your generated alpaca as an image file
- Fully responsive UI built with React

---

## Tech Stack

| Technology | Purpose |
|---|---|
| [React 18](https://reactjs.org/) | UI framework and component state management |
| CSS | Styling and layout |
| [html-to-image](https://github.com/bubkoo/html-to-image) | Converting the rendered alpaca to a downloadable image |
| [downloadjs](https://github.com/rndme/download) | Triggering the file download in the browser |

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v16 or higher recommended)
- npm (comes with Node.js)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/shenaltissera/alpaca-image-generator.git
   cd alpaca-image-generator
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

4. Open [http://localhost:3000](http://localhost:3000) in your browser.

### Available Scripts

| Command | Description |
|---|---|
| `npm start` | Run the app in development mode |
| `npm run build` | Build the app for production |
| `npm test` | Launch the test runner |
| `npm run eject` | Eject from Create React App (irreversible) |

---

## Project Structure

```
alpaca-image-generator/
├── public/          # Static assets
├── src/             # React source code
│   ├── components/  # UI components
│   └── ...
├── package.json
└── README.md
```

---

## How It Works

The app renders an alpaca avatar by layering multiple PNG images on top of each other — one per feature category (e.g. ears, hair, accessories). When a user selects a style for a category, the corresponding layer updates in real time.

State is managed with React's `useState` hook, with props passed down to child components to keep the entire avatar in sync. When the user is happy with their alpaca, `html-to-image` captures the rendered component and `downloadjs` saves it to their device.

---

## Lessons Learned

This was a first hands-on project with interactive React state management. Key takeaways included:

- Working confidently with the `useState` hook across multiple components
- Using props to propagate state changes through a component tree
- Structuring data files to drive dynamic UI rendering (including nested arrays for style variants)
- Integrating third-party libraries (`html-to-image`, `downloadjs`) to extend browser functionality

---

## Acknowledgements

This project was built as part of the [DevProjects](https://www.codementor.io/projects/web/alpaca-image-generator-website-ce2oc0eus8) open-source challenge by Codementor.

---

## License

This project is open source. Feel free to fork, learn from, and build on it.
