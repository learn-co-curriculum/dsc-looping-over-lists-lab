
# Looping over Lists - Lab

## Introduction

In this lab, we will be practicing what we know about `for` loops. We will use them to reduce the amount of code we write by hand to iterate through collections. We will be using parts of the top travel cities data used in the previous list lab, along with their population and their populations and their areas, and use them to practice our for loops. Let's get started!

## Objectives
You will be able to:
* Use a `for` loop to iterate over a list

## Practice with For Loops: Print 

In the last lessons, we worked with some of our travel data.  Additional data has been compiled in the next cell.


```python
cities = ["Buenos Aires", "Toronto", "Pyeongchang", "Marakesh", 
          "Albuquerque", "Los Cabos", "Greenville", "Archipelago Sea"]

populations = [2891000, 2800000, 2581000, 928850, 559277, 287651, 84554, 60000] 

areas = [4758, 2731, 3194, 200, 491, 3750, 68, 8300]
```

Next, create a for loop That prints out the following line for each of the eight `cities`:

> The population of {CITY} is {POPULATION SIZE}


```python

for index in list(range(0, len(cities))):
    print("The population of " + cities[index] + " is",  + populations[index])
```

    The population of Buenos Aires is 2891000
    The population of Toronto is 2800000
    The population of Pyeongchang is 2581000
    The population of Marakesh is 928850
    The population of Albuquerque is 559277
    The population of Los Cabos is 287651
    The population of Greenville is 84554
    The population of Archipelago Sea is 60000


As a next exercise, we'd like to know what the **sum of all the areas** of these 8 cities is. You can use a for loop for this as well. Start off by creating a variable `area_sum = 0`, then, in each iteration of the for loop, you'll add the respective city area to the `area_sum`. **HINT** use `+=`! 




```python

area_sum = 0
for area in areas:
    area_sum += area
print(area_sum)
```

    23492


Next we want to print out the population density for each of the cities. Note that you can find the population density by using the following formula: 

> Population Density = Population / Area

Print out each of the population densities one by one. Before you print them make sure to round the final densities to two decimals. You can do this by using
```python
round(your_density, 2)
```


```python

for index in list(range(0, len(areas))):
    print(round(populations[index] / areas[index],2))
```

    607.61
    1025.27
    808.08
    4644.25
    1139.06
    76.71
    1243.44
    7.23


## Practice with For Loops: Creating New Lists

In the past few exercises, you've learned how to use for loops to print out certain values. Another very relevant application of for loops is when we use them to create new lists instead of simply using them to print!

Let's illustrate this with an example. Imagine we have a list of numbers ranging from 1-5, and we want to use this to create a list with numbers from 2-6. You can use a for loop to create this new list, using two essential pieces of code:
- Start off creating an empty list like this: `new_list = []`
- In the last line inside the for loop, use `new_list.append()`

This would look like this:


```python
numbers_list = [1,2,3,4,5]
```


```python
new_list = []
for numbers in numbers_list: 
    new_list.append(numbers + 1)
```

Let's have a look at our `new_list`:


```python
new_list
```




    [2, 3, 4, 5, 6]



That worked! Let's use what we just learned and repeat our population density exercise. Instead of printing out the densities, let's create a new list `population_densities` that holds the density values.


```python

population_densities = []
for index in list(range(0, len(areas))):
    population_densities.append(round(populations[index] / areas[index],2))
    
print(population_densities)
```

    [607.61, 1025.27, 808.08, 4644.25, 1139.06, 76.71, 1243.44, 7.23]


## Summary

In this section we saw how we can use `for` loops to go through elements of a list and perform the same operation on each.  By using `for` loops we were able to reduce the amount of code that we wrote and write more expressive code.
