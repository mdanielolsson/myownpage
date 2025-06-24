# My Kubernetes & Cloud Blog

This is a Jekyll-based blog designed for sharing insights, tutorials, and thoughts on Kubernetes, cloud computing, and related technologies. It's set up to be easily hosted on GitHub Pages.

## Prerequisites

Before you begin, ensure you have the following installed:

*   **Ruby**: Jekyll is a Ruby gem. [Install Ruby](https://www.ruby-lang.org/en/documentation/installation/) (version 2.5.0 or higher is recommended).
*   **RubyGems**: Usually comes with Ruby.
*   **GCC and Make**: If your system doesn't have them (e.g., some Linux distros, macOS with Command Line Tools not installed). Run `gcc -v` and `make -v` to check.
*   **Bundler**: Install with `gem install bundler`.

## Local Development

To set up and run this Jekyll site locally:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/YOUR_GITHUB_USERNAME/YOUR_REPOSITORY_NAME.git
    cd YOUR_REPOSITORY_NAME
    ```
    *(Replace `YOUR_GITHUB_USERNAME` and `YOUR_REPOSITORY_NAME`)*

2.  **Install dependencies:**
    Navigate to the project directory and run:
    ```bash
    bundle install
    ```
    This command installs all the gems specified in your `Gemfile`.

3.  **Serve the site:**
    ```bash
    bundle exec jekyll serve --livereload
    ```
    *   `--livereload` automatically refreshes the page in your browser when you make changes to content or styling.

4.  **View the site:**
    Open your web browser and go to `http://localhost:4000`.

## Configuration

*   Edit `_config.yml` to personalize your site settings:
    *   `title`: Your site's title.
    *   `email`: Your contact email.
    *   `description`: A brief description of your site.
    *   `github_username`: Your GitHub username (used for links).
    *   `baseurl`: If you are hosting on a GitHub Project page (e.g., `username.github.io/repository-name`), set this to `/repository-name`. For a user/organization page (`username.github.io`), keep it as `""`.
    *   `url`: Your site's main URL (e.g., `https://username.github.io`). GitHub Pages often sets this automatically.
    *   Update the default `author` under `defaults` if desired.

## Creating Content

*   **Blog Posts:**
    *   Create new Markdown files in the `_posts` directory.
    *   Filename format: `YYYY-MM-DD-your-post-title.md`.
    *   Include front matter at the top of each post (see example post for structure).
*   **Pages:**
    *   Create Markdown or HTML files in the root directory (e.g., `about.md`) or in dedicated folders.
    *   Include front matter (at least `layout` and `title`).
*   **E-books:**
    *   Add details for your e-books in the `ebooks.md` file.
    *   Update links and cover images. Store images in `assets/images/`.
    *   The `ebooks` collection is configured in `_config.yml`. If you want to create individual pages per e-book, you can create markdown files in a `_ebooks` directory.

## Deployment to GitHub Pages

This site is configured to be easily deployed using GitHub Pages.

1.  **Push to GitHub:**
    Commit your changes and push them to your GitHub repository's main branch (or whichever branch you've configured for GitHub Pages).
    ```bash
    git add .
    git commit -m "Add content and configure site"
    git push origin main
    ```

2.  **Configure GitHub Pages:**
    *   Go to your repository on GitHub.
    *   Click on "Settings".
    *   Navigate to the "Pages" section in the sidebar.
    *   Under "Build and deployment", for "Source", select "Deploy from a branch".
    *   Choose the branch you want to deploy from (e.g., `main`).
    *   Ensure the `/ (root)` folder is selected.
    *   Save changes.

    GitHub Pages will then build and deploy your site. It might take a few minutes for the site to become live at `https://YOUR_GITHUB_USERNAME.github.io/YOUR_REPOSITORY_NAME/` (for project pages) or `https://YOUR_GITHUB_USERNAME.github.io/` (for user/org pages).

## Custom Domain

If you have a custom domain, you can configure it in the GitHub Pages settings for your repository. You'll also need to update your DNS records. See [GitHub's documentation on custom domains](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

## Styling

*   Basic styles are in `assets/css/style.css`.
*   The site uses the `minima` theme as a base, but the custom CSS will override many aspects. You can further customize `style.css` or add more stylesheets.

---

Happy blogging! Remember to replace placeholder values like `[Your Name]`, `your-email@example.com`, and `YOUR_GITHUB_USERNAME` in the configuration and content files.
