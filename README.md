# Upper Body Strength

A simple, phone-friendly web app that guides you through an upper-body strength routine: two alternating workouts, a rest timer between sets, and progress tracking. Everything runs in the browser, with no account, server or sign-up.

## Features

- **Two alternating workouts.** Workout A (push focus) and Workout B (pull focus), about 20–25 minutes each. The app suggests whichever one is next, and you can pick the other instead.
- **Four equipment modes.** Dumbbells, resistance band, bodyweight, or mix & match. Every exercise has a version for each type of equipment. In mix & match mode you choose the equipment exercise by exercise, and the app remembers your choices.
- **Dumbbell weights.** Each exercise has its own weight, starting at 3 lb and going up in steps (3, 5, 8, 10, 12, 15, 20, 25 lb). After a workout, the app offers to raise the weight for anything you're ready to go heavier on.
- **Band tension.** Track light, medium, heavy or extra-heavy bands for each exercise.
- **Guided sets.** Big tap targets, a set checklist, form tips, and an automatic rest timer of 30, 45 or 60 seconds (you can pause it, skip it, or add or remove 15 seconds). Planks have their own countdown timer.
- **Weekly goal.** Choose 1–7 strength sessions a week and track them on the home screen.
- **Progress charts.** Workouts per week over the last 12 weeks compared with your goal, your streak of weeks that hit the goal, and a chart of dumbbell weight over time for each exercise.
- **Notes.** Add a note at the end of each workout about how it felt.
- **Keeps the screen on** during a workout, where the browser allows it.
- **Backup and restore.** Copy or download your data and restore it on another device.

## Your data

Workout history and settings are saved in your browser's local storage on your own device. Nothing is sent anywhere.

- Each browser and device keeps its own separate data. Use **Settings → Backup and restore** to move your history between them.
- Clearing your browser's website data erases your history, so make a backup now and then.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: layout, styles and code |
| `manifest.webmanifest` | App name, colors and icons for installing on a phone |
| `icon-192.png`, `icon-512.png` | App icons (Android and browser tabs) |
| `apple-touch-icon.png` | Home-screen icon for iPhone and iPad |

## Hosting on GitHub Pages

1. Create a repository and upload all the files above to the top level of the repository (not inside a folder).
2. Go to **Settings → Pages**, choose **Deploy from a branch**, then select `main` and `/ (root)`, and save.
3. After a minute or two, the app is live at `https://<your-username>.github.io/<repository-name>/`.

GitHub Pages on a free account requires a public repository. The code is public, but your workout data never leaves your device.

## Installing on your phone

- **iPhone or iPad (Safari):** tap Share → **Add to Home Screen**.
- **Android (Chrome):** tap the ⋮ menu → **Add to Home screen** or **Install app**.

The app then opens full-screen from its own icon, like a regular app.

## Changing the workouts

The exercises are defined near the top of the `<script>` section in `index.html`, in the object named `W`. Each exercise lists its sets, reps and a version for each type of equipment:

```js
{id:'curl', sets:3, reps:'10–12', rest:1, def:'db', v:{
  db:   {name:'Biceps curls', tip:'Elbows stay at your sides; lower slowly.'},
  band: {name:'Band curls',   tip:'Stand on the band, curl handles to shoulders.'},
  bw:   {name:'Towel isometric curls', tip:'Stand on a towel, curl up against it and hold.'}}}
```

- `def` is the equipment that mix & match mode uses by default (`db`, `band` or `bw`).
- Keep each `id` the same after you've logged workouts, because history, weights and charts are linked to it.

## The program

Three strength sessions a week (or your own goal), alternating A and B, with 30–60 seconds of rest between sets. Pair them with active recovery (running, hiking, biking) about three times a week and yoga or rest once a week. When you can do every set at the top of the rep range with good form, move up a weight or a harder variation.
