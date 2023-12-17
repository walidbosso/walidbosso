name: WakaTime status update

on:
  schedule:
    # Runs at 12 am  '0 0 * * *'  UTC
    - cron: "1 0 * * *"

jobs:
  update-readme:
    name: Update the WakaTime Stat
    runs-on: ubuntu-latest
    steps:
      # Use avinal/Profile-Readme-WakaTime@<latest-release-tag> for latest stable release
      # Do not change the line below until you have forked this repository
      # If you have forked this project you can use <username>/Profile-Readme-WakaTime@master instead
      - uses: avinal/Profile-Readme-WakaTime@master
        with:
          # WakaTime API key stored in secrets, do not directly paste it here
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          # Automatic github token
          GITHUB_TOKEN: ${{ github.token }}
          # Branch - newer GitHub repositories have "main" as default branch, change to main in that case, default is master
          BRANCH: "master"
          # Manual Commit messages - write your own messages here
          COMMIT_MSG: "Automated Coding Activity Update :alien:"
          # Range of fetching data - default is "last_7_days". See https://wakatime.com/developers#stats for more options
          STATS_RANGE: "last_7_days"
