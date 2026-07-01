# Movie Analytics — Power BI Project

An interactive Power BI report analyzing a movie dataset, covering box office performance, ratings, genres, and trends over time.

## File

```
powerBI-project.pbix
```

## Data Model

The report uses a single table, **`Movies`**, with fields including:

| Field | Description |
|---|---|
| `Title` | Movie title |
| `Director` | Movie director |
| `Genre` | Movie genre |
| `Year` | Release year |
| `Runtime` | Movie runtime |
| `Rating` | Audience/critic rating |
| `Revenue` | Box office revenue |
| `Votes` | Number of audience votes |
| `Metascore` | Critic score |

**Key measures** used throughout the report: `Total Movies`, `Total Revenue`, `Total Votes`, `Avg Rating`, `Avg Runtime`, `Avg Revenue`, `Avg Metascore`.

## Report Pages

**1. Movie Overview & Time Trends**
- Total revenue by year (line chart)
- Average rating by year (line chart)
- Average runtime by year (area chart)
- Total movies by year (clustered column chart)
- Total votes by year (clustered bar chart)

**2. Genre & Rating Analysis**
- Total movies by genre (donut chart)
- Average rating by genre (bar chart)
- Total revenue by genre (treemap)
- Average metascore by genre (clustered bar chart)
- Total votes by genre (funnel chart)

**3. Top Performers & Box Office**
- Total revenue by director (bar chart)
- Rating vs. revenue (scatter chart)
- Total votes by title (bar chart)
- Detailed movie table (title, revenue, rating, director, year, votes)
- Revenue by title (funnel chart)
- Navigation/action button

**4. Correlation & Advanced Metrics**
- Runtime vs. average revenue & rating (combo chart)
- Rating vs. revenue by year (scatter chart)
- Revenue by year and genre (bar chart)
- Votes vs. revenue (scatter chart)
- Genre slicer
- Year slicer

## How to Use

1. Open `powerBI-project.pbix` in **Power BI Desktop**.
2. If prompted, refresh the data source to pull the latest data.
3. Use the **Genre** and **Year** slicers on the Correlation & Advanced Metrics page to filter the whole report.
4. Navigate between the four report pages using the page tabs at the bottom.

## Requirements

- Power BI Desktop (recent version recommended)
- Access to the underlying data source, if data refresh is required (not embedded as a live connection — data is imported into the model)

## Notes

- All visuals are built on a single `Movies` table (no relationships/joins required).
- Measures are pre-calculated in the data model (DAX) rather than computed live in each visual.
