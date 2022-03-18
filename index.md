![Hello World](https://c.tenor.com/Vlde4572j6QAAAAi/animated-text-greet.gif)

<br/>
  
# Welcome to my STATS 220 Website!
 
 On this space, I will be introducing myself, uploading a meme that I have created and explaining how and why this meme was produced the way it was! 😊
  
## About me 
 
* I'm currently in my 4th year, studying BCom & BSc at [The University of Auckland](https://www.auckland.ac.nz/en/study/study-options/find-a-study-option/bachelor-commerce-science.html) 🧑‍🎓
* I love playing tennis in my free time! 🎾
* My favourite food is anything sweet, however donuts top everything else 🍩
  <br/>
  
## My first R project 

Below is a pikachu meme that I have created using a package on R called [magick](https://cran.r-project.org/web/packages/magick/vignettes/intro.html), if you want to learn how to make memes of your own, follow my R code below and test it out yourself! ⭐

# <img src= "https://github.com/Hardishahx/stats220/blob/main/final_meme.png?raw=true" width="700" height="700">

**Check out my code down below** ⏬

``` r

library(magick)

#Insert images 

happy_pikachu <- image_read("https://i.imgflip.com/4k2dfm.png") %>%
  image_scale(600)

surprised_pikachu <- image_read("https://media.wired.com/photos/5f87340d114b38fa1f8339f9/master/w_1600%2Cc_limit/Ideas_Surprised_Pikachu_HD.jpg") %>%
  image_scale(600)

# Insert text images

first_text <- image_blank(width = 600, 
                          height = 575, 
                          color = "#000000") %>%
  image_annotate(text = "Submitting an assignment",
                 color = "#FFFFFF",
                 size = 45,
                 font = "Impact",
                 gravity = "center")

second_text <- image_blank(width = 600, 
                         height = 575, 
                         color = "#000000") %>%
  image_annotate(text = "Recieving the grade back",
                 color = "#FFFFFF",
                 size = 45,
                 font = "Impact",
                 gravity = "center")
                 
# Create Rows

first_row <- c(happy_pikachu, first_text) %>%
  image_append()

second_row <- c(surprised_pikachu, second_text) %>%
  image_append()
  
#Put rows together 

meme <- c(first_row, second_row) %>%
  image_append(stack = TRUE)
  
# Produce image
image_write(meme, "final_meme.png")

```

## Inspiration behind my meme ☁️

1. My main inspiration behind this meme was self experience, there have been many times I thought I handed in a great assignment but the grades did not reflect that 
2. I love pikachu 
3. I've been seeing alot of university related memes lately, but this [meme](https://img.universitystudent.org/1/4/3203/me-acting-surprised-when-i-get-a-bad-grade-for-an-assignment-i-did-overnight-meme.jpg) was one that I found funny, therefore I did my own version of it! 



