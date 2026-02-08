# 🚀 QUICK START - 5 STEPS!

## Step 1: Create GitHub Repo (2 min)
1. Go to github.com
2. Click "New repository"
3. Name: `my-video-gallery`
4. Make it **PUBLIC**
5. Click "Create repository"

## Step 2: Upload Videos (3 min)
1. In repo, click "Add file" → "Create new file"
2. Type: `videos/.gitkeep`
3. Commit
4. Click "videos" folder
5. Click "Upload files"
6. **DRAG YOUR VIDEOS HERE**
7. Commit

## Step 3: Upload index.html (1 min)
1. Go back to main page
2. Click "Upload files"
3. Upload **index.html** from this package
4. Commit

## Step 4: Edit Video URLs (2 min)
1. Click **index.html**
2. Click pencil icon (Edit)
3. Find line 162 (the `videos` array)
4. Replace `YOUR-USERNAME` with your GitHub username
5. Replace `YOUR-REPO` with `my-video-gallery`
6. Replace video filenames with your actual video names

**Example:**
```javascript
const videos = [
    {
        title: "My Video",
        description: "Cool video",
        url: "https://raw.githubusercontent.com/john123/my-video-gallery/main/videos/myvideo.mp4"
    }
];
```

## Step 5: Enable GitHub Pages (1 min)
1. Go to Settings → Pages
2. Source: **main** branch
3. Click Save
4. Wait 2 minutes
5. Visit: `https://YOUR-USERNAME.github.io/my-video-gallery/`

## ✅ DONE!

Your video gallery is live! 🎉

---

## 📝 Quick Example

If your username is `john123` and you uploaded `vacation.mp4`:

```javascript
const videos = [
    {
        title: "Summer Vacation",
        description: "Beach trip 2024",
        url: "https://raw.githubusercontent.com/john123/my-video-gallery/main/videos/vacation.mp4"
    }
];
```

---

## ⚠️ Important Notes

- Videos must be **PUBLIC** (GitHub Pages requirement)
- Max file size: **25MB** (use Git LFS for larger)
- Use **MP4** format for best compatibility
- Wait 2-3 minutes after commits for updates

---

**Need more help?** Read the full **README.md** file!
