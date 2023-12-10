---
layout: post
title: "Exploring Trends in Pneumonia and Influenza"
author: Dallin Robison
description: "How can we use past data to better prevent death from influenza and pneumonia?"
---

# Introduction

Winter is on the horizon, and with it comes a new flu season. I have encountered quite a few ads encouraging me to get my flu vaccine, and I am spending more time worrying about my health and the health of those around me. Using historical data, I would like to explore the effect of the flu and try to find trends to inform my own expectations of the flu. One of the most important pieces of information about the flu is how many people die from it. These are tragedies, and I want to believe that we are improving in our ability to prevent death due to disease. I want to find data to see if hope is well placed in our ability to conquer these diseases.

# Data Collection

For the United States, the organization with the most reach and therefore the most data on health is the CDC. I used API requests to obtain a dataset of pneumonia and influenza deaths from the years 2009-2019. Much of my data cleaning involved checking all of the data to see if there were any typos or exceptions. I changed the single date entry into two columns: one for year, and the other for week. I dropped the columns that did not provide additional information, like the season column and the percentage column. I also renamed the columns to be shorter and hopefully more clear. Last, I changed the data types of the columns.

# The Human Element

This data is about human death. This is not something to be taken lightly, and I am trying to make sure that my graphs do not hide the tragedy of the loss of life from the flu. I made sure that the CDC allowed me to create code to request data from them, and in presenting this data, I want to always show the cost and the weight of this data. 

# Conclusion

Using this data, I hope to be able to show that we are improving in our ability to fight these common diseases. I will look at trends in this data set to find out how the US is dealing with the flu and pneumonia.

[This]({{ lotuseat3r.github.io }}/assets/deaths.csv) is the data set. You can find more details in my github <a href="https://github.com/LotusEat3r/Project">repository</a>.