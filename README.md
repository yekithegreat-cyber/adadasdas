# 🎬 GitHub Video Gallery

A simple, free video hosting solution using GitHub and GitHub Pages!

## ✨ Features

- ✅ **100% FREE** - Uses GitHub for storage & hosting
- ✅ **No backend needed** - Pure HTML/CSS/JS
- ✅ **Unlimited videos** - GitHub allows large files with Git LFS
- ✅ **Beautiful UI** - Gradient design with video cards
- ✅ **Responsive** - Works on mobile and desktop
- ✅ **Full-screen player** - Click to watch videos

## 🚀 How to Set Up (10 minutes)

### Step 1: Create GitHub Repository

1. Go to [github.com](https://github.com)
2. Click **"New repository"** (green button)
3. Name it: `my-video-gallery` (or any name)
4. Make it **Public** (required for GitHub Pages)
5. Check **"Add a README file"**
6. Click **"Create repository"**

### Step 2: Upload Your Videos

1. In your repository, click **"Add file"** → **"Create new file"**
2. Type: `videos/.gitkeep` (this creates a videos folder)
3. Click **"Commit new file"**
4. Click on the **"videos"** folder
5. Click **"Add file"** → **"Upload files"**
6. **Drag and drop your video files** (MP4, WebM, MOV, etc.)
7. Click **"Commit changes"**

**Note**: For videos larger than 25MB, you'll need to use Git LFS (see instructions below)

### Step 3: Upload index.html

1. Go back to the main repository page
2. Click **"Add file"** → **"Upload files"**
3. Upload the **index.html** file from this package
4. Click **"Commit changes"**

### Step 4: Edit Video URLs in index.html

1. Click on **index.html** in your repository
2. Click the **pencil icon** (Edit this file)
3. Find the `videos` array (around line 162)
4. Replace `YOUR-USERNAME` with your GitHub username
5. Replace `YOUR-REPO` with your repository name
6. Update video names to match your uploaded videos

Example:
```javascript
const videos = [
    {
        title: "My First Video",
        description: "This is my first video",
        url: "https://raw.githubusercontent.com/john123/my-video-gallery/main/videos/myvideo.mp4"
    },
    {
        title: "Vacation 2024",
        description: "Summer vacation highlights",
        url: "https://raw.githubusercontent.com/john123/my-video-gallery/main/videos/vacation.mp4"
    }
];
```

7. Click **"Commit changes"**

### Step 5: Enable GitHub Pages

1. Go to your repository **Settings**
2. Click **"Pages"** (left sidebar)
3. Under **"Source"**, select **"main"** branch
4. Click **"Save"**
5. Wait 1-2 minutes
6. Your site will be live at: `https://YOUR-USERNAME.github.io/YOUR-REPO/`

🎉 **Done! Your video gallery is live!**

---

## 📹 Adding More Videos

### Option 1: Web Interface (Easy, < 25MB videos)

1. Go to your repository
2. Click on **"videos"** folder
3. Click **"Add file"** → **"Upload files"**
4. Upload your video
5. Go to **index.html** and click edit (pencil icon)
6. Add new video to the array:
```javascript
{
    title: "New Video Title",
    description: "Description here",
    url: "https://raw.githubusercontent.com/YOUR-USERNAME/YOUR-REPO/main/videos/newvideo.mp4"
}
```
7. Commit changes

### Option 2: Git LFS (For Large Videos > 25MB)

GitHub has a 25MB file size limit. For larger videos, use Git LFS:

**Install Git LFS:**
```bash
# Windows (with Git installed)
git lfs install

# Mac
brew install git-lfs
git lfs install

# Linux
sudo apt-get install git-lfs
git lfs install
```

**Use Git LFS:**
```bash
# Clone your repo
git clone https://github.com/YOUR-USERNAME/YOUR-REPO.git
cd YOUR-REPO

# Track video files with LFS
git lfs track "videos/*.mp4"
git lfs track "videos/*.mov"
git lfs track "videos/*.avi"

# Add .gitattributes
git add .gitattributes

# Add your large video
git add videos/large-video.mp4
git commit -m "Add large video"
git push
```

**GitHub LFS Free Tier:**
- 1GB storage
- 1GB bandwidth/month
- Perfect for 10-20 videos

---

## 🎨 Customization

### Change Colors

Edit the gradient in `index.html`:
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

Try these:
- Blue to Purple: `#667eea 0%, #764ba2 100%`
- Pink to Orange: `#f093fb 0%, #f5576c 100%`
- Green to Blue: `#11998e 0%, #38ef7d 100%`
- Red to Yellow: `#eb3349 0%, #f45c43 100%`

### Change Title

Edit line 142:
```html
<h1>🎬 My Video Gallery</h1>
```

### Video Grid Columns

Edit line 63 for more/fewer columns:
```css
grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
```

Change `350px` to:
- `250px` for smaller cards (more columns)
- `450px` for larger cards (fewer columns)

---

## 📊 Storage Limits

### GitHub Free Account:
- ✅ Repository size: Unlimited (with Git LFS)
- ✅ File size: 100MB (with Git LFS)
- ✅ Bandwidth: Unlimited for public repos
- ✅ Git LFS: 1GB storage, 1GB bandwidth/month

### What This Means:
- **Without Git LFS**: ~40-50 small videos (< 25MB each)
- **With Git LFS**: 10-20 large videos (50-100MB each)

---

## 🔧 Troubleshooting

### Videos won't play
**Problem**: Video URL is wrong

**Solution**: 
1. Go to your video on GitHub
2. Click "Raw" button
3. Copy the URL
4. Make sure it starts with: `https://raw.githubusercontent.com/`

### Video is too large to upload
**Problem**: File is > 25MB

**Solution**: 
1. Use Git LFS (see instructions above)
2. Or compress your video using [HandBrake](https://handbrake.fr/)

### Site not updating
**Problem**: Changes not showing on live site

**Solution**:
1. Wait 2-3 minutes for GitHub Pages to rebuild
2. Hard refresh browser: `Ctrl+F5` (Windows) or `Cmd+Shift+R` (Mac)
3. Clear browser cache

### Page shows 404
**Problem**: GitHub Pages not enabled correctly

**Solution**:
1. Go to Settings → Pages
2. Make sure "main" branch is selected
3. Wait 2 minutes
4. Try again

---

## 🎯 File Structure

```
my-video-gallery/
├── videos/
│   ├── video1.mp4
│   ├── video2.mp4
│   └── video3.mp4
├── index.html          ← Your website
└── README.md           ← This file
```

---

## 🚀 Advanced: Custom Domain

Want `videos.yourdomain.com` instead of `username.github.io`?

1. Buy domain from [Namecheap](https://namecheap.com) (~$10/year)
2. In your repo: Settings → Pages → Custom domain
3. Enter your domain
4. Add CNAME record in your domain settings
5. Wait 24 hours for DNS to update

GitHub Pages supports custom domains on free tier! ✨

---

## 💡 Tips

### Video Optimization
- Use MP4 format (best compatibility)
- Compress videos with HandBrake before uploading
- Recommended settings: H.264, 720p, ~2-5 Mbps bitrate

### Organization
- Create subfolders: `videos/2024/`, `videos/vacation/`, etc.
- Name videos descriptively: `vacation-2024-hawaii.mp4`

### Privacy
- **Public repos**: Anyone can see your videos
- **Private repos**: GitHub Pages only works on public repos
- **Solution**: Use Cloudinary for private videos (see other package)

---

## 🆚 Comparison: GitHub vs Cloudinary

| Feature | GitHub (This) | Cloudinary (Other Package) |
|---------|--------------|---------------------------|
| **Cost** | Free | Free (25GB) |
| **Setup** | 10 minutes | 15 minutes |
| **Backend** | None needed | Needs server (Render) |
| **Video Size** | 100MB (with LFS) | No limit |
| **Privacy** | Public only | Can be private |
| **Editing** | Manual | Auto upload/delete |
| **Best For** | Simple galleries | Full video platform |

---

## 📖 Next Steps

1. ✅ Upload your videos to GitHub
2. ✅ Edit index.html with your video URLs
3. ✅ Enable GitHub Pages
4. ✅ Share your gallery URL!

---

## 🆘 Need Help?

- [GitHub Pages Docs](https://docs.github.com/en/pages)
- [Git LFS Tutorial](https://git-lfs.github.com/)
- [HTML Video Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video)

---

**🎬 Enjoy your free video gallery!**

Built with ❤️ using GitHub Pages
