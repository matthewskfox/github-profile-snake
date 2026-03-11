# 🐍 github-profile-snake

Automated workflow that generates a snake animation from my GitHub contribution graph and publishes it to the `assets/snake-animations` branch for use in my profile README.

## How it works

1. The workflow runs every Sunday at 00:00 UTC (or on every push to `main`)
2. [Platane/snk](https://github.com/Platane/snk) reads the contribution graph and renders the animations
3. The output files are pushed to the `assets/snake-animations` branch via GitHub Actions

## Outputs

| File | Description |
|------|-------------|
| `github-snake.svg` | Light mode snake |
| `github-snake-dark.svg` | Dark mode snake |
| `ocean.gif` | Ocean-themed variant |

## Usage

Add one of the following to your profile README, replacing `<username>` with your GitHub username:

**Light mode**
```md
![snake](https://raw.githubusercontent.com/<username>/<repo>/assets/snake-animations/github-snake.svg)
```

**Dark / light mode switch**
```md
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/<username>/<repo>/assets/snake-animations/github-snake-dark.svg" />
  <img alt="github contribution snake" src="https://raw.githubusercontent.com/<username>/<repo>/assets/snake-animations/github-snake.svg" />
</picture>
```

## Setup

1. Fork or clone this repo
2. Go to **Settings → Actions → General** and set workflow permissions to **Read and write**
3. Push to `main` or trigger the workflow manually to generate the first animation
