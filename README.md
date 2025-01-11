# globalfindexdatabase_R
R is case sensitive
The tidyverse package in R is a collection of packages designed for data science tasks such as data manipulation, exploration, and visualization. 
> install.packages("palmerpenguins")
> library(palmerpenguins)
> summary(penguins)
>View(penguins)
> install.packages("tidyverse")
>library(tidyverse)
if you need documentation of any function of r then write this. Here for print function
> ?print()
> vector_1 <- c(12,13,14)
> pipes in r works same as in linux command pipe, outcome of one function is send as input of another   %>%
> Vectors


Data frames

Matrices

Arrays
>
>  two types of vectors: atomic vectors and lists.
>vector is a group of data elements of the same type, stored in a sequence in R
>There are six primary types of atomic vectors: logical, integer, double, character (which contains strings), complex, and raw. The last two–complex and raw–aren’t as common in data analysis
This diagram illustrates the hierarchy of relationships among these four main types of vectors:

![Screenshot 2024-10-26 at 22 13 38](https://github.com/user-attachments/assets/9b645386-fecb-44fe-9b9e-7f83a375a0c1)

One way to create a vector is by using the c() function (called the “combine” function)
>For example, you can use the c() function to store numeric data in a vector. 

c(2.5, 48.5, 101.5)

To create a vector of integers using the c() function, you must place the letter "L" directly after each number.

c(1L, 5L, 15L)

You can also create a vector containing characters or logicals. 

c(“Sara” , “Lisa” , “Anna”)

c(TRUE, FALSE, TRUE)

>typeof(c(“a” , “b”))

#> [1] "character"

x <- c(33.5, 57.75, 120.05)

length(x)

#> [1] 3

You can also check if a vector is a specific type by using an is function: is.logical(), is.double(), is.integer(), is.character().
x <- c(2L, 5L, 11L)

is.integer(x)

#> [1] TRUE


Naming vectors 
All types of vectors can be named. Names are useful for writing readable code and describing objects in R. You can name the elements of a vector with the names() function. As an example, let’s assign the variable x to a new vector with three elements. 

x <- c(1, 3, 5)

You can use the names() function to assign a different name to each element of the vector. 

names(x) <- c("a", "b", "c")


Now, when you run the code, R shows that the first element of the vector is named a, the second b, and the third c.

x 

#> a b c 

#> 1 3 5

Remember that an atomic vector can only contain elements of the same type. If you want to store elements of different types in the same data structure, you can use a list. 

Creating lists
Lists are different from atomic vectors because their elements can be of any type—like dates, data frames, vectors, matrices, and more. Lists can even contain other lists. 

You can create a list with the list() function

list("a", 1L, 1.5, TRUE)

Like we already mentioned, lists can contain other lists. If you want, you can even store a list inside a list inside a list—and so on. 

list(list(list(1 , 3, 5)))

Determining the structure of lists 
If you want to find out what types of elements a list contains, you can use the str() function. To do so, place the code for the list inside the parentheses of the function. When you run the function, R will display the data structure of the list by describing its elements and their types.

Let’s apply the str() function to our first example of a list. 

str(list("a", 1L, 1.5, TRUE))

We run the function, then R tells us that the list contains four elements, and that the elements consist of four different types: character (chr), integer (int), number (num), and logical (logi). 

#> List of 4

#>  $ : chr "a"

#>  $ : int 1

#>  $ : num 1.5

#>  $ : logi TRUE

Let’s use the str() function to discover the structure of our second example.  First, let’s assign the list to the variable z to make it easier to input in the str() function. 

z <- list(list(list(1 , 3, 5)))

Let’s run the function. 

str(z)

#> List of 1

#>  $ :List of 1

#>   ..$ :List of 3

#>   .. ..$ : num 1

#>   .. ..$ : num 3

#>   .. ..$ : num 5

The indentation of the $ symbols reflect the nested structure of this list. Here, there are three levels (so there is a list within a list within a list).  

Naming lists
Lists, like vectors, can be named. You can name the elements of a list when you first create it with the list() function:

list('Chicago' = 1, 'New York' = 2, 'Los Angeles' = 3)

$`Chicago`

[1] 1

$`New York`

[1] 2

$`Los Angeles`

[1] 3

https://www.coursera.org/learn/data-analysis-r/supplement/7dRY6/vectors-and-lists-in-r







