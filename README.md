# Cabinet

**Cabinet** is a mobile-first personal style, wardrobe, and fragrance concierge. It combines a weather-aware daily stylist, a gradually built digital wardrobe, a fragrance catalog with inventory tracking, and practical shopping guidance in one iPhone-friendly web app.

It is designed to be hosted through GitHub Pages and saved to an iPhone Home Screen—no Apple Developer account, App Store submission, backend, or build process required.

## What Cabinet does

### Today

- Pulls live local weather when browser location access is allowed.
- Recommends a fragrance from your available collection using weather, season, scent intensity, and rotation history.
- Provides heat and humidity-aware spray guidance.
- Displays a wardrobe prompt that becomes a complete daily outfit recommendation as you add clothing items.

### Stylist

- Builds a complete look from your available wardrobe items.
- Uses occasion, desired presentation, current weather, season, and availability.
- Supports office, client dinner, date night, golf, casual, formal events, night out, vacation, and work travel.
- Pairs the suggested outfit with a fragrance from your current collection.
- Only recommends clothing you have actually added and marked as available.

### Wardrobe

- Lets you add wardrobe items one at a time from your iPhone.
- Supports shirts, pants, shorts, outerwear, knitwear, shoes, hats, and accessories.
- Captures item name, brand, category, color, season, best use, status, and personal styling notes.
- Supports clothing-specific status tracking:
  - Available
  - In laundry
  - At dry cleaner
  - Needs repair
  - Needs replacing
  - Seasonal storage
  - Retired / donated
- Excludes unavailable pieces from Stylist outfit suggestions.

### Fragrance

- Includes the initial fragrance collection cataloged from your photos.
- Uses stylized in-app bottle illustrations and monograms rather than third-party product images.
- Stores fragrance name, house, notes, season, occasion, vibe, strength, format, and quantity.
- Includes Room 1015 samples and nine EPC Paris discovery-set fragrances with an initial quantity of **7 each**, reflecting seven complete sample kits.
- Supports Full, Running Low, and Empty inventory status.
- Supports “Use one sample,” which decreases quantity and automatically marks the scent Low at one remaining and Empty at zero.
- Automatically moves empty fragrances to the repurchase list.
- Supports fragrance wear logging and short rotation protection.

### Shop Smart

- Shows wardrobe items marked **Needs replacing** or **Needs repair**.
- Shows fragrances marked for repurchase.
- Provides high-value, modern-classic wardrobe-gap suggestions.
- Prioritizes useful additions, replacements, and upgrades over random shopping.
- Includes recommendations suited to polished work travel, client dinners, date nights, premium golf apparel, and your brown-leather/warm-neutral style direction.
- Allows data backup export and import.

## Style direction

Cabinet starts with a tailored, modern-classic point of view:

- Polished smart casual for senior-leader work settings and client dinners.
- Premium, fashion-aware golf and travel clothing.
- Warm neutrals, navy, chocolate, olive, cream, muted blue, and brown leather.
- A wardrobe built around useful combinations, strong fit, versatile layers, and understated quality rather than disposable trends.
- Fragrance matched to weather, activity, setting, and desired presence.

## Repository contents

```text
cabinet/
├── index.html       # The complete Cabinet web app
└── README.md        # Project documentation and deployment guide
```

## Publish with GitHub Pages

### 1. Create a repository

1. Sign in to [GitHub](https://github.com).
2. Click the **+** icon in the upper-right corner.
3. Select **New repository**.
4. Name the repository:

   ```text
   cabinet
   ```

5. Add an optional description:

   ```text
   Personal style, wardrobe, and fragrance concierge.
   ```

6. Choose **Public** for the simplest free GitHub Pages setup.
7. Click **Create repository**.

### 2. Upload the app

1. Download the generated Cabinet HTML app file from the chat file panel.
2. Rename it exactly:

   ```text
   index.html
   ```

3. On the repository page, select **Add file → Upload files**.
4. Upload these two files to the repository root:

   ```text
   index.html
   README.md
   ```

5. Enter a commit message, for example:

   ```text
   Launch Cabinet personal style concierge
   ```

6. Select **Commit changes**.

### 3. Enable GitHub Pages

1. Open the repository’s **Settings** tab.
2. In the left sidebar, select **Pages**.
3. Under **Build and deployment**, choose:

   ```text
   Source: Deploy from a branch
   ```

4. Under **Branch**, select:

   ```text
   main
   ```

5. Under the folder selector, select:

   ```text
   / (root)
   ```

6. Click **Save**.
7. Wait a few minutes, refresh the page, and GitHub will display the live site URL.

It will generally look like:

```text
https://YOUR-GITHUB-USERNAME.github.io/cabinet/
```

## Install on iPhone

1. Open the published Cabinet URL in **Safari** on your iPhone.
2. Tap the **Share** button—the square with an upward arrow.
3. Scroll down and choose **Add to Home Screen**.
4. Confirm the app name as **Cabinet**.
5. Tap **Add**.
6. Launch Cabinet directly from the Home Screen icon.

The app opens in an app-like, full-screen experience. This is a web app rather than an App Store-native app, so no Apple Developer membership is required.

## Add wardrobe items

Cabinet launches with the fragrance collection populated and the Wardrobe ready for gradual entry.

1. Open **Wardrobe** from the bottom navigation.
2. Tap **+ Add item**.
3. Enter the item name, category, color, season, best use, availability, and optional styling notes.
4. Tap **Save to wardrobe**.
5. Repeat over time, starting with your most-worn shoes, pants/shorts, shirts/polos, and outerwear.
6. Open **Stylist** and tap **Build my look** once several core pieces are available.

Cabinet will never pretend you own a garment that is not in the Wardrobe. It will become more accurate as you add items.

## Inventory workflows

### Wardrobe condition

Open a wardrobe item to set its current condition:

```text
Available
In laundry
At dry cleaner
Needs repair
Needs replacing
Seasonal storage
Retired / donated
```

Items marked Needs Repair or Needs Replacing appear in Shop Smart and are excluded from outfit suggestions by default.

### Fragrance inventory

Open a fragrance to:

```text
Log wear
Use one sample
Set Full
Set Running Low
Mark Empty
Add to repurchase
```

For sample sets, “Use one sample” reduces the count. At zero, Cabinet automatically marks the fragrance Empty and adds it to the repurchase list.

## Weather and location

Cabinet requests browser location permission only when you refresh weather. It uses your approximate coordinates to request current temperature, humidity, and weather conditions from Open-Meteo.

- Allow location access for the best outfit and fragrance recommendations.
- If you decline access or weather cannot load, Cabinet still works using its seasonal logic.
- Use Safari for the best iPhone Home Screen experience.

## Data, privacy, and backup

Cabinet stores your wardrobe entries, fragrance changes, inventory levels, wear logs, and repurchase selections locally in your browser using `localStorage`.

- Your personal wardrobe additions are not automatically written to GitHub.
- Use the same Cabinet URL and browser on your iPhone to retain your data.
- Do not clear Safari website data for Cabinet unless you want to reset local data.
- Open **Shop Smart** and select **Export backup** regularly to save a JSON backup file.
- Use **Import backup** if you switch devices or need to restore the app.

A public GitHub repository exposes the app’s source code, but it does not expose the information you enter later into the browser-based app. Avoid putting sensitive data—addresses, passwords, payment information, or confidential notes—into the app fields.

## Updating Cabinet

To install an updated version of the app:

1. Open your GitHub repository.
2. Replace the root `index.html` file with the newer version.
3. Commit the update to the `main` branch.
4. Wait a few minutes for GitHub Pages to redeploy.
5. Reopen Cabinet from your iPhone Home Screen.

Your locally entered data should remain intact as long as you use the same website domain and do not clear browser data.

## Troubleshooting

### GitHub Pages shows a 404 error

- Confirm the app file is named exactly `index.html`.
- Confirm it is in the top-level repository folder, not inside another folder.
- Confirm GitHub Pages is set to `main` and `/(root)`.
- Wait several minutes after making publishing changes, then refresh.

### Weather cannot find your location

- Open Cabinet in Safari rather than an in-app browser.
- On iPhone, check **Settings → Privacy & Security → Location Services → Safari Websites**.
- Set access to **While Using the App**.
- Return to Cabinet and tap **↻ Weather**.

### Wardrobe or fragrance changes disappeared

- Verify that you are using the same browser and Cabinet URL.
- Make sure Safari is not in Private Browsing mode.
- Restore a prior JSON backup via **Shop Smart → Import backup**.

## Future roadmap

- Clothing photo capture and background cleanup.
- Better visual outfit boards.
- More sophisticated color and garment-compatibility logic.
- Saved outfits and outfit ratings.
- Cost-per-wear tracking.
- Calendar-aware event styling and trip planning.
- Cloud synchronization for multiple devices.
- Optional AI free-text concierge for deeper style coaching and shopping research.
