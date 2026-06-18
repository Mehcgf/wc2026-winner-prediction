# WC 2026 — Winner Prediction 🏆

Hey, I'm Mehmet — a Data Science from Germany.

The FIFA World Cup 2026 is live and I couldn't resist building something 
with it. So I wrote a Monte Carlo simulation that predicts the most likely 
winner based on real data.

The idea is simple: simulate the full tournament 10,000 times and see who 
wins most often. Football is random — but over 10,000 runs, patterns emerge.

---
## How it works

Every match is simulated using the Poisson distribution, which is the 
standard statistical model for football goals. The expected goals per team 
are calculated from three data sources combined:

- **WM match history 1930–2022** — how strong is each nation historically?
- **FIFA Ranking June 2026** — where do they stand right now?
- **EA FC 26 squad ratings** — how good are the current players?

The tournament runs from group stage all the way to the final — 10,000 times.

---
## Results

| Rank | Team | Win Probability |
|------|------|----------------|
| 🥇 | Brazil | 14.74% |
| 🥈 | France | 13.09% |
| 🥉 | Argentina | 10.36% |
| 4 | England | 8.93% |
| 5 | Portugal | 8.06% |
| 6 | Spain | 7.80% |
| 7 | Germany | 7.45% |
| 8 | Netherlands | 6.61% |

---
## What's interesting

100 simulations are not enough — the results jump around too much. 
Only after around 2,500 runs do the probabilities start to stabilize. 
The stability diagram in this repo shows exactly that.

---
## Data sources
Download these files from Kaggle and place them in the same folder 
as the notebook:

- `matches_1930_2022.csv` — [Football FIFA World Cup 1930–2026](https://www.kaggle.com/datasets/piterfm/fifa-football-world-cup)
- `fifa_ranking_2026-06-08.csv` — same dataset
- `schedule_2026.csv` — same dataset
- `FC26_20250921.csv` — [EA FC 26 Player Ratings](https://www.kaggle.com/datasets/rovnez/fc-26-fifa-26-player-data)

---
## Tech stack
Python · Pandas · NumPy · Matplotlib · Jupyter Notebook


## Author
**Mehmet Cagferoglu**
Data Science Student · Germany
[LinkedIn](https://www.linkedin.com/in/mehmet-cagferoglu)

---

*Greetings from Germany 🇩🇪 — let's see if Brazil actually pulls it off.*
