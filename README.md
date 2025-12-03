# Chris Selden's Blog

A minimalist Jekyll-based blog with full support for markdown, images, and videos.

## Features

- Clean, minimalist design using the Minima theme
- Full markdown support for writing posts
- Automatic responsive image handling
- Support for local and embedded videos
- Simple to use and maintain

## Getting Started

### Prerequisites

- Ruby (version 2.7 or higher)
- Bundler gem (`gem install bundler`)

### Installation

Dependencies are already installed, but if needed:

```bash
bundle install
```

### Running the Blog Locally

Start the Jekyll development server:

```bash
bundle exec jekyll serve
```

Then open your browser to `http://localhost:4000`

The server will automatically reload when you make changes to your posts or configuration.

## Creating a New Post

1. Create a new file in the `_posts` directory with the naming format:
   ```
   YYYY-MM-DD-title-of-post.md
   ```
   For example: `2025-12-02-my-awesome-post.md`

2. Add front matter at the top of the file:
   ```yaml
   ---
   layout: post
   title: "Your Post Title"
   date: 2025-12-02 10:00:00 -0000
   categories: blog category1 category2
   ---
   ```

3. Write your content in markdown below the front matter

4. Save the file and it will automatically appear on your blog

## Adding Images

1. Place your image files in the `assets/images/` directory

2. Reference them in your posts using markdown:
   ```markdown
   ![Alt text for the image](/assets/images/your-image.jpg)
   *Optional caption text below the image*
   ```

Images will automatically be:
- Responsive (scale to fit any screen size)
- Centered on the page
- Styled with a subtle shadow

## Adding Videos

### Local Video Files

1. Place video files in the `assets/videos/` directory

2. Use HTML5 video tags in your post:
   ```html
   <video controls>
     <source src="/assets/videos/your-video.mp4" type="video/mp4">
     Your browser does not support the video tag.
   </video>
   ```

### Embedded Videos (YouTube, Vimeo, etc.)

Wrap the embed iframe in a `.video-container` div for responsive sizing:

```html
<div class="video-container">
  <iframe src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0" allowfullscreen></iframe>
</div>
```

## Customization

### Site Settings

Edit `_config.yml` to customize:
- Site title
- Description
- Email
- Social media usernames
- And more

After changing `_config.yml`, restart the Jekyll server.

### Styling

Custom styles are in `assets/css/style.css`. You can modify this file to:
- Change colors and fonts
- Adjust image and video styling
- Add new CSS rules

## Project Structure

```
.
├── _config.yml          # Site configuration
├── _layouts/            # Custom page layouts
│   └── post.html       # Blog post layout
├── _posts/              # Your blog posts go here
├── assets/
│   ├── css/
│   │   └── style.css   # Custom styles
│   ├── images/          # Image files
│   └── videos/          # Video files
├── about.markdown       # About page
├── index.markdown       # Home page
└── Gemfile             # Ruby dependencies
```

## Deployment

### GitHub Pages

1. Push your repository to GitHub
2. Go to Settings > Pages
3. Select the branch to deploy (usually `main`)
4. Your site will be available at `https://username.github.io/repository-name`

### Other Hosting

Build the static site:

```bash
bundle exec jekyll build
```

The built site will be in the `_site` directory. Upload this to any static hosting service.

## Markdown Reference

See the sample post at `_posts/2025-12-02-welcome-to-my-blog.md` for examples of:
- Text formatting
- Code blocks
- Lists
- Blockquotes
- Images and videos

## Troubleshooting

### Server won't start
- Make sure all dependencies are installed: `bundle install`
- Check Ruby version: `ruby -v` (should be 2.7+)

### Changes not showing
- Restart the Jekyll server
- Clear your browser cache
- For `_config.yml` changes, always restart the server

### Images not displaying
- Check the file path is correct
- Ensure images are in the `assets/images/` directory
- Image paths are case-sensitive

## License

This blog is open source and available for your personal use.
