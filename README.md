# Portfolio

This is the source code for my portfolio website, written from scratch in Vue.

# Installation

1. Install the dependencies: `npm install`
2. Compile the project: `npm run build`
3. Deploy the `dist` directory.

# Usage

The components are pretty straightforward. For a project that takes up a whole row, use LargeProject. For a project that takes up half a row (except when mobile scaled) use SmallProject inside of ProjectGrid. LargeProject takes an optional parameter for the image.

All projects take an array of icon variables to display. I wouldn't recomment using more than 4 or 5 icons per project.

The about section is stored in a variable called about since it's multiple lines of text that wouldn't fit well in a single tag.
