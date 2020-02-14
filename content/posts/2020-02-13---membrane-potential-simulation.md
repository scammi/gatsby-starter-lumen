---
title: Membrane potential simulatiton
date: "2020-02-12T23:46:37.121Z"
template: "post"
draft: false
slug: "/posts/potential-simulatiton/"
category: "physiology"
tags:
  - Physiology
  - Simulation
description: "Simulation of membrane potential and the action potential of excitable cells."
socialImage: "/KnowledgeInformationWisdom.jpg"
---
Simulation of membrane potential and the action potential of excitable cells.

![](https://miro.medium.com/max/480/1*ZXBfXrINyC-UrCh7PqFz8w.gif)

It is written on processing, an open-source graphical library and uses the Java language, with additional simplifications. It is meant to be a flexible software sketchbook. I choose processing since trying ideas and sharing them easy and straight forward.
The program works by simulating an excitable “cell” as a class, there are three main methods “membrane potential”, “depolarized” and “conduct”. Membrane potential method uses a simplified version of the Goldman-Hodgkin-Katz (GHK) voltage equation.
Medical physiology Walter Boron

![](https://miro.medium.com/max/408/1*KvF83mRq8aLjcDNjF597jA.png)

The alpha variable in the equation is the quotient of the permeability between Na and K (PNa/Pk). The number is very low during resting potential since the permeability of K predominates. During an action potential these changes, the permeability of Na increases rapidly in a sigmoid fashion. The depolarize method generates this same change in the alpha variable producing a sudden increase in membrane voltage.
The first action potential is trigger through an automatic cell through a timer, it then propagates thanks to the conducted method.

###Array of cells
![](https://miro.medium.com/max/480/1*bKgCyWNTup538aygSytsLg.gif)

Every square is a cell object and holds in its state the result of the GHK equation that’s calculated 30 times per second. The first cell on the left sequentially triggers the rest and one by one are depolarized.
When white the cell is in resting potential, when red it has been depolarized.
Run

1- Install > processing https://processing.org/download/

2- Clone repository > https://github.com/scammi/membrane-potential-sim

3- Run main.pde insde the main folder
