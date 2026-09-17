# André Mello Jablonski — academic website

A lightweight, responsive academic homepage for **https://andremellojablonski.github.io/**. The site uses plain HTML and CSS, with no installation, build, or third-party scripts required.

## Start here: everyday edits in your browser

Your **repository** is the folder of files that powers your website. GitHub Pages publishes those files as a website. A **commit** is a saved version with a short description of what changed. The **main branch** is the version that gets published.

### Change your biography, email, or paper title

1. Open [your repository](https://github.com/andremellojablonski/andremellojablonski.github.io).
2. Click **index.html**, then the pencil icon (**Edit this file**).
3. Find the sentence you want to change and edit the words. Keep the surrounding HTML tags, such as `<p>` and `</p>`.
4. Click **Commit changes…**, enter a short description such as `Update research interests`, and commit directly to **main**.
5. Wait for the update to publish, then refresh [your website](https://andremellojablonski.github.io/). Publishing can take up to 10 minutes. If necessary, use Command+Shift+R on a Mac or Control+Shift+R on Windows to refresh cached files.

For example, `<p>Your biography here.</p>` creates a paragraph. `<a href="files/cv.pdf">Curriculum vitae</a>` creates a link: `href` is the destination, and the text between the tags is what visitors see.

### Upload a PDF or photo

1. In your repository, open the destination folder: **files** for PDFs or **assets** for photos.
2. Choose **Add file → Upload files**, then drag in the file or choose it from your computer.
3. Use a short filename without spaces, for example `cv.pdf`, `working-hours-brazil.pdf`, or `portrait.jpg`. Filenames and links are case-sensitive.
4. Click **Commit changes**.
5. Edit `index.html` to add a link or image using one of the examples below. Uploading a file makes it available; adding the HTML link or image makes it visible on the page.

If the **files** folder does not exist yet, choose **Add file → Create new file** from the repository's home page, enter `files/README.md` as the filename, type `Public PDFs for the academic website.`, and commit. GitHub creates the folder automatically. Then open it and upload your PDFs.

To replace a PDF, upload the new version to the same folder with the same filename and commit the replacement. Existing links will keep working. Files uploaded to this public repository are public, so use versions intended for your academic website.

### Fix a mistake

You can edit the file again and commit a correction. To recover older text, open the file and click **History**, open an earlier version, copy the text you want, then return to the current file and paste it back through the editor. Each commit preserves the previous version.

If a change does not appear, look at the repository's **Actions** tab for a failed or unfinished Pages deployment. A green check means the deployment finished successfully. Keep `index.html` in the repository root and leave `.nojekyll` in place.

## Publish on GitHub Pages

1. Sign in to GitHub as **andremellojablonski**.
2. Create a **public** repository named **andremellojablonski.github.io**. If it already exists, review its contents before replacing files.
3. Upload `index.html`, the `assets` folder, and `.nojekyll` to the repository's root on the `main` branch. You can also include this README and `.gitignore`.
4. In the repository, open **Settings → Pages**.
5. Set **Source** to **Deploy from a branch**, choose **main** and **/ (root)**, then save.
6. GitHub will publish the website at **https://andremellojablonski.github.io/**. Initial publication can take up to 10 minutes.

GitHub's instructions: [Pages quickstart](https://docs.github.com/en/pages/quickstart) and [configure a publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## Preview locally

From this folder, run:

```sh
python3 -m http.server 4173 --bind 127.0.0.1
```

Then open **http://127.0.0.1:4173/**. Press Control+C in the terminal to stop the server. You can also open `index.html` directly in a browser.

## Update the content

- **Biography, contact, and research:** edit `index.html`.
- **Colors, spacing, and typography:** edit `assets/style.css`.
- **New paper:** duplicate the `<article class="paper">` block inside the research section. Use only confirmed authors, title, and status.
- **Footer:** update the year in `index.html` when needed.

Commit changes to `main` to publish updates automatically once GitHub Pages is enabled.

### Add a portrait

Save the photo as `assets/portrait.jpg`, then insert the following just above the `<h1>` in the profile header:

```html
<img class="portrait" src="assets/portrait.jpg"
     alt="André Mello Jablonski" width="160" height="160">
```

### Add a CV

Create a `files` folder, save the PDF as `files/andre-mello-jablonski-cv.pdf`, and add this link inside the navigation:

```html
<a href="files/andre-mello-jablonski-cv.pdf">Curriculum vitae (PDF)</a>
```

### Add the research paper

Once the manuscript is ready for public sharing, save it as `files/working-hours-brazil.pdf`, then add the following below the paper status:

```html
<p class="paper-links"><a href="files/working-hours-brazil.pdf">Paper (PDF)</a></p>
```

An abstract can be inserted as a paragraph within the same article. No abstract or results have been assumed in the initial version.

## Design

Original HTML and CSS with a restrained profile-and-research layout inspired by the academic homepage of [Axelle Ferriere](https://axelleferriere.github.io/). No source code, photographs, or other assets from that site are included.
