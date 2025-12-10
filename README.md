This repository is for homework assignments for Dr. Karimi, California State University of San Marcos. It is not in your interest to utilize the information, there are errors. I am learning and I am documenting my assignments as I go. This repository is utilizng Visual Studio Code (Python), I am describing what did. I suggest you look at the Python notebook for more context. The dataset has been provided for me.

**Main GitHub page [aeczuniga.github.io](https://aeczuniga.github.io/)**

# Assignments
**GitHub**

***

The **first Python assignment** is data cleaning. This assignment is more of an introductory to  data, ensuring it is ready to be analyzed further, primarily focusing on inventory, made to stock (MTS) items. 

The **first question** is looking at formatting, not all datasets are formatted in a way that is easy to work with, usually I have to apply some sort of transformation. The easiest way is to understand a dataset is by knowing how columns are formatted, like text versus integer. What I ended up doing is renaming three columns that are not matching the rest of the dataset using the **_rename_** function. 

The **second question** is looking at "oddities" in the dataset, outliers. I use the **_describe_** function and notice that two SKUs have negative costs, the problem here is that both SKUs occur more than 700+ times. However, the negative costs only appear once for each SKU...read the notebook for more information.
        A little snippet of the notebook in Python
                However, the instance in which the negative price occurs in **SKU 2D43CB75**, there is a null value in column "manufacturing_site," I do not have to drop this, when I drop null values it will go away. However, the instance in which the negative price price occurs in **SKU 2D43CB75**, there is no null values in any of the other columns...
Another realization is the the lead time, it is large.

The **third question** is finding _null | NaN | empty_ values. Using the **_print_** function identifies the amount of null values per column. Knowing that I want to calculate safety stock (SS) values by SKU, I want to drop _null | NaN | empty_ values in the sku column. I use a **_dropna_** function.

The **fourth question** is identifying relevant information, unique SKUs, manufacturing sites, divisions, top and bottom 10...I end up adding a custom column for sales. However, it is important to note that the question identifies items that are "made to stock" (MTS), I filter all data by the column **stocking_type** to ensure it is **MTS**. 


***

The **second Python assignment** continues using the data from the previous assignment. This assignment calculates safety stock for various sevice levels. The assignment begins by calculating aggregated statistics and utilizing the transformed data for calculations. The assignment ends with the  calculated average safety stock for all SKUs and the identification of the SKU with the greatest and smallest amount of safety stock.

