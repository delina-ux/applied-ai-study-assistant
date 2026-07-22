# Model Card

## Model Name
MoodMatch Recommender

## Goal / Task
This recommender suggests songs that best match a user's music preferences. It compares genre, mood, and energy level to rank songs from most to least relevant.

## Data Used
The system uses a CSV file containing song information. Each song includes its title, artist, genre, mood, energy, tempo, valence, danceability, and acousticness. The dataset is small, so recommendations are limited.

## Algorithm Summary
The algorithm gives points for matching the user's favorite genre and mood. It also compares the song's energy to the user's preferred energy. Songs with higher total scores are ranked first.

## Observed Behavior / Biases
The recommender tends to favor songs that match the user's preferred genre because genre receives the highest weight. With a small dataset, the same songs often appear near the top of the recommendations. Users with uncommon preferences may receive fewer relevant results.

## Evaluation Process
I tested the recommender using multiple user profiles, including Pop/Happy, Chill Lofi, and Rock/Intense. I compared the rankings after changing user preferences and verified that the recommendations changed logically.

## Intended Use
This project is designed as a simple educational music recommendation system. It demonstrates how scoring and ranking algorithms work.

## Non-Intended Use
This system should not be used as a production recommendation engine. The dataset is too small and the algorithm is too simple for real-world personalization.

## Ideas for Improvement
- Increase the size of the song dataset.
- Add artist similarity and tempo weighting.
- Learn user preferences over time instead of using fixed values.

## Evaluation

### Tested Profiles

**High-Energy Pop**
- Produced mostly upbeat pop songs.
- Results matched expectations.

**Chill Lofi**
- Returned calmer songs with lower energy.
- Rankings changed as expected.

**Rock / Intense**
- Rock songs moved toward the top.
- Genre weighting had a strong effect.

### Experiment

I increased the importance of energy when comparing songs. This caused songs with similar energy levels to move higher in the rankings. The recommendations became more varied while still matching the user's preferences.

### Limitations

The dataset is small and contains only a few genres. Genre receives more weight than the other features, which can cause similar songs to appear repeatedly. A larger dataset and better feature weighting would improve recommendation quality.
