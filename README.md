# Hugo Blog Setup

Hugo is a fast and flexible static site generator written in Go. This guide will help you set up a new blog using Hugo.

## Installation Instructions

1. **Install Hugo**:
   - You can download the latest version of Hugo from the [Hugo Releases page](https://github.com/goharbor/hugo/releases).
   - For macOS, you can use Homebrew:
     ```bash
     brew install hugo
     ```
   - For Windows, you can use Chocolatey:
     ```bash
     choco install hugo-extended
     ```

2. **Verify the installation**:
   Run the following command to confirm Hugo is installed:
   ```bash
   hugo version
   ```

## Creating a New Hugo Site

1. Create a new Hugo site by running:
   ```bash
   hugo new site myblog
   ```
   Replace `myblog` with your desired site name.

2. Navigate into your new site’s directory:
   ```bash
   cd myblog
   ```

3. Add a theme to your site:
   ```bash
   git init
   git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
   ```
   Replace the theme URL with the theme of your choice.

4. Configure your site:
   Edit the `config.toml` file to set your site’s title and other parameters as desired.

## Starting the Local Server

1. Start the Hugo development server by running:
   ```bash
   hugo server
   ```

2. Open your web browser and visit [http://localhost:1313](http://localhost:1313) to see your blog.

## Deployment Instructions

Once you're happy with your blog, you can deploy it:

1. **Build the site**:
   ```bash
   hugo -D
   ```
   This will generate your site in the `public` directory.

2. **Deploying to GitHub Pages**:
   - Create a new repository on GitHub.
   - Change directory to your `public` folder:
     ```bash
     cd public
     ```
   - Initialize a Git repository, add files, and commit:
     ```bash
     git init
     git add .
     git commit -m "Initial commit"
     ```
   - Push to the `gh-pages` branch of your GitHub repository:
     ```bash
     git remote add origin YOUR_REPOSITORY_URL
     git push -u origin master:gh-pages
     ```
   Replace `YOUR_REPOSITORY_URL` with the URL of your GitHub repository.

Your Hugo blog is now set up and deployed!