# 🐋 Hitchhiker's Guide to Cetaceans

**A friendly field guide to whales, dolphins, and porpoises—with science for those who want to dive deeper.**

[![GitHub Pages](https://img.shields.io/badge/GitHub-Pages-blue)](https://yourusername.github.io)
[![Weekly Posts](https://img.shields.io/badge/Cadence-Weekly-green)]()

---

## 🌊 About This Project

This is a **photo-forward marine biology blog** that explores the latest research on cetaceans—whales, dolphins, and porpoises. Each post includes:

- 📸 **High-quality images** with proper attribution
- 📖 **Narrative storytelling** accessible to everyone
- 🔬 **Scientific Geek Version** (toggle) with methods, citations, and research deep-dives
- 💡 **My angle & analysis** on the latest findings

**Live site:** [https://muditsinha01.github.io](https://muditsinha01.github.io)

---

## 📅 Publishing Schedule

**One post per week** exploring topics like:
- Communication in sperm whales
- Ecotypes of killer whales
- Navigation in humpback whales
- Social structures in dolphin pods
- Recent discoveries and emerging research

---

## 🛠️ Technical Stack

This site is built with:
- **GitHub Pages** (free hosting, auto-deployment)
- **Jekyll** (static site generator)
- **Minima theme** (clean, minimal, mobile-first)
- **Markdown** for all content (easy to write, version-controlled)
- **Vanilla JavaScript** for the "Geek Toggle" feature

### Why This Stack?

- ✅ **Zero maintenance** – no servers, no databases
- ✅ **Fast** – static HTML, no backend queries
- ✅ **Version control** – every edit is tracked in Git
- ✅ **Markdown-first** – write in plain text, publish in seconds
- ✅ **Free** – GitHub Pages is free for public repos

---

## 📁 Repository Structure
```
.
├── _config.yml              # Site configuration
├── _posts/                  # Blog posts (Markdown files)
│   └── YYYY-MM-DD-title.md
├── assets/
│   ├── css/
│   │   └── custom.css       # Ocean-blue theme styling
│   └── images/              # Post images (organized by date)
│       └── YYYY-MM-DD-post-name/
│           ├── hero.jpg
│           └── diagram.png
├── _includes/
│   └── head.html            # Custom CSS loader
├── index.md                 # Homepage
└── README.md                # This file
```

---

## 🎨 Design Philosophy

**Minimal. Readable. Ocean-inspired.**

- **Typography:** Clean sans-serif, generous line-height
- **Colors:** Ocean blues (#0a2e36, #167c9a), calm whites, coral accents
- **Mobile-first:** Most readers are on phones—design for thumbs
- **No clutter:** No animations, no popups, no distractions

---

## 📝 Writing Workflow

### 1. Create a new post
```bash
# File naming convention: _posts/YYYY-MM-DD-title.md
_posts/2025-11-15-humpback-navigation.md
```

### 2. Front matter template
```yaml
---
layout: post
title: "Navigation in Humpback Whales"
date: 2025-11-15
---
```

### 3. Add images
```markdown
![Humpback whale breaching]({{ '/assets/images/2025-11-15-humpback/breach.jpg' | relative_url }})
<p class="photo-credit">Photo: NOAA Fisheries (public domain)</p>
```

### 4. Include the "Geek Toggle"
```html
<button class="geek-toggle" onclick="toggleGeek()">🔬 Show Scientific Geek Version</button>

<div class="geek-content" style="display:none;">
<!-- Your research methods, citations, and deeper science here -->
</div>

<script>
function toggleGeek() {
  const el = document.querySelector('.geek-content');
  const btn = document.querySelector('.geek-toggle');
  if (el.style.display === 'none') {
    el.style.display = 'block';
    btn.textContent = '🔬 Hide Scientific Geek Version';
  } else {
    el.style.display = 'none';
    btn.textContent = '🔬 Show Scientific Geek Version';
  }
}
</script>
```

### 5. Commit and push
```bash
git add .
git commit -m "Add post: Navigation in Humpback Whales"
git push
```

🎉 **Your post is live in ~2 minutes.**

---

## 🖼️ Image Guidelines

### Sourcing
- **Public domain:** NOAA, Wikimedia Commons, NASA
- **Creative Commons:** Flickr, Unsplash (with attribution)
- **Licensed:** Contact researchers directly, credit properly

### Organization
```
assets/images/2025-11-15-humpback/
  ├── hero.jpg          # Main post image
  ├── migration-map.png # Supporting visual
  └── song-spectrogram.jpg
```

### Markdown syntax
```markdown
![Alt text]({{ '/assets/images/2025-11-15-humpback/hero.jpg' | relative_url }})
<p class="photo-credit">Photo: Dr. Jane Smith, Ocean Research Institute (CC BY 4.0)</p>
```

---

## 🔬 Scientific Standards

Every "Geek Version" should include:

1. **Methods** – How the research was conducted
2. **Key findings** – What the data shows
3. **My analysis** – What this means, open questions, connections to other research
4. **Citations** – Primary sources (papers, books, databases)
5. **Tools/Data** – Where readers can explore further

### Citation format
```markdown
- Whitehead, H., & Rendell, L. (2003). *The Cultural Lives of Whales and Dolphins*. University of Chicago Press.
```

---

## 📰 Research Focus

This blog follows **current cetacean research** and adds original analysis:

- Recent papers from marine biology journals
- Conference presentations and findings
- Long-term field studies
- Emerging methods and technologies
- Cross-species comparisons and patterns

**My angle:** Connecting dots between studies, asking "what's next?", and making cutting-edge research accessible.

---

## 🚀 Future Enhancements

**Planned features:**
- [ ] Upgrade to Minimal Mistakes theme (better layouts)
- [ ] Add image galleries (Lightbox/GLightbox)
- [ ] Client-side search (Lunr.js or Pagefind)
- [ ] Species index page (A-Z cetacean directory)
- [ ] Research timeline visualizations
- [ ] Paper summary archive

---

## 📚 Resources

### Marine Biology Journals & Sources
- [Marine Mammal Science Journal](https://onlinelibrary.wiley.com/journal/17487692)
- [Journal of the Acoustical Society of America](https://asa.scitation.org/journal/jas)
- [NOAA Fisheries Research](https://www.fisheries.noaa.gov/science-and-data)
- [bioRxiv Preprints (Ecology)](https://www.biorxiv.org/collection/ecology)

### Jekyll & GitHub Pages
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Guide](https://docs.github.com/en/pages)
- [Markdown Cheatsheet](https://www.markdownguide.org/cheat-sheet/)

---

## 📬 Contact

Questions, corrections, or collaboration ideas?

- **Email:** your@email.com
- **Twitter/X:** @yourusername
- **GitHub Issues:** [Open an issue](https://github.com/yourusername/yourusername.github.io/issues)

---

## 📄 License

### Content
All written content (blog posts, narratives, analysis) is licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/).  
**Attribution required. Non-commercial use only.**

### Code
All code (HTML, CSS, JavaScript) is licensed under the [MIT License](https://opensource.org/licenses/MIT).

### Images
Images are credited individually in each post. See photo credits for specific licenses.

---

## 🙏 Acknowledgments

This project stands on the shoulders of:
- Marine biologists and researchers studying cetaceans
- Open-source contributors to Jekyll and GitHub Pages
- Peer reviewers and journal editors advancing the field
- The ocean, and the whales who call it home

---

**🐋 Happy reading, and welcome aboard!**

---

*Built with ❤️ for ocean lovers and science nerds*