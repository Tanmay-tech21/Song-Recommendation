Song Recommendation System README

Overview

This project is a Song Recommendation System that utilizes content-based filtering to provide personalized song recommendations based on user preferences. The system takes user-selected songs from their Spotify playlists and uses both text and attribute features of songs to generate recommendations.

Technologies Used

Python
Pandas
NumPy
Scikit-learn
Spotipy (Spotify API wrapper)
Matplotlib
Seaborn


Setup and Authentication

Ensure you have the required Python libraries installed. You can install them using:
pip install pandas numpy scikit-learn spotipy matplotlib seaborn

Create a Spotify Developer account and register your application to obtain the client_id and client_secret. Save these credentials in a file named secret.txt.
Update the redirect_uri in the code to match the redirect URI specified in your Spotify Developer application settings.
Run the script to authenticate and obtain access to your Spotify account.

Usage

Upon running the script, you will be prompted to select a playlist from your Spotify account. The script will retrieve the tracks from the selected playlist.
The system will use both text data (song and artist names) and attribute features (acousticness, energy, loudness, danceability, valence, liveness, tempo, duration) to create a dataset.
The content-based filtering algorithm calculates the cosine similarity between the selected playlist and a dataset of popular songs.
The top recommended songs are displayed based on the weighted combination of text and attribute similarities.
Scatter plots and visualizations are provided to showcase attribute similarities and the recommendations.
File Descriptions

song_recommendation_system.py: Main script containing the recommendation system implementation.
secret.txt: File to store Spotify API credentials.
spotify_dataset.csv: Dataset of popular songs with attributes.
Recommendation.csv: An alternative dataset (commented out in the code) for recommendations.
