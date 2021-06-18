# Funciones-para-visualización rápida con Seaborn
Diversas funciones para la visualización rápida de las características de una variable (columna de un dataframe) de la relación de dos o tres variables entre sí o de la correlación de todas las variables del dataframe (matriz de Phick).

La más completa es la función overview. 

Esta es su documentación:

 1. Description
    
    Function that graphically displays up to three variables through through the most appropiate kind of plot depending on the variables provided, as well as a Phick
    matrix in case that a whole dataframe is provided.
    
    - One numerical varible is displayed through a through a displot or a boxplot, if the argument boxplot is introduced.
    - One categorical variable is displayed through a countplot.
    - Two numeric variables are displayed through a scatterplot.
    - Two categorical variables are displayed through a catplot.
    - A categorical and a numeric variable are displayed through a treeplot.   
    - The relation between three variables is displayed through a scatterplot. The third variable is introduced as hue and must be a categorical or binary variable.
    - If a whole dataframe is provided, the function displays a Phick matrix for all variables in the dataframe.    
    
    2. Funtions used
    
    The overview function uses the following functions from this same library. 
    Please refer to their corresponding documentation for more clarification.
    
    - univariant
    - bivariant_num
    - bivariant_cat
    - bivariant_cat_num
    - bivariant_all
    - trivariant_num
    - phik_matrix_simple    
    
     
   3. Arguments
    
    - df: dataframe.
    - col_1:  dataframe´s column (i.e. series) containing the fist variable.
    - col_2: dataframe´s column (i.e. series) containing the second variable.
    - hue: dataframe´s column (i.e. string)containig a third variable to be displayed through the colors of the scatterplot´s points, which 
        be a categorical or binary variable. Hue takes None by default.
    - boxplot = It takes None by default. If scatter is informed as True, the function displays a boxplot instead of a histogram. This argument only works for type "one"               plotting functions and numeric variables.
    - kde = kde stands for Kernel Density Estimate, which is used for visualizing the probability density of a continuous variable.It takes None by default.
    - rotation = It takes None by default. If rotation is informed as True, the labels for x values are displayed with a 45 º rotation.
    - target: the name of the target´s colum. If informed as True, the function plots the correlation matrix of all variables (accumulated) with
        the target. It takes None by default.
    - color: The color to be displayed by the scatterplot when two numeric variables are provided. Color is red ("#A61D39") by default.
    - palette: the palette by default is "rocket".
    - nuevo_cmap: this argument is used to change the Phick matrix´s colormap by default. Example: nuevo_cmap = sns.diverging_palette(150, 275, s=80, l=55, n=9)
    - xlabel: False by default. It is used to define the xlabel. It must be introduced as a string.
    - ylabel: False by default. It is used to define the ylabel. It must be introduced as a string.
