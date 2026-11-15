# Plot Your Past Bosses (Leadership Grid)

An in-class activity for PSY170. Students name three bosses, rate each one on 8 behavior questions (4 consideration items and 4 initiating structure items), and see all three plotted on Blake and Mouton's Leadership Grid. They then copy those spots into a Top Hat click-on-target question.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole student app. One file, no outside fonts, libraries, or network requests. Nothing is collected or sent anywhere. |
| `index.html?grid` | Instructor view: the blank grid with Download SVG and Download PNG buttons. |
| `blank-grid.svg` | Blank grid for Top Hat (vector, sharp at any size). |
| `blank-grid.png` | Blank grid for Top Hat, 2000 x 2000 px. |

## Deploy

1. Commit and push this folder to the PSY170 repo on GitHub.
2. Netlify redeploys automatically. The app is at your site's address plus `/Leadership%20Grid%20Survey/` (the space in the folder name becomes `%20`).
3. Open the link on your phone once to check it, then share it with students.

Answers are kept in the browser tab's session storage only, so an accidental refresh doesn't erase them. Closing the tab clears them.

## Set up the Top Hat question

1. Create a click-on-target question and upload `blank-grid.png` (or `blank-grid.svg` if Top Hat accepts it).
2. Don't crop the image. It is square and has the same margins as the grid in the app, so positions line up when students copy them by eye.
3. If one question can't take three clicks per student, make three questions (Boss 1, Boss 2, Boss 3) with the same image.

## Regenerate the grid images

The grid in the app, the `?grid` view, and both image files all come from the same drawing function (`LG.draw` in the `grid-lib` script inside `index.html`). If you change anything about the grid, regenerate both images so Top Hat still matches the app:

1. Open `index.html?grid` in a desktop browser (the deployed site or the local file both work).
2. Click **Download SVG** and **Download PNG**.
3. Replace `blank-grid.svg` and `blank-grid.png` in this folder with the downloaded files, and re-upload the image to Top Hat.

## Scoring (for reference)

- Relationship score = mean of R1 to R4. Task score = mean of T1 to T4. Both are on the 1 to 5 answer scale.
- Each mean is converted to the 1 to 9 grid: `grid = 1 + 2 x (mean - 1)`, so 1 becomes 1, 3 becomes 5, and 5 becomes 9.
- Quadrants are split at 5. A score of exactly 5 is reported as "on the line between" the two neighboring styles, and (5, 5) as the center of the grid.
- If bosses land on the same or nearly the same spot, the markers are spread apart slightly and a dot with a short line marks the exact spot. The score cards always show the exact values.
