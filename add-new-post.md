# How to Add a New Blog Post

## Step 1: Create a New Post File
1. Go to the `_posts` directory
2. Create a new Markdown file with the naming format: `YYYY-MM-DD-title-of-your-post.md`
   - Example: `2025-02-26-my-new-blog-post.md`

## Step 2: Add Front Matter
Add the following YAML front matter at the top of your markdown file:
```yaml
---
title: "Your Post Title"
date: YYYY-MM-DD
excerpt: "A brief description of your post"
tags: ["tag1", "tag2"]
coverImage: "optional-cover-image-path"
---
```

## Step 3: Add Content
Write your blog post content in Markdown format below the front matter.

## Step 4: Add Images (if any)
- Place images in the `content/images` directory
- Reference them in your markdown using the correct relative path

## Step 5: Test Locally
1. Start the Jekyll development server:
   ```bash
   bundle exec jekyll serve
   ```
   If port 4000 is in use, use an alternative port:
   ```bash
   bundle exec jekyll serve -P 4001
   ```
2. Visit `http://localhost:4000` (or the alternative port) in your browser
3. Check that your post appears and is formatted correctly

## Step 6: Commit and Push
1. Stage your changes:
   ```bash
   git add _posts/
   git add content/images/  # if you added images
   ```
2. Commit your changes:
   ```bash
   git commit -m "Add new blog post: [Your Post Title]"
   ```
3. Push to GitHub:
   ```bash
   git push origin main
   ```

Your post will be automatically deployed to your GitHub Pages site after pushing.