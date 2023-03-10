#### Eastern Conference

| Team                |   W |   L | Last10Games   |
|:--------------------|----:|----:|:--------------|
| Milwaukee Bucks     |  48 |  19 | 8W2L          |
| Boston Celtics      |  47 |  21 | 6W4L          |
| Philadelphia 76ers  |  45 |  22 | 7W3L          |
| Cleveland Cavaliers |  43 |  27 | 5W5L          |
| New York Knicks     |  40 |  30 | 7W3L          |
| Brooklyn Nets       |  39 |  29 | 5W5L          |
| Miami Heat          |  37 |  33 | 4W6L          |
| Atlanta Hawks       |  34 |  35 | 5W5L          |

#### Western Conference

| Team                   |   W |   L | Last10Games   |
|:-----------------------|----:|----:|:--------------|
| Denver Nuggets         |  46 |  22 | 6W4L          |
| Memphis Grizzlies      |  41 |  26 | 6W4L          |
| Sacramento Kings       |  40 |  26 | 8W2L          |
| Phoenix Suns           |  37 |  30 | 7W3L          |
| LA Clippers            |  36 |  33 | 5W5L          |
| Minnesota Timberwolves |  35 |  34 | 4W6L          |
| Golden State Warriors  |  35 |  33 | 6W4L          |
| Dallas Mavericks       |  34 |  35 | 3W7L          |

The `nba-standings-python` repo is last updated on *2023-03-13*

---

## How it works
The script uses an `API key` that is stored in a GitHub secret to authenticate with the `Rapid API`. The API key is passed as an environment variable to the script, which then uses it to make the API request. The script retrieves the standings data as a JSON object, parses it using the json library, and creates a pandas DataFrame containing the standings for each conference.

The script then sorts the standings by wins and losses and selects the top 8 teams from each conference. The standings for each conference are then formatted as markdown tables using the to_markdown() method of the pandas DataFrame. The markdown tables are then appended to the end of the `README.md` file.

## How to use it
To use this script, you need to have a Rapid API account and an `API key` that has access to the standings endpoint. You should store your `API key` as a secret in your GitHub repository, which can be accessed by the script during execution.

To schedule the script to run at a regular interval, you can use a `GitHub Actions` workflow that is triggered by a schedule event. The workflow `YAML file` should specify the interval at which the script should run, as well as the timezone in which the script should be executed. An example workflow YAML file is included in this repository, which you can modify to suit your needs.
