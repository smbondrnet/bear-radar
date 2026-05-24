# Bear Radar

A static landing page hosted on GitHub Pages at [bear-radar.io](https://bear-radar.io).

## Setup GitHub Pages with Custom Domain

### 1. Push to GitHub
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/smbondrnet/bear-radar.git
git push -u origin main
```

### 2. Enable GitHub Pages
1. Go to your repository on GitHub
2. Navigate to **Settings** → **Pages**
3. Under "Source", select **Deploy from a branch**
4. Select **main** branch and **/ (root)** folder
5. Click **Save**

### 3. Configure DNS in GoDaddy

Go to GoDaddy → **My Products** → **DNS** for `bear-radar.io`:

#### Add A Records (for apex domain `bear-radar.io`):
| Type | Name | Value |
|------|------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

#### Add CNAME Record (for `www.bear-radar.io`):
| Type | Name | Value |
|------|------|-------|
| CNAME | www | smbondrnet.github.io |

### 4. Finalize in GitHub
1. In **Settings** → **Pages**, enter `bear-radar.io` as custom domain
2. Click **Save**
3. Wait for DNS to propagate (can take up to 24-48 hours, usually faster)
4. Check **Enforce HTTPS** once available

## Local Development
Simply open `index.html` in your browser.
