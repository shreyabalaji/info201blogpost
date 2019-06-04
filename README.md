
# INFO 201 at the University of WA

by Shreya Balaji

After my first year here at the **University of Washington**, I can safely say
there are a few courses that seem to stand out to me, for a variety of
different reasons. INFO 201 fits in this category for the sole reason that
it has exposed to me a lot of useful topics that I know I will be using
throughout my academic years and career as well. Some of the most important
(in my opinion, of course) are: _GitHub_, _command line_, _R markdown_, _dplyr_,
and _shiny_, which can help us make interactive applications. In this blog post,
I want to focus on dplyr, which is the R package that deals with data wrangling
and data manipulation, and talk about a few important functions of it.

##### DPLYR

1. To start off, one must first download the package for dplyr, and make sure
to load it.

`install.packages("dplyr")`
`library(dplyr)`

2. Now that we have it installed and loaded, let us pretend the data set we
are working with is called "flowers" and that it contains information about the
number of petals, color, and length.

3. The first important function is called the `select()` function, which allows
us to select what column of the data set we find relevant and filter it as such.
`specific <- select(flowers, length, color)`

4. Another important function is called the `filter()` function, which allows
us to select what rows of the data set we find relevant and filter it as such.
_(Note the difference between column and row.)_
 `peonies_data <- filter(flowers, color == blue)`

5. Another important function is called the `mutate()` function, which provides
the ability to create more columns in the data set!
`flowers <- mutate(
  flowers,
  compare_to_petal_avg = 34 - petal_count)`

6. Another important function is called the `arrange()` function, and this lets
you sort the rows of your data frame by some way you indicate...placing no operator
in front of the column will sort it in increasing order, and a minus sign will
sort it decreasingly.
`flowers <- arrange(flowers, -petal_count, length)`
In this, the petal count would be sorted in decreasing order, and length in
increasing order.

7. Another important function is called the `summarize()` function, which reduces
a column to a single value, like a sum or average.
`petal_avg <- summarize(
  flowers,
  mean = mean(petal_count)`

IMPORTANT FEATURE: **The pipe operator!**
(written as %>%) takes the result from a function and passes it as the first argument to the next function, so they can be chained together!

#### So overall....

This was a very basic overview of some of the concepts of dplyr, and some of the
important functions and features of the package. The best way to get a grasp of
these concepts is through practice and doing the homework, but overall, INFO 201
teaches you a lot and I am glad I took it!
