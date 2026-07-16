# Setup

1. Use a public GitHub profile repository whose name exactly matches your GitHub username.
2. Copy `README.md`, `assets/banner.svg`, and `.github/workflows/metrics.yml` into that repository.
3. Create a GitHub personal access token with only the permissions required for the metrics you want to show.
4. Add the token to the profile repository as an Actions secret named `METRICS_TOKEN`.
5. Open the repository's Actions tab, select `GitHub Profile Metrics`, and run it manually once.
6. After the workflow finishes, `assets/github-metrics.svg` will be created and the analytics section will render in the README.

## Important

- Do not put your token directly inside the workflow file.
- The workflow automatically uses the repository owner's username through `${{ github.repository_owner }}`.
- If you want private-repository statistics, the token needs suitable access to those repositories.
- If the metrics image does not appear, inspect the workflow log first. Plugin permission errors are usually shown there.
