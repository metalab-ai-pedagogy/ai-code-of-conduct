# AI Code of Conduct

## Getting Started
1. Ensure you have Node.js installed on your local computer. 
2. Clone the repository to your computer

### Structure
The website's files lives in two places in this repository: the `main` branch and the `development` branch. The `main` branch holds the live site (the static files that are displayed when you visit the URL). The `development` branch holds everything you'll need to make updates and changes.

### Install Dependencies
Before you begin making changes, you'll want to ensure you've installed all of the website's dependencies (notably Tailwind CSS, the style library we're using). This can all be installed with a single command within your terminal (make sure you're in the `ai-code-of-confuct` folder):
```bash
npm install
```

### Run Tailwind CSS engine
Once you've installed the dependencies, run this command in your terminal. It will run in the background and take all of the input styles from both the HTML file and our inputted CSS file and consolodate them into a single file. 
```bash
npx tailwindcss -i ./src/input.css -o ./public/assets/styles/output.css --watch
```

### Making Changes
There are only two places you'll need to go to make changes to the website:
* `public/index.html`: the stucture and content of the website
* `src/input.css`: the _custom_ styles supporting the website

As you make changes, updating styles, content, or classes, the output styles will automatically update thanks to the Tailwind CSS engine running in the background.

If you're making changes to the styles, Tailwind CSS has classes for pretty much every stylistic change you'd need (see [Tailwind CSS Docs](https://tailwindcss.com/)). If there's something custom you want to do (like metaLAB-specific colors), that goes in the `src/input.css` file! 

### Uploading Changes to GitHub
Once you've made all of the desired changes, commit the changes of the `development` branch to GitHub. You'll then want to copy _all_ of the contents of the `public` folder and paste them into the `main` branch. This is because the static site itself lives in the `public` folder, and the `main` branch is just a reflection of that. 

As soon as you commit changes to the `main` branch, the GitHub pages website will automatically update (but you can check on its progress with the repo's [Actions page](https://github.com/metalab-ai-pedagogy/ai-code-of-conduct/actions)). 