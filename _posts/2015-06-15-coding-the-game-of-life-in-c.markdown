---
layout: post
title: "Coding the Game of Life in C"
date: 2015-06-15 19:00:00
categories: c game college
---

So, the last test of my Introduction to Programming class in college is to create a program with C using most of the concepts we learned this semester. And I decided to write the Game of Life.

###The Game of Life###
In the 1940s, John von Neumann created, under very complicated rules, a machine that could create copies of itself. Then someday in 1970, a brittish mathematician called Jonh Horton Conway developed the Life, a successful attempt to simplify von Neumann's ideas. Life became very famous and even introduced a new field of mathematical reasearch, the cellular automata. Duo to it's analogies with the behavior of a society of living organisms, it is a "simulation game" - a game that resembles real life processes.

###The Program###
My `main` function calls only one fuction: `game`.

{% highlight c %}
int randomCellCreation(unsigned density){
  return rand() < (RAND_MAX / density) ? 1 : 0;
}

int game(unsigned width, unsigned height){
  unsigned universe[height][width];
  for_position universe[line][column] = randomCellCreation(4);
  while (1) {
    populate(universe, width, height);
    evolution(universe, width, height);
    usleep(200000);
  }
}
{% endhighlight %}

What's happening here is: `game` receives `width` and  `height`, which will be the array indices. The array `universe` is my grid, where the interactions will happen.

In this game, I'll need a lot of `for` conditionals, so I created constants to improve the readability of the code.

{% highlight shell %}
#define for_column for (int column = 0; column < width; column++)
#define for_line for (int line = 0; line < height; line++)
#define for_position for_line for_column
{% endhighlight %}

So in the second line of `game`, I introduce a new function. This function will randomically set a status for the cell in the position `universe[line][column]`. You can see that this fuction asks an argument, `density` is the value responsible for the quantity of living cells at the beggining of the game.

Ok, we now have the status of every cell. Moving on to the `while` loop, I am now calling three other functions. `populate` is the responsable for drawing the grid with the dead and the living cells, `evolution` is the responsable for defining which cells dies and which cells lives to the next generation, and `usleep` - that comes from the `unistd.h` - sets the time in microseconds between the generations.
