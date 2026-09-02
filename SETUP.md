# GitHub Profile README — Local Stats Setup

## Files

- `README.md` — updated profile README using local SVG files.
- `.github/workflows/update-profile-cards.yml` — scheduled GitHub Actions workflow.
- `profile/` — generated SVG cards will be stored here.

## Setup

1. Your GitHub profile repository must be named exactly:
   `shivshikharsinha/shivshikharsinha`

2. Copy the contents of this package into that repository.

3. Commit and push the files.

4. Open:
   **GitHub → Repository → Settings → Actions → General**

5. Under **Workflow permissions**, select:
   **Read and write permissions**

6. Save the setting.

7. Open the repository's **Actions** tab.

8. Select **Update GitHub Profile Cards**.

9. Click **Run workflow**.

The workflow is also scheduled to run daily.

## Important note about the streak card

The stats and trophy cards are generated as SVG files and committed into the repository, so the README itself loads those files directly from GitHub.

The streak card in this version is fetched during the workflow run and saved locally as `profile/streak.svg`. It therefore still depends on the streak service being available when the workflow runs. If you want, this can also be replaced with a fully self-contained GitHub-API-based streak generator later.

## Result

Your README displays:

```text
./profile/stats.svg
./profile/top-langs.svg
./profile/streak.svg
./profile/trophy.svg
```

instead of making the GitHub profile page request the public stats/trophy endpoints every time someone views your profile.
