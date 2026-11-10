# Shiftbook

A monthly shift-hours tracker with two separate calculations:

- **Shift hours**: hours per shift, working days, leave, overtime and your pay per hour.
- **Off working days**: your company's official holiday calendar (added one by one or pasted as a list), the holidays you worked, and your pay per off working day.

The top of the page shows both monthly earnings and their total.

It's a static site with no build step and no backend. Data is saved in each visitor's own browser (localStorage).

## Project structure

```
shiftbook/
├── public/
│   ├── index.html            the whole app (HTML, CSS and JavaScript)
│   ├── favicon.svg           site icon
│   └── manifest.webmanifest  lets phones add it to the home screen
├── vercel.json               tells Vercel to serve the public folder
├── .gitignore
└── README.md
```

## Deploy to Vercel

1. Create a new repository on GitHub and upload the contents of this folder, keeping the same structure.
2. In Vercel, choose **Add New → Project** and import that repository.
3. Leave **Framework Preset** as **Other**, with no build command. `vercel.json` already points to the `public` folder.
4. Click **Deploy**.

Every push to the main branch redeploys automatically.

## Run locally

Open `public/index.html` in a browser, or serve the folder:

```
npx serve public
```

## Notes

- Data lives in the browser, so it isn't shared between devices or browsers. Clearing browser data removes it.
- Fonts load from Google Fonts. Everything else is self-contained.
