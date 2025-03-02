# Google Calendar Analysis Notebook

## Overview

This notebook was used to write the blog post [A Year in Time: My 2024 Google Calendar Analysis](https://eltsai.github.io/posts/2025/03/gcal-analysis/), which analyzes how I spent my time in 2024 based on my Google Calendar data. The `gcal_analysis_2024.ipynb` etches, processes, and visualizes event data, generating insights on time spent across categories, word clouds, and monthly hour distributions. It can also be adapted for other years.

![](imgs/2024_gcal_overview.png)

I use four major categories of events in my Google Calendar:

<ul>
  <li><span style="color: #E57373;">&#11044;</span> <strong>Important and Urgent</strong> – Tasks that require immediate attention, such as projects, meetings, or deadlines.</li>
  <li><span style="color: #7986CB;">&#11044;</span> <strong>Important and Not Urgent</strong> – Long-term projects, deep work, and research that significantly impact my goals but don’t have immediate deadlines.</li>
  <li><span style="color: #FBC02D;">&#11044;</span> <strong>Not Important and Urgent</strong> – Tasks that feel time-sensitive but aren’t truly meaningful, like administrative work, responding to emails, job applications, and Leetcode.</li>
  <li><span style="color: #64B5F6;">&#11044;</span> <strong>Not Important and Not Urgent</strong> – Activities that are neither urgent nor that important, such as housework, grocery shopping, low-priority work stuff, and Duolingo.</li>
</ul>

<p>In addition to these main categories, I also track specific event types:</p>

<ul>
  <li><span style="color: #D32F2F;">&#11044;</span> <strong>Life Events</strong> – I wanted to use this as major personal milestones. However, it turned out to be only used for medical appointments and stuff like that.</li>
  <li><span style="color: #43A047;">&#11044;</span> <strong>Fun Stuff</strong> – Leisure activities, hobbies, and planned social time.</li>
  <li><span style="color: #388E3C;">&#11044;</span> <strong>Family</strong> – Dedicated time spent with family members.</li>
  <li><span style="color: #8E24AA;">&#11044;</span> <strong>Exercise</strong> – Workouts and other physical activities.</li>
</ul>

## Features

- Fetches events from Google Calendar using OAuth 2.0 authentication.
- Analyzes event data to calculate total hours spent on various categories.
- Generates a word cloud visualization of event summaries.
- Provides insights into event distribution over weeks and months.

## Requirements

To run this project, you need the following Python packages:

- `pytz`
- `matplotlib`
- `pandas`
- `collections`
- `statistics`
- `google-auth`
- `google-auth-oauthlib`
- `google-api-python-client`

You can install the required packages using pip:

```bash
pip install pytz matplotlib pandas google-auth google-auth-oauthlib google-api-python-client
```

## Setup

1. **Clone the Repository:**

   Clone this repository to your local machine:

   ```bash
   git clone git@github.com:eltsai/gcal_analysis.git
   cd gcal_analysis
   ```

2. **Google Calendar API Setup:**

   - Go to the [Google Cloud Console](https://console.cloud.google.com/).
   - Create a new project.
   - Enable the Google Calendar API for your project.
   - Create OAuth 2.0 credentials and download the `credentials.json` file.
   - Place the `credentials.json` file in the project directory.

3. **Run the Jupyter Notebook:**

   Open `gcal_analysis_2024.ipynb` and run the cells to fetch and analyze your Google Calendar events.

## Usage

- The notebook is structured into several sections:
  - **Fetch Data From Google Calendar:** This section handles authentication and fetching events.
  - **Load Data:** Loads the fetched event data from a JSON file (you'll probably need to rewrite the mapping between color and category).
  - **Data Analysis:** Analyzes the events to calculate total hours spent on different categories.
  - **Visualizations:** Generates visualizations such as word clouds and monthly hour distributions.

## Important Notes

- Ensure that you have the necessary permissions to access your Google Calendar data.
- The project includes a `.gitignore` file to exclude sensitive files like `credentials.json` and any generated data files.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.