# -------------------------------
# 1. Create Dataset
# -------------------------------

movies <- data.frame(
  Title = c("Inception", "Titanic", "Avengers", "Joker", "Frozen", "Interstellar", "Batman", "Coco"),
  Genre = c("Sci-Fi", "Romance", "Action", "Drama", "Animation", "Sci-Fi", "Action", "Animation"),
  Rating = c(8.8, 7.8, 8.0, 8.5, 7.5, 8.6, 7.9, 8.4)
)

# Display dataset
print("Movie Dataset:")
print(movies)


# -------------------------------
# 2. Highest Rated Movie
# -------------------------------

top_movie <- movies[which.max(movies$Rating), ]
print("Highest Rated Movie:")
print(top_movie)


# -------------------------------
# 3. Average Rating
# -------------------------------

avg_rating <- mean(movies$Rating)
print("Average Rating:")
print(avg_rating)


# -------------------------------
# 4. Genre Distribution
# -------------------------------

genre_count <- table(movies$Genre)
print("Genre Distribution:")
print(genre_count)


# -------------------------------
# 5. Sort Movies by Rating
# -------------------------------

sorted_movies <- movies[order(-movies$Rating), ]
print("Movies Sorted by Rating:")
print(sorted_movies)


# -------------------------------
# 6. Bar Plot (Ratings)
# -------------------------------

barplot(movies$Rating,
        names.arg = movies$Title,
        main = "Movie Ratings Comparison",
        xlab = "Movies",
        ylab = "Ratings",
        col = "pink",
        border = "black")


# -------------------------------
# 7. Pie Chart (Genre Distribution)
# -------------------------------

pie(genre_count,
    main = "Genre Distribution",
    col = rainbow(length(genre_count)))
