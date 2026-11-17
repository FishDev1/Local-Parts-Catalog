# Local Parts Catalog

A browser-based parts catalog for production. Search parts by **Part Number** or **Description**, add new parts with a photo, and export the catalog to Excel.

The page is hosted on GitHub Pages, but **all catalog data stays on the network drive**. This repo contains only the web page. It has no part data or images.

## Open the Catalog

**https://<username>.github.io/parts-catalog/**

> Use **Chrome** or **Edge**. Other browsers can't connect to the shared folder.

## First-Time Setup

1. Open the Catalog link above.
2. Press **Choose Shared Folder**.
3. Browse to the shared **Local Parts Catalog** folder on the network drive.
4. Select the folder and press **Select Folder**.
5. Allow access when the browser asks.
6. Verify the status box turns **green**. Green means the page is in sync and saving.

> You only need to do this once per computer and browser. If the connection drops, press **Reconnect**.

## Add a Part

1. Enter the **Part Number** and **Description**.
2. Press **Choose File** and select the picture.
3. Press **Add Part** when you're done with the entry.

Pictures save automatically to the `images` folder on the network drive.

## Edit or Delete a Part (Admin Mode)

1. Add `#admin` to the end of the page URL and refresh:
   `https://<username>.github.io/parts-catalog/#admin`
2. Edit or delete entries as needed.
3. When you're done, remove `#admin` and reload the page.

> **WARNING:** Deleting an entry also **DELETES the photo** linked to it. Don't delete entries if you want to keep the image.

## Backups

- **Export / Import:** Manually back up or restore the `.json` save file.
- **Export to Excel:** Creates an Excel copy of the catalog.

> Occasionally save a backup to the **Manual Backups** folder. Don't rely on a single save file!

## Where the Data Lives

| Item | Location |
|---|---|
| Web page (`index.html`) | This GitHub repo |
| Catalog save file (`parts-catalog.json`) | Shared Catalog folder on the network drive |
| Part pictures | `images` folder inside the shared Catalog folder |
| Manual backups | `Manual Backups` folder inside the shared Catalog folder |

> The catalog only works on the plant network. Off the network, the page will load but no parts will show.

## Updating the Page

1. Edit `index.html`.
2. Commit and push to `main`.
3. GitHub Pages republishes the site in about a minute. Refresh the page to see the changes.

**Never commit `parts-catalog.json`, images, or backups to this repo.** The `.gitignore` file blocks them.
