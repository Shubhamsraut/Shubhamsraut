# Hi there 👋, I'm Shubham

<p>
  <img src="https://komarev.com/ghpvc/?username=Shubhamsraut&label=Profile%20views&color=0e75b6&style=flat" alt="profile views"/>
</p>

### 💡 About Me

Business Analyst with **2+ years** of experience turning business questions into actionable decisions. I partner with product, sales, and ops to define KPIs, build self‑serve dashboards, and deliver clear narratives that move the needle.

I’m also leaning hard into the **automation era**—using Python/SQL scripts, scheduled notebooks, and lightweight agents to remove repetitive work, trigger proactive alerts, and keep stakeholders in the loop.

**Focus areas**

* KPI design & metric governance
* Experimentation (A/B test design, lift analysis, readouts)
* Cohort/retention and funnel diagnostics
* Automation: GitHub Actions, Apps Script/Power Automate, Zapier/n8n; exploring LLM‑powered agents for data QA & report drafting

---

### 🧰 Analytics Toolkit

<p>
  <img src="https://img.shields.io/badge/Power%20BI-F2C811?logo=Power%20BI&logoColor=black"/>
  <img src="https://img.shields.io/badge/Tableau-E97627?logo=Tableau&logoColor=white"/>
  <img src="https://img.shields.io/badge/Looker-4285F4?logo=looker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Excel-217346?logo=microsoft-excel&logoColor=white"/>
  <img src="https://img.shields.io/badge/Google%20Sheets-34A853?logo=google-sheets&logoColor=white"/>
  <img src="https://img.shields.io/badge/BigQuery-4285F4?logo=google-bigquery&logoColor=white"/>
  <img src="https://img.shields.io/badge/Snowflake-29B5E8?logo=snowflake&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white"/>
</p>

---

### 🗣️ Languages

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/SQL-336791?logo=postgresql&logoColor=white"/>
</p>

---

### 🧭 What I Do

* 📊 KPI design & business performance tracking
* 🧹 Data wrangling, modeling, and documentation
* 📈 Dashboarding & self‑serve analytics (Power BI/Tableau/Looker)
* 🧪 Experimentation: A/B test design, lift analysis, and readouts
* 🔮 Forecasting & cohorts: time series, retention, segmentation
* 🤝 Stakeholder storytelling: clear narratives, executive reports

---

### 📊 Analyst Dashboard (Auto‑Generated)

> A living dashboard that updates from my public repos: languages, heatmap, habits, topics, lines added/removed, and highlights.

<div align="center">
  <img src="./github-metrics.svg" alt="Core metrics" width="49%"/>
  <img src="./analytics-habits.svg" alt="Habits & heatmap" width="49%"/>
</div>
<p align="center">
  <img src="./achievements.svg" alt="Achievements" width="98%"/>
</p>

<p>
  <img src="https://img.shields.io/github/followers/Shubhamsraut?label=Followers"/>
  <img src="https://img.shields.io/github/stars/Shubhamsraut?affiliations=OWNER&label=Stars"/>
  <img src="https://komarev.com/ghpvc/?username=Shubhamsraut&label=Profile%20views&color=0e75b6&style=flat"/>
</p>

---

### 📊 GitHub Stats

<p>
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=Shubhamsraut&show_icons=true&theme=default&rank_icon=github" />
  <img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Shubhamsraut&layout=compact" />
</p>
<p>
  <img height="160" src="https://streak-stats.demolab.com?user=Shubhamsraut" />
</p>

---

### 🤝 Connect with Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin\&logoColor=white)](https://www.linkedin.com/in/shubham-raut-analytics)

---

### ⭐ Featured Work (Case Studies)

* **Cohort Retention Dashboard (Power BI/Tableau):** acquisition → activation → retention with filters by channel/segment.
* **Sales Funnel Diagnostic (SQL + Looker):** conversion drop‑off, anomaly alerts, and revenue impact.
* **A/B Test Readout Template (Python/Notebook):** design → checks → lift & power → final recommendations.

> Replace these with links to your repos or BI public gallery.

---

### 🏃 Recent GitHub Activity

<!--START_SECTION:activity-->

<!--END_SECTION:activity-->

---

### 🧩 Fun Extras

* 🔭 Currently working on: self‑serve dashboards & metric definitions
* 🌱 Learning: causal inference & experimentation best practices
* 💬 Ask me about: analytics strategy, A/B testing, dashboard UX
* 📫 How to reach me: LinkedIn above

---

## .github/workflows/metrics.yml

```yaml
name: Generate metrics cards

on:
  schedule:
    - cron: "30 2 * * *"   # daily 02:30 UTC
  workflow_dispatch:

permissions:
  contents: write

jobs:
  metrics:
    runs-on: ubuntu-latest
    steps:
      # 1) Core profile metrics (languages, topics, follow-up)
      - name: Core metrics
        uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
          user: Shubhamsraut
          filename: github-metrics.svg
          template: classic
          base: header, activity, repositories, metadata
          config_timezone: Asia/Kolkata
          plugin_languages: yes
          plugin_languages_sections: most-used, recently-used
          plugin_languages_limit: 8
          plugin_languages_ignored: Jupyter Notebook
          plugin_topics: yes
          plugin_topics_limit: 12
          plugin_followup: yes
          committer_branch: main
          committer_message: "chore: update core metrics"
          output_action: commit

      # 2) Analyst habits dashboard (heatmap, habits, lines, optional traffic)
      - name: Habits & heatmap
        uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
          user: Shubhamsraut
          filename: analytics-habits.svg
          template: classic
          base: header
          config_timezone: Asia/Kolkata
          plugin_isocalendar: yes
          plugin_isocalendar_duration: full-year
          plugin_habits: yes
          plugin_habits_facts: yes
          plugin_habits_charts: yes
          plugin_lines: yes
          # Uncomment next line if your PAT has `repo` scope to enable traffic graphs
          # plugin_traffic: yes
          committer_branch: main
          committer_message: "chore: update habits metrics"
          output_action: commit

      # 3) Achievements strip (compact)
      - name: Achievements
        uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
          user: Shubhamsraut
          filename: achievements.svg
          template: classic
          base: ""
          config_timezone: Asia/Kolkata
          plugin_achievements: yes
          plugin_achievements_threshold: C
          plugin_achievements_display: compact
          plugin_achievements_secrets: yes
          committer_branch: main
          committer_message: "chore: update achievements"
          output_action: commit
```

## .github/workflows/activity.yml (optional)

```yaml
name: Update recent activity

on:
  schedule:
    - cron: "45 2 * * *"   # daily
  workflow_dispatch:

permissions:
  contents: write

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Generate Activity
        uses: Readme-Workflows/recent-activity@v2
        with:
          GH_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          COMMIT_MSG: "chore: update recent activity"
```

### One-time setup for metrics

1. Create a **classic Personal Access Token**. Start with `public_repo`; if you enable `plugin_traffic`, use full `repo` scope.
2. In your repo **Shubhamsraut/Shubhamsraut** → **Settings → Secrets and variables → Actions** → **New repository secret**

   * Name: `METRICS_TOKEN`
   * Value: *your PAT*
3. Commit these workflow files and run **Generate metrics cards** once from the **Actions** tab.
4. The three SVGs will appear at the repo root and render in the README automatically.
