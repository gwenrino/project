EDA visualizations show that the week of the year is highly correlated (though not linearly) with the number of cases. This correlation is finer than the correlation with season and should be a key feature in the best predictive model. However, although the week of the year captures information about the annual cycle of disease occurrence, some years are much worse than others, so I need more information than just week of year.

If I include year.season as a feature in a linear or tree model, I get pretty good results (MAE = ~11), getting in range of my required model performance per my FPS. **I might be able to improve my MAE by engineering a feature year.weekofyear.** On the other hand, this doesn't really seem like a legitimate strategy, since year.weekofyear is essentially the identifier of an observation!

So I think the next step is to get a clearer understanding of which weather-related features would have the most impact on my model. **Some things to try:**
- Try focusing on the features that came up as significant in the linear models.
- Try building a tree model that doesn't include anything about dates. First few nodes could be useful as features.
- Seems like there is redundancy in some of the features (e.g. temperatures in both Kelvin and celsius). Is this redundancy confounding or diluting the variables that have the most impact?
- Learn about the caret package and how I might use it to select features.
- Ask Kannu; I think she understands something about this, maybe using random forest?

Another step is to learn more about **time series forecasting methods** to see if they are relevant to this situation.