IMDb Top 1000 Movies: Exploratory Data Analysis

Interactive Dashboards

PowerBI Dashboard

Tableau Dashboard


Overview

Cinema has long enchanted audiences with its ability to tell compelling stories, portray powerful emotions, and reflect the human experience. From black-and-white classics to modern blockbusters, movies continue to leave a deep cultural and emotional imprint. This project explores IMDb’s top 1000 highest-rated films, aiming to identify trends, uncover insights, and better understand what defines a critically acclaimed movie.

Purpose

The goal of this analysis is to examine IMDb’s list of top 1000 films to identify patterns across multiple aspects—ratings, genres, directors, actors, and financial performance. Through this deep dive, I aim to better understand what factors influence a movie’s success and longevity in public memory.

Technologies & Tools

R

PowerBI

Tableau


Data Source

IMDb Top 1000 Movies: Exploratory Data Analysis

Interactive Dashboards

PowerBI Dashboard

Tableau Dashboard


Overview

Cinema has long enchanted audiencethe years 1920 through 2020. Each entry provides a wide range of attributes including title, release year, age certificate, runtime, genres, IMDb rating, plot summary, Metascore, director, main cast, and gross earnings.

Data Cleaning & Preparation

Before analysis, data cleaning was crucial to ensure consistency and usability. Key steps included:

1. Duplicate Removal

Checked for duplicates; none were found.



2. Removing Irrelevant Columns

The "Poster Link" column was removed as it was not useful for the analysis.



3. Converting Release Year

Transformed from text to integer format.



4. Standardizing Runtime

Removed the “min” text and converted values to integers.



5. Cleaning Gross Revenue

Removed commas and converted the values to integer format.



6. Standardizing Age Certification

Mapped Indian CBFC ratings to the U.S. MPA system for consistency:

CBFC’s “16” was mapped to PG-13 (only one film affected).

Older ratings like “Approved” and “Passed” were grouped as “Unrated.”

The outdated “GP” was updated to “PG.”

“G” was matched with “PG” for standardization.

TV-based ratings like “TV-PG,” “TV-14,” and “TV-MA” were retained.





With the data cleaned and standardized, meaningful exploration could now begin.


Exploratory Data Analysis

Trends Over Time
To start, I analyzed how top-rated films have evolved over time, particularly with regard to ratings, runtime, and representation.

How have average IMDb ratings changed over the decades?

<img src="images/avg_rating_over_decades.png" width="700">The average ratings peaked in the 1930s and have gradually declined over the decades. This may reflect shifting audience preferences or an increase in the number of films, which could dilute the average.

Which decades contribute the most to the top 1000 list?

<img src="images/representation_decade.png" width="700">Recent decades, especially the 2000s and 2010s, are more heavily represented than earlier periods. This may partly explain the decline in average ratings, as more films from recent years increase competition and variability.

How has runtime evolved over the years?

<img src="images/distribution_runtimes.png" width="700">Since the 1960s, runtimes have remained close to 120 minutes, though there’s a slight upward trend in recent years, possibly reflecting a trend toward longer storytelling formats.

Genre Analysis

Genres reveal a lot about audience taste and critical reception.

Which genres are most common?

<img src="images/distribution_genres.png" width="700">Drama dominates the list, followed by comedy, adventure, crime, and action. These genres appear to resonate most with both critics and audiences.

What are the average ratings by genre?

<img src="images/top_genres.png" width="700">Genres such as war, western, and film-noir have the highest average ratings. In contrast, horror, comedy, and thriller films tend to have slightly lower average IMDb scores.

Is there a link between genre and age certification?

<img src="images/correlation_genre_age_rating.png" width="700">Dramas, thrillers, and crime films are more often rated R. Meanwhile, genres like adventure, comedy, and animation lean toward PG and PG-13, catering to broader audiences.

Director Analysis

Next, I looked into which directors had the strongest presence on the list and how their average ratings stacked up.

Which directors are most frequently featured?

<img src="images/top_directors.png" width="700">Alfred Hitchcock tops the list with 14 entries, followed closely by Steven Spielberg (13), Hayao Miyazaki (11), and both Akira Kurosawa and Martin Scorsese with 10 each.

Is there a correlation between number of films and average rating per director?

<img src="images/correlation_director.png" width="700">There’s no strong correlation here. Having more films in the top 1000 doesn’t necessarily mean a higher average rating, suggesting quality and quantity are not always aligned.

Actor Analysis

Now to the stars of the screen: which actors appear most frequently and how do their movies fare?

Which actors appear the most?

<img src="images/top_actors.png" width="700">Robert De Niro leads with 17 top-rated appearances. Others include Tom Hanks, Al Pacino, Brad Pitt, and Leonardo DiCaprio, all with double-digit appearances.

Does acting in more top-rated films translate to higher average ratings?

<img src="images/correlation_actor.png" width="700">Actors like De Niro manage both volume and quality, while others like Denzel Washington appear often but with slightly lower average ratings. Overall, there’s no clear pattern between quantity and rating.

Revenue vs Rating Analysis

Finally, I explored the financial side of top-rated films.

What are typical earnings for these movies?

<img src="images/distribution_revenue.png" width="700">Most films earn under $50 million, with a few blockbusters exceeding $250 million. The distribution is heavily skewed toward lower revenue brackets.

Do higher IMDb ratings lead to more revenue?

<img src="images/correlation_rating_revenue.png" width="700">The data shows only a weak correlation. A high rating doesn’t guarantee box office success—commercial appeal depends on many other factors.

Other Insights

Which age ratings are most common?

<img src="images/movies_age_rating.png" width="700">  
<img src="images/movies_age_rating_2.png" width="700">R-rated movies are the most prevalent overall, followed by PG and PG-13. Even after filtering to post-1984 (when PG-13 was introduced), R remains the most common.

What themes are common in the top movies?

<img src="images/wordcloud.png" width="350">The word cloud of plot overviews suggests common themes such as youth, life journeys, family, love, and transformation. Words like “young,” “story,” “world,” and “find” reflect both coming-of-age narratives and personal growth arcs.

Summary Dashboards

All key visualizations and insights are presented in interactive dashboards:

PowerBI Dashboard

Tableau Dashboard


Conclusion

This analysis offered a deeper look into the characteristics of top-rated movies over the past century. Temporal trends highlighted shifts in ratings and representation. Genre and age ratings showed distinct patterns, while director and actor data revealed who shaped cinema’s most celebrated works. Revenue analysis demonstrated that critical acclaim doesn’t always equal box office dominance.

Ultimately, this project reveals that while IMDb ratings can signal quality, a movie’s legacy is shaped by storytelling, direction, emotion, and the human connections they spark. Numbers alone can’t capture the full magic of great cinema.

