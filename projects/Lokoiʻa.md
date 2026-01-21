---
layout: project
type: project
image: img/micromouse/spanish-scholarship.png
title: "Lokoiʻa"
date: 2023
published: true
labels:
  - video games 
  - java
summary: "My ICS 211 final project and videogame"
---


During my sophomore year, my classmates and I developed a text based fishing competition game. Where we implemented object oriented programming to allow users to interact with a simulated fishing pond. The purpose of this final project was to combine Hawaiian cultural practices with programming principles. 

As for the mechanics of the game itself, players through a series of choices, could gain the most amount of fish based off the options in rules provided. Such as their equipment, selecting from items like fishing poles, spears, and nets. Players would alternate turns, amassing or loosing fish. We randomizated indigenous of fish's sizes and variety. With restrictions, such as the fish being adolescence or endangered, resulting in releases.  


Here is some code to intergated the defining standards for what would advance players:

```cpp
public Fish(String name, String bodyColor, String finColor, String food) {
        this(name, bodyColor, finColor, food, (int) (Math.random() * 1000) + 1); 
    }

    //Generates a random interger. 
    private int generateRandomLength() {
        Random lengthR = new Random();
        return lengthR.nextInt(1000) + 1;
    }
    //Gets fish's body weight.
    public int getWeight() {
        return weight;
    }
   
    //Calculates and sets the weight of the fish based on its length. 
    private void setWeight() {
        this.weight = (int) (0.00001 * Math.pow(this.length, 3));   
    }

```



