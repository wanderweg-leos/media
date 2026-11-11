# Wanderweg Leonbergers – photos and videos

Every photo and video used on the Wanderweg website. The site itself lives in
[`wanderweg-leos/wanderweg-leos.github.io`](https://github.com/wanderweg-leos/wanderweg-leos.github.io).

GitHub Pages publishes this repository at **`/media/`** on the same website, so
`img/gallery/snow.jpg` here appears on the site as `/media/img/gallery/snow.jpg`
(today at `https://wanderweg-leos.github.io/media/…`, and at `https://wanderweg.ca/media/…`
once the domain is switched over; nothing here needs to change when that happens).

## Folders

| Folder | Holds | Used by |
|---|---|---|
| `img/` | the big photos on the home page and thank-you page | `_data/home.yml`, `_data/questionnaire.yml` |
| `img/gallery/` | the "Life with Leos" gallery | `_data/gallery.yml` |
| `img/leos/` | one photo per dog in the Our Leos section | `_data/leos.yml` |
| `img/litter/` | the mother and father of the current litter | `_data/litter.yml` |
| `img/blog/<post>/` | full-size photos for each old blog post, in post order | the post's file in `_posts/` |
| `img/blog-thumbs/<post>.jpg` | small thumbnail for each post in the blog archive list | `thumb:` in the post |
| `video/blog/` | the six old blog videos, each `.mp4` with a matching `.jpg` still | `{% include video.html %}` in posts |

The blog photos are full size: wherever the old Blogger blog had a bigger copy than
Wix, the Blogger original is used.

## Adding a photo

1. Resize it to about 1400 pixels wide (not needed for blog photos), and give it a
   simple name with no spaces, like `riley-beach.jpg`. Names are case-sensitive:
   `Riley.JPG` and `riley.jpg` are different.
2. Open the right folder here on GitHub and click **Add file → Upload files**.
3. In the site repository, edit the matching `.yml` file to use the new name.

Don't rename or delete a photo the site still uses, or it will show as an empty grey box.

## Setup

**Settings → Pages**: deploy from branch **main**, folder **/ (root)**. The repository
must be public. The empty `.nojekyll` file tells GitHub to publish the files as they are,
without processing them.
