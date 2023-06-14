# Chapter 1 Matplotlib

**Basic plots with Matplotlib**:
- import matplotlib.pyplot as plt
- year = [1950, 1970, 1990, 2010] = x
- pop = [2.519, 3.692, 5.263, 6.972] = y
- plt.plot(year, pop)
- plt.show()
- plt.scatter(year, pop) - **scater plot**
- A correlation will become clear when you display the GDP per capita on a logarithmic scale. Add the line **plt.xscale('log')**

**Histogram**:
- Explore dataset
- Get idea about distribution
- values = [0,0.6,1.4,1.6,2.2,2.5,2.6,3.2,3.5,3.9,4.2,6]
    - plt.hist(values, bins=3)
    - plt.show()
- In the previous exercise, you didn't specify the number of bins. By default, Python sets the number of bins to 10 in that case. The number of bins is pretty important. Too few bins will oversimplify reality and won't show you the details. Too many bins will overcomplicate reality and won't show the bigger picture.
- plt.show() displays a plot; **plt.clf()** cleans it up again so you can start afresh.

**Customiyation**:
- Many options
    - Different plot types
    - Many customizations
- Choice depends on 
    - DataStory you want to tell
- Ex.:
    - import matplotlib.pyplot as plt
    - year = [1950, 1951, 1952, ..., 2100] 
    - pop = [2.538, 2.57, 2.62, ..., 10.85]
    - #Add more data 
    - year = [1800, 1850, 1900] + year
    - pop = [1.0, 1.262, 1.650] + pop
    - plt.plot(year, pop)
    - plt.xlabel('Year')
    - plt.ylabel('Population')
    - plt.title('World Population Projections')
    - plt.yticks([0, 2, 4, 6, 8, 10], ['0', '2B', '4B', '6B', '8B', '10B'])
    - plt.show()
- **Update: set s argument to np_pop**
    - plt.scatter(gdp_cap, life_exp, s = np_pop)
    - You can see that this list is added to the scatter method, as the argument s, for size.
    - Add c = col to the arguments of the plt.scatter() function.
    - Change the opacity of the bubbles by setting the alpha argument to 0.8 inside plt.scatter(). Alpha can be set from zero to one, where zero is totally transparent, and one is not at all transparent.
    - If you have another look at the script, under # Additional Customizations, you'll see that there are two **plt.text()** functions now. They add the words "India" and "China" in the plot.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Dictionaries 

**Dictionaries**:
- world = {"afghanistan":30.55, "albania":2.77, "algeria":39.21} - key-value pairs
- world["albania"] => 2.77
- my_dict = {
   "key1":"value1",
   "key2":"value2",
 }
- **Check out which keys** are in europe by calling the **keys() method** on europe. Print out the result.
- keys have to be unique
- Keys have to be "immutable" objects
- **update a value** world["sealand"] = 0.000028
- **delate a value** by refering to key del(world["sealand"])
- Indexed by unique keys
- Lookup table withunique keys
- print('italy' in europe) **access an el in dictionary**
- Remember lists? They could contain anything, even other lists. Well, for dictionaries the same holds. *Dictionaries can contain key:value pairs where the values are again dictionaries.*
- It's perfectly possible to chain square brackets to select elements. To fetch the population for Spain from europe, for example, you need: **europe['spain']['population']**
