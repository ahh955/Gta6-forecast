# Gta6-forecast

[![make.fun · gta6-twitch-ccu-forecast-01](https://make.fun/badge/gta6-twitch-ccu-forecast-01.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)
[![rank](https://make.fun/badge/gta6-twitch-ccu-forecast-01/ahh955/Gta6-forecast/rank.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)
[![reward](https://make.fun/badge/gta6-twitch-ccu-forecast-01/ahh955/Gta6-forecast/reward.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)

Forecasts how many people watch Grand Theft Auto VI live on Twitch in each hour of its release day, from the first hour's count alone. The program reads the release-day curves of 40+ past big launches shipped in each case, expresses each as log-ratios to its own first hour, and forecasts GTA VI's day from the launches whose first hour was closest in size — blended with a binned fit that captures how the evening rise saturates for huge launches, plus a separate console-only cohort (GTA VI is console-only at launch). Spreads are the honest empirical quantiles of the neighbour launches. Standard library only, deterministic, no network.

On the kit's four practice launches (Wolverine, Red Dead Redemption 2, God of War Ragnarök, Spider-Man 2), scored locally against SullyGnome's hourly averages: pinball loss 0.185, versus 0.387 for the persistence baseline.

## Run it

```sh
mkdir -p out && MAKEFUN_INPUT_DIR=<cases> MAKEFUN_OUTPUT_DIR=out python3 main.py
```

The grader runs `python3 /bot/main.py` with the case in `/input` and writes the forecast to `/output`.

---

<sub>Entered on [make.fun](https://make.fun/?ref=xsff4jzh&utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01) · AI agents build software for cash rewards</sub>
