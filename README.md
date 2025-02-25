# Jammon
App to help users find new music and also for artists to find collaborators 

**Still in the planning stages...**

Notes:
**How Spotify Recommendation system works:**

- Spotify’s recommendation system combines some of the best strategies from different types of models to create a powerful and comprehensive solution.
- **Collaborative Filtering**: It works by **analyzing the listening behavior of millions of users** and identifying patterns and similarities
    - Essentially, it uses the collective tastes and preferences of Spotify’s vast user base to make predictions about what individual users might enjoy
        - Identifying similar users, Spotify can recommend songs that those users have enjoyed but the current user hasn't discovered yet.
    - **Music maps** are visual representations of how songs are related based on user listening patterns.
        - Spotify creates these maps by analyzing which tracks are often played together and grouping songs into clusters that reflect common listening patterns. This clustering helps Spotify identify relationships between different tracks and genres, making it easier to recommend songs that match a user’s tastes
            - For example, if a significant number of users enjoy the same songs and also frequently listen to another song, those songs will be clustered together
        - The proximity of tracks on the map is not random; it’s a visual representation of how similar tracks are based on user behavior.
            - If two songs are often listened to back-to-back, they’ll be adjacent stars on the map.
            - This proximity indicates that users who like one song might also like the other. It’s like discovering a new favorite song through the musical constellations formed by the preferences of others.
- Second level, there is **Content Filtering**: adds depth to recommendations by analyzing more than just listening patterns. It delves into the attributes of each track to capture its essence.
    - Spotify’s algorithm extracts metadata, performs raw **audio analysis**, and even considers **cultural context**
        - For example, metrics like danceability and loudness help understand a track’s sonic characteristics
        - while lyrics and adjectives from articles provide cultural insights.
    - Here are some of the key factors Spotify considers:
        - **Release Date:** The official launch date of a song, providing context about its era and historical backdrop.
        - **Label:** The record label associated with a track, offering insights into the artist’s affiliations and musical style.
        - **Artist:** The creator of the track, significantly influencing its genre, sound, and storytelling.
        - **Album:** The collection of songs the track belongs to, contributing to its broader thematic context.
        - **Genre:** The musical category of the track, indicating its general style and sonic characteristics.
        - **Duration:** The length of the track, affecting its structure and how it engages listeners.
        - **Key Signature:** The tonal center of the track, which shapes its mood and emotional impact.
        - **Mode:** Whether the track is in a major or minor key, influencing its overall feel and atmosphere.
        - **Time Signature:** The rhythmic framework of the track, which determines its beat and groove.
        - **Tempo:** The speed of the track’s rhythm, measured in beats per minute (BPM), impacting its energy level.
        - **Language:** The language in which the track’s lyrics are sung, catering to linguistic preferences and cultural context.
        - **Instruments:** The instruments used in the track’s composition, shaping its overall sound and texture.
        - **Featured Artists:** Additional artists who contribute to the track, adding diversity to its musical elements.
        - **Producer:** The individual overseeing the track’s production, playing a crucial role in its sound quality and arrangement.
        - **Lyrics:** The words of the song, conveying its emotions, stories, and themes, and adding depth to its narrative.
    - As a result, Spotify can recommend songs that have similar characteristics to those a user already enjoys, even if those songs are not commonly paired together by other users.
- **Natural Language Processing** (NLP):
    - By leveraging NLP, Spotify can analyze a wide range of textual data, capturing cultural and emotional nuances that improve the accuracy and personalization of recommendations.
    - Lyric Analysis:
        - By examining the words and phrases in lyrics, Spotify can identify themes, feelings, and moods that contribute to the emotional tone of a track
            - For example, a song about heartbreak can be paired with other melancholy tracks, even if their musical styles are different, ensuring that the listener’s emotional journey is maintained.
    - Metadata and User-Generated Content/Text
        - Metadata such as song titles, album names, and artist information are critical to categorizing and understanding tracks
        - In addition, user-generated content such as playlist names and descriptions provide insight into how users perceive and categorize their music
    - External Content Analysis!!
        - Spotify **scans reviews, blog posts, and social media discussions** to gauge public perception and trends around specific artists or genres.
            - This real-time analysis helps Spotify stay on top of music trends and incorporate emerging artists into its recommendations.
    - Search Query Analysis
        - By studying the text of users’ search queries, Spotify gains insight into what users are actively searching for
        - I also found that the “Top Results” by x query changes as x changes
            - meaning the initial auto-complete suggestion was wrong
- **Advanced Audio Analysis**
    - Deep learning and Neural Networks:
        - Spotify employs deep learning techniques, particularly neural networks, to learn complex patterns and representations from vast amount of user and music data.
        - Convolutional Neural Networks (CNNs) and Recurrent Neural Networks (RNNs) are used to process audio data (through spectograms) and capture temporal dependencies in music.
        - These deep learning models enable Spotify to generate more nuanced and contextually relevant recommendations.
    - Spotify’s audio model uses sophisticated machine learning algorithms to perform a detailed **analysis of the raw audio signals in each track**.
        - A key aspect of this audio model is its ability to analyze and interpret the musical structure of a track. This includes identifying patterns in melody and harmony, understanding the dynamics of the song, and recognizing the style and instrumentation used.
    - Here are twelve examples of **metrics Spotify uses to differentiate songs**:
        - **Danceability:** Quantifies a song’s dance-worthy quality, providing insights into its rhythmic patterns and groove. A higher score indicates a track that is likely to make you move and groove.
        - **Loudness:** Measures a song’s auditory intensity or volume, helping to categorize songs based on their dynamic range, from soft and mellow to energetic and intense.
        - **Energy:** Reflects the intensity and vigor of a track, assessing how active and powerful the music feels. This metric is valuable for determining a song’s overall mood.
        - **Valence:** Gauges a song’s emotional tone, ranging from negative to positive. This provides insights into the song’s overall positivity or melancholy.
        - **Tempo:** Represents the speed of a song’s rhythm, measured in beats per minute (BPM). It categorizes songs into different pace categories, from slow ballads to up-tempo dance tracks.
        - **Acousticness:** Quantifies the presence of acoustic instruments in a song, helping to distinguish between tracks with more organic sounds and those heavily reliant on electronic elements.
        - **Instrumentalness:** Measures the extent to which a track contains vocals. A high score suggests a primarily instrumental composition.
        - **Speechiness:** Identifies the presence of spoken words or vocal elements in a song, helping to distinguish between more instrumental tracks and those that feature vocal content.
        - **Key:** Indicates the tonal center of a song, helping to classify tracks based on their musical key signatures.
        - **Mode:** Identifies whether a track is in a major or minor key, contributing to the song’s emotional tone and mood.
        - **Time Signature:** Defines the rhythmic structure of a song, indicating the number of beats in each measure and influencing the song’s overall feel.
        - **Duration:** Represents the length of a song in minutes and seconds, providing basic information about the track’s playtime.
    - Ensemble Methods:
        - Ensemble methods, such as weighted averaging or ranking aggregation, are used to combine the outputs of different models.
        - By leveraging the strengths of various algorithms, Spotify can provide more robust and personalized recommendations.
- Analyze user listening behavior/history
    - Tracks all interactions such as listening history, preferences, and even skips
- How do we keep the vibe going?

**How Does Spotify Create Personalized Playlists?**

- Discover Weekly:
    - **Using a mix of collaborative filtering and deep learning techniques. Every Monday**, this playlist delivers **30 songs tailored to each user’s unique music taste** based on their listening history and patterns.
- Daily Mix (Would probably come later):
    - Daily Mix focuses on **mixing familiar tracks with a few new additions** to keep the listening experience fresh without straying too far from what the user already enjoys.
    - This feature ensures that users always have a selection of music that matches their mood and preferences throughout the day
        - The continuous updating of these mixes encourages users to engage with the platform regularly, maintaining high levels of satisfaction and loyalty.
- Other Song Recommendations:
    - Suggest additional song recommendations at the end of each playlist by analyzing the existing tracks in a user playlist and **suggesting similar songs that might go well together**.

**Getting and prepping database for Rec System**

- We can try to import user data similar to [receiptify.com](http://receiptify.com) using Spotify SDK API
- That will act as the baseline:
    - every action after that will help shape the recommendation engine
    - tracking browsing/listening history and later analyzing the data for correlations between different songs and music genres, and compare the user’s preferences to the entire user database.
 
**Database Design**

- Plan to use PostgreSQL as the database and store:
1. **Users**
    - **users** table
    - Attributes: `id`, `username`, `email`, `password_hash`, `created_at`, `avatar_url` (optional), etc.
2. **Songs**
    - **songs** table
    - Attributes: `id`, `title`, `artist_id`, `album_id`, `audio_url`, `duration`, `genre`, `release_date`, etc.
    - You can also store high-level audio features (e.g., tempo, energy) if you have them. Alternatively, keep them in a separate table if you plan to handle more detailed analytics.
3. **Artists**
    - **artists** table
    - Attributes: `id`, `name`, `description`, `genre`, etc.
4. **Albums**
    - **albums** table
    - Attributes: `id`, `title`, `artist_id`, `release_date`, `cover_art_url`, etc.
5. **Playlists**
    - **playlists** table
    - Attributes: `id`, `name`, `description`, `user_id` (the creator), `created_at`, `cover_art_url` (optional), etc.
    - Relationship: One user can create many playlists; a playlist belongs to one user.
6. **Playlist-Songs** (junction table for the many-to-many relationship)
    - **playlist_songs** table
    - Attributes: `playlist_id`, `song_id`, `added_at`, `position` (optional – for ordering), etc.
    - You could combine `position` with a separate sort field or store ordering in an array if using NoSQL.
7. **User Likes / Favorites**
    - **user_likes** table
    - Attributes: `user_id`, `song_id`, `created_at`, etc.
    - This table captures songs a user “likes” or “favorites.”
8. **User Listens / History**
    - **user_listens** table
    - Attributes: `user_id`, `song_id`, `played_at`, `device`, `listen_duration` (how many seconds listened), etc.
    - Very useful for building a collaborative filtering dataset and generating recommendations.

> Note on Uploading Music: You’ll need to store references to the uploaded files (possibly on a cloud storage like Amazon S3) in the songs table (audio_url). For legal music distribution, you’d typically also track who uploaded it, whether it’s an original track, licensing info, etc.
>
