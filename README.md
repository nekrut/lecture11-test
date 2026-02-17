# Academic Website - Miffy B. Pluis

A professional academic website built with [Quarto](https://quarto.org/), featuring a CV homepage and integrated blog functionality. The site is automatically deployed to GitHub Pages using GitHub Actions.

## 🌐 Live Site

Visit the live website at: **https://nekrut.github.io/lecture11-test/**

## 📋 Features

- **CV Homepage**: Full academic curriculum vitae displayed as the main landing page
- **Blog Section**: Integrated blog with automatic post listing and categorization
- **Responsive Design**: Clean, professional layout that works on all devices
- **Automatic Deployment**: GitHub Actions workflow that builds and deploys on every push
- **Easy Content Management**: Write content in Markdown/Quarto format
- **SEO Friendly**: Proper metadata and structure for search engines

## 📁 Project Structure

```
.
├── _quarto.yml                          # Main Quarto configuration
├── index.qmd                            # CV homepage
├── blog.qmd                             # Blog listing page
├── posts/                               # Blog posts directory
│   └── creating-this-website/
│       └── index.qmd                    # Individual blog post
├── styles.css                           # Custom CSS styling
├── .github/
│   └── workflows/
│       └── publish.yml                  # GitHub Actions deployment workflow
├── .gitignore                           # Git ignore file (excludes build artifacts)
└── README.md                            # This file
```

## 🚀 Getting Started

### Prerequisites

To work with this project locally, you need:

- [Quarto](https://quarto.org/docs/get-started/) installed on your system
- Git for version control
- A text editor (VS Code, RStudio, etc.)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/nekrut/lecture11-test.git
   cd lecture11-test
   ```

2. **Preview the site locally**
   ```bash
   quarto preview
   ```
   This will start a local server (usually at `http://localhost:4200`) and automatically reload when you make changes.

3. **Render the site**
   ```bash
   quarto render
   ```
   This generates the static website in the `_site/` directory.

## ✍️ Adding Content

### Updating Your CV

Edit `index.qmd` to update your CV. This file uses standard Markdown formatting with YAML frontmatter.

### Adding a New Blog Post

1. **Create a new directory** in the `posts/` folder:
   ```bash
   mkdir -p posts/my-new-post
   ```

2. **Create an `index.qmd` file** in the new directory with this structure:
   ```yaml
   ---
   title: "Your Post Title"
   author: "Your Name"
   date: "2026-02-17"
   categories: [category1, category2, category3]
   description: "A brief description of your post"
   ---

   ## Introduction

   Your content here...
   ```

3. **Write your content** using Markdown, including:
   - Headers (`##`, `###`)
   - Lists (bulleted or numbered)
   - Links: `[text](url)`
   - Images: `![alt text](image-url)`
   - Code blocks with syntax highlighting
   - Mathematical equations (LaTeX syntax)

4. **Commit and push**:
   ```bash
   git add posts/my-new-post/
   git commit -m "Add new blog post: Your Post Title"
   git push origin main
   ```

The site will automatically rebuild and deploy within 1-2 minutes.

### Blog Post Features

Quarto supports rich content including:

- **Code blocks** with syntax highlighting
- **Mathematical equations** using LaTeX syntax: `$E = mc^2$`
- **Interactive plots** (if using R or Python)
- **Tables**, **images**, and **diagrams**
- **Cross-references** between sections
- **Citations and bibliographies**

Example code block:
````markdown
```python
def hello_world():
    print("Hello, World!")
```
````

## 🎨 Customization

### Theme and Styling

- **Theme**: Edit the `theme` setting in `_quarto.yml` (current: `cosmo`)
  - Available themes: `default`, `cosmo`, `flatly`, `darkly`, `journal`, etc.
- **Custom CSS**: Modify `styles.css` for additional styling
- **Navigation**: Update the navbar in `_quarto.yml` to add/remove pages

### Site Configuration

Edit `_quarto.yml` to customize:
- Site title and description
- Navigation menu
- Footer content
- Theme and appearance
- Output options

Example:
```yaml
website:
  title: "Your Name"
  navbar:
    left:
      - text: "Home"
        href: index.qmd
      - text: "Blog"
        href: blog.qmd
      - text: "Publications"
        href: publications.qmd
```

## 🔄 Deployment

### Automatic Deployment (Enabled)

The site automatically deploys to GitHub Pages when you push to the `main` branch:

1. **Push your changes** to GitHub
2. **GitHub Actions** automatically:
   - Checks out the code
   - Installs Quarto
   - Renders the website
   - Deploys to GitHub Pages
3. **Site updates** live in 1-2 minutes

### Manual Deployment

You can also manually trigger deployment:
1. Go to the [Actions tab](https://github.com/nekrut/lecture11-test/actions)
2. Click "Publish Quarto Website"
3. Click "Run workflow" → "Run workflow"

## 🛠️ Workflow Details

The GitHub Actions workflow (`.github/workflows/publish.yml`):
- Triggers on push to `main` branch
- Requires GitHub Pages to be enabled with "GitHub Actions" as the source
- Uses the official Quarto action for setup
- Builds the site and uploads artifacts
- Deploys to the `gh-pages` environment

## 📚 Resources

- **Quarto Documentation**: https://quarto.org/docs/guide/
- **Quarto Websites**: https://quarto.org/docs/websites/
- **Quarto Blogs**: https://quarto.org/docs/websites/website-blog.html
- **GitHub Pages**: https://docs.github.com/en/pages
- **Markdown Guide**: https://www.markdownguide.org/

## 🐛 Troubleshooting

### Site not updating
- Check the [Actions tab](https://github.com/nekrut/lecture11-test/actions) for workflow status
- Ensure GitHub Pages is enabled with "GitHub Actions" as the source
- Clear your browser cache

### Local preview not working
- Ensure Quarto is installed: `quarto --version`
- Check for syntax errors in `.qmd` files
- Try rendering first: `quarto render`

### Build failures
- Check the Actions logs for error messages
- Verify YAML frontmatter is properly formatted
- Ensure all file paths are correct

## 📄 License

This project is open source and available under the MIT License.

## 👤 Author

**Miffy B. Pluis, PhD**
Professor of Burrow Architecture & Lapine Behavioral Sciences
University of Utrecht-den-Haag

---

*Built with [Quarto](https://quarto.org/) and deployed via [GitHub Actions](https://github.com/features/actions)*
