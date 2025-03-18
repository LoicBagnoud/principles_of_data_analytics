# Principles of Data Analytics

## by Loic Bagnoud

The following is a breakdown and analysis of the famous Iris Dataset. 
We will be going through several steps in how we would approach an analysis of the entire dataset and its structure and relationship.

## References:

1. https://gist.github.com/curran/a08a1080b88344b0c8a7 - Organization of the Iris Dataset and it's feature descriptions by Github user (curran)

2. https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.head.html - Pandas documentation on getting the first and last 5 values of a data set

3. https://interactivechaos.com/en/python/function/numpynumber - Numpy function to exclude numeric columns. 

4. https://www.w3schools.com/python/pandas/ref_df_select_dtypes.asp - Pandas select_dtypes() that includes or excludes specific columns. 

5. https://www.geeksforgeeks.org/numpy-mean-in-python/ - For getting the mean
   
6. https://www.geeksforgeeks.org/numpy-median-in-python/?ref=ml_lbp - For getting the median
   
7. https://numpy.org/doc/2.2/reference/generated/numpy.min.html - For getting the minima
   
8. https://numpy.org/doc/2.2/reference/generated/numpy.max.html - For getting the maxima
   
9. https://numpy.org/doc/stable/reference/generated/numpy.std.html - For getting the Standard Deviation

10. https://medium.com/@maxmarkovvision/optimal-number-of-bins-for-histograms-3d7c48086fde - On the various types of Bin number calculations in boxplots.

11. ChatGPT for the most appropriate number of bins in boxplots
    Answer: _There's no one "correct" number of bins—it really depends on your data and what you want to emphasize in your histogram._
_Sometimes, it's just about testing a few options. You might experiment with 10, 20, or 30 bins and see which one best reveals the characteristics of your data without making it look too binned or too smooth._

12. https://subhralina.medium.com/iris-dataset-but-make-it-interesting-f8857190c8d6 - For ideas on how to approach showcasing relationships with the Iris Dataset.

13. https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.scatter.html - For how to display colours.
    https://matplotlib.org/stable/gallery/shapes_and_collections/scatter.html

14. Chatgpt on how to display multiple colours of multiple species.
    Answer: You can change the colors by passing a color argument to the plt.scatter() function. In your loop, you can set up a dictionary that maps each species to a specific color. For example:
        Define a color mapping for each species
        colors = {"setosa": "red", "versicolor": "green", "virginica": "blue"}
    for sp in df['species'].unique():
        subset = df[df['species'] == sp]
        plt.scatter(subset['sepal_length'], subset['sepal_width'], label=sp, color=colors[sp], alpha=0.7)
