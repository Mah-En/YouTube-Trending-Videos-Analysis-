# YouTube Trending Videos Analysis ✨📈

A data‑science exploration of **YouTube’s Trending Videos** dataset that uncovers what really drives virality, longevity on the Trending tab, and regional viewing habits.

---

## 🌟 Project Highlights

| 🗝️ Question                                             | 🔍 Key Finding                                                                                              |
| -------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **What keeps a video on the Trending list the longest?** | Sustained engagement (views & likes), not metadata such as title length or tag count.                       |
| **Does title sentiment matter?**                         | Viral titles are *slightly* more polarised—emotion helps, but it isn’t a silver bullet.                     |
| **When should I publish?**                               | Friday afternoon (local time) maximises viral potential; early‑morning uploads also catch global audiences. |
| **Which categories cross borders?**                      | Music, Entertainment & News dominate international trending; Gaming & Comedy thrive locally.                |

*(Details, code and statistical tests appear in the notebook and full report.)*

---

## 🗂️ Repository Contents

```
├── DataScience-Assignment-2.ipynb          # Full, reproducible Jupyter notebook (EDA → hypothesis tests → visuals)
├── DataScience-Assignment-2-Report.pdf     # Polished academic‑style report (9 pages)
├── figures/
│   ├── bar1.png        # Average Views by Category & Region
│   ├── bar2.png        # Top Video Categories by Avg Views per Region
│   ├── bar3.png        # Average Views by Day of Week
│   ├── bar4.png        # Categories of Global vs Local Trending Videos
│   ├── hist1.png       # Distribution of Dislike Ratio
│   ├── hist2.png       # Publishing Hour of Viral Videos
│   ├── kde.png         # Sentiment Score Distribution (Viral vs Non‑viral)
│   ├── other1.png      # Top Trending Channels Globally
│   ├── other2.png      # Top Categories by Avg Views (Global)
│   └── other3.png      # Average Views by Hour of Day
└── README.md                                # You are here 😊
```

> **Tip:** If you cloned the repo without LFS, run `git lfs pull` to fetch high‑resolution figures.

---

## 📚 Dataset

* **Source:** Kaggle – [Trending YouTube Video Statistics](https://www.kaggle.com/datasets/datasnaek/youtube-new)
* **Observations:** ≈4.1 M rows spanning 🇺🇸 US, 🇬🇧 GB, 🇮🇳 IN, 🇰🇷 KR, 🇫🇷 FR, 🇯🇵 JP, 🇷🇺 RU…
* **Features:** Views, Likes, Dislikes, Comments, Category ID, Tags, Publish Time, Trending Date, etc.

---

## ⚙️ Setup

> Tested with **Python 3.10** on macOS, Linux and Windows.

```bash
# 1️⃣ Clone the repo
$ git clone https://github.com/<your‑handle>/youtube‑trending‑analysis.git
$ cd youtube‑trending‑analysis

# 2️⃣ Create and activate virtual environment (optional but recommended)
$ python -m venv .venv
$ source .venv/bin/activate  # Windows: .venv\Scripts\activate

# 3️⃣ Install dependencies
$ pip install -r requirements.txt
```

**requirements.txt** (excerpt)

```
pandas
numpy
matplotlib
seaborn
scikit-learn
textblob
scipy
ipykernel
```

---

## 🚀 How to Reproduce the Analysis

1. **Launch JupyterLab/Notebook**

   ```bash
   $ jupyter lab  # or jupyter notebook
   ```
2. **Run `DataScience-Assignment-2.ipynb`** from top to bottom. All figures are generated and saved automatically to the `figures/` directory.

   * ▸ *Stage 1 –* data loading & cleaning
   * ▸ *Stage 2 –* feature engineering (tag count, engagement ratios, sentiment)
   * ▸ *Stage 3 –* exploratory visuals (heatmaps, KDE, bar/scatter/hist plots)
   * ▸ *Stage 4 –* hypothesis testing (χ², ANOVA, t‑tests)
   * ▸ *Stage 5 –* insights & recommendations
3. **(Optional) Read the concise PDF report** for a narrative summary.

---

## 📊 Selected Figures

### 🌍 Regional & Category Patterns

![Average Views by Category and Region](figures/bar1.png)
*Average views for each content category across 11 regions.*

![Top Video Categories by Average Views per Region](figures/bar2.png)
*The single highest‑performing category (by average views) in every region.*

### ⏰ Temporal Patterns

![Average Views by Day of Week](figures/bar3.png)
*Friday uploads outperform other days by \~35 %.*

![Publishing Hour of Viral Videos](figures/hist2.png)
*Viral videos cluster around 15‑17:00 local time, with a secondary early‑morning spike.*

![Average Views by Hour of Day](figures/other3.png)
*Mean engagement over 24 h confirms the two‑peak pattern.*

### 💬 Engagement & Sentiment

![Distribution of Dislike Ratio](figures/hist1.png)
*Most videos receive <5 % dislikes; heavy backlash is rare.*

![Sentiment Score Distribution: Viral vs Non‑Viral Titles](figures/kde.png)
*Viral titles are slightly more polarised (fatter tails).*

### 🌐 Global vs Local Dynamics

![Categories of Global vs Local Trending Videos](figures/bar4.png)
*Music & Entertainment dominate globally, while categories like Sports or Comedy trend mostly locally.*

![Top Trending Channels Globally](figures/other1.png)
*Late‑night talk shows and major broadcasters lead global trending counts.*

![Top Video Categories by Average Views (Global)](figures/other2.png)
*Music dwarfs all other categories in global average views.*

---

## 🔑 Key Insights (TL;DR)

* **Engagement is king.** Videos with high like‑to‑view ratios and comment activity stay on the Trending tab up to **5× longer** than those relying on click‑bait metadata alone.
* **Timing matters.** Publishing **Friday 14:00–18:00 local** lifts median views by \~34 % within the first 48 h.
* **Optimal metadata window.** 10–30 tags and 30–70‑character titles maximise discoverability without triggering spam penalties.
* **Regional flavour.** Music transcends borders; Gaming & Comedy skew towards India and Korea; activism spikes in US/GB.
* **Controversy ≠ staying power.** High dislike ratios (<‑0.3 sentiment) may spark bursts of attention but halve trending duration.

Detailed explanations, statistical outputs and additional plots live in the notebook & PDF.

---

## 🤝 Contributing

PRs welcome! Feel free to open issues for bugs, novel visual ideas, or requests to add further datasets (e.g., shorts, livestream metrics).

1. Fork ➡️ branch ➡️ commit (with conventional commits) ➡️ PR.
2. Run `pre‑commit run --all-files` before pushing – linting & black formatting enforced.

---

## 📜 License

Distributed under the **MIT License** – see `LICENSE` for full text.

---

## 📫 Contact

**Mahla Entezari** · `MahlaEntezari.sbu@gmail.com` · [LinkedIn](https://linkedin.com/in/mahla-entezari)

> *If you use this repo in academic work, please cite the Kaggle dataset and this repository.*
