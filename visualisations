# Load libraries
library(streamgraph)
library(dplyr)
library(babynames)

# Prepare data
data <- babynames %>%
  filter(
    sex == "F",
    name %in% c("Ashley", "Jessica", "Amanda", "Patricia","Helen","Betty")
  )

# Create streamgraph
streamgraph(
  data,
  key = "name",
  value = "n",
  date = "year"
) %>%
  sg_fill_brewer("BuPu")


#An Almost StemGraph using ggplot

library(tidyverse)
library(babynames)

# Prepare data
data <- babynames %>%
  filter(
    sex == "F",
    name %in% c("Ashley", "Jessica", "Amanda", "Emily")
  )

# Plot
ggplot(data, aes(x = year, y = n, fill = name)) +
  geom_area(alpha = 0.9, colour = "white", linewidth = 0.2) +
  scale_fill_brewer(palette = "BuPu") +
  labs(
    title = "Popularity of Selected Female Names",
    x = "Year",
    y = "Number of Births",
    fill = "Name"
  ) +
  theme_minimal(base_size = 14)


#SteamGraph with plotly
library(plotly)
library(dplyr)
library(babynames)

data <- babynames %>%
  filter(
    sex == "F",
    name %in% c("Ashley", "Jessica", "Amanda", "Emily")
  )

plot_ly(
  data,
  x = ~year,
  y = ~n,
  color = ~name,
  type = "scatter",
  mode = "lines",
  stackgroup = "one"
) %>%
  layout(
    title = "Popularity of Selected Female Names",
    xaxis = list(title = "Year"),
    yaxis = list(title = "Number of Births")
  )


#GGANIMATE
library(gapminder)
library(gganimate)
library(ggplot2)
library(gifski)
df<-gapminder
a<-ggplot(gapminder, aes(x=gdpPercap, y=lifeExp,
                      size=pop, colour = continent))+
  geom_point(alpha=0.7)+
  scale_x_log10()+
  scale_size(range=c(2,12), guide="none")+
  transition_time(year)+
  labs(title = 'Year:{round(frame_time)}',
       x="GDP per capita",y = "Life expectancy")
animate(a,
        nframes = 100,  # Total frames
        fps = 10,       # Frames per second
        width = 600,    # Width in pixels
        height = 400)   # Height in pixels
anim_save("FisrtGraph.gif")



# install.packages("dplyr")
library(dplyr)
library(ggplot2)
library(gganimate)
library(gapminder)

df <- gapminder %>%
  filter(year %in% c(1952, 1972, 1992, 2007)) %>%
  group_by(year, continent) %>%
  summarise(mean_life = mean(lifeExp))

b<-ggplot(df, aes(x = continent, y = mean_life, fill = continent)) +
  geom_col() +
  transition_states(year,
                    transition_length = 2,
                    state_length = 1) +
  labs(title = "Year: {closest_state}") +
  theme_minimal() +
  theme(legend.position = "none")
animate(b,
        nframes = 100,  # Total frames
        fps = 10,       # Frames per second
        width = 600,    # Width in pixels
        height = 400)   # Height in pixels
anim_save("SecondGraph.gif")

library(dplyr)
library(ggplot2)
library(gganimate)
library(gapminder)

df <- gapminder %>%
  filter(country %in% c("United States", "China",
                        "India", "Germany", "Brazil"))

c<-ggplot(df, aes(x = year, y = lifeExp,
               color = country, group = country)) +
  geom_line(linewidth = 1) +
  geom_point(size = 2) +
  transition_reveal(year) +
  labs(x = "Year", y = "Life expectancy") +
  theme_minimal()
animate(c,
        nframes = 100,  # Total frames
        fps = 10,       # Frames per second
        width = 600,    # Width in pixels
        height = 400)   # Height in pixels
anim_save("ThirdGraph.gif")
library(ggplot2)
library(gganimate)
library(gapminder)

d<-ggplot(gapminder, aes(x = gdpPercap, y = lifeExp,
                      size = pop, color = continent)) +
  geom_point(alpha = 0.7) +
  scale_x_log10() +
  scale_size(range = c(2, 12), guide = "none") +
  transition_time(year) +
  labs(title = "Year: {round(frame_time)}") +
  shadow_mark(alpha = 0.1, size = 0.5)
animate(d,
        nframes = 100,  # Total frames
        fps = 10,       # Frames per second
        width = 600,    # Width in pixels
        height = 400)   # Height in pixels
anim_save("FourthGraph.gif")
getwd()
