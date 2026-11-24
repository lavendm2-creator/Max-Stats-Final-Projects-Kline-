# Max-Stats-Final-Projects-Kline-

library(readr)

setwd("/courses/STA145/lavendm2")
data <- read_csv("data.csv")
View(data)

#step 5: run the three checks
dim(data)
names(data)
summary(data)

# sd
sd(data$star_rating)
sd(data$lunch)

# linear regression
linear_model <- lm(star_rating ~ lunch, data = data)
summary(linear_model)

# scatter plot
linear_plot <- plot(data$lunch, data$lunch)
print(linear_plot)

# add x line and y line for means
meany <- mean(data$lunch)
meanx <- mean(data$lunch)

abline(v = meany, col = "black")
abline(h = meanx, col = "black")
