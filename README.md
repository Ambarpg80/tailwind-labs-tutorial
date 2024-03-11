This repo is a starting point to learn Tailwind CSS from tailwind labs.
[Tailwinds_tutorial] "https://www.youtube.com/watch?v=UvF56fPGVt4"

Steps to initiate Tailwind CSS :

1. Install tailwindcss via npm, and create your tailwind.config.js file. 
    `npm install -D tailwindcss`
    `npx tailwindcss init `
    
2. to configure your template paths, add the paths to all of your template files in your *tailwind.config.js* file.
    > /** @type {import('tailwindcss').Config} */
    >   module.exports = {
    >    content: ["./src/**/*.{html,js}"],
    >    theme: {
    >       extend: {},
    >    },
    >    plugins: [],
    >    }

3. Add the @tailwind directives for each of Tailwind’s layers to your main CSS file.
   - @tailwind base;
   - @tailwind components;
   - @tailwind utilities;

4. Start the Tailwind CLI build process. Run the CLI tool to scan your template files for classes and build your CSS. In terminal this will trigger a rebuild so that changes made are automatically shown in preview.  *This command can also be added to package.json to keep watch of changes but may cause a delay*

   - `npx tailwindcss -i ./src/input.css -o ./src/output.css --watch`

5. Add your compiled CSS file to the <head> and start using Tailwind’s utility classes to style your content.

  - *link href="./output.css" rel="stylesheet"*
    