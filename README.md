# gender-detector-model

In this Project we worked on a simple classification probleme using categorical data.
Since the Algerian companies need is not to get information only from algerian name so we had to use *First Names* from all over the world.
## About the data

- The first dataset used in this project is from kaagle : https://www.kaggle.com/datasets/kaggle/us-baby-names
But since the dataset need to get enriched with african names and others written in arabic we had to do some scraping to get more data to get a strong model
- We scraped mainly : https://angelsname.com

### Some EDA visualization
<div class="container" align="center">
<!--     <h3 align="rigth">Gender Pie Chart</h3> -->
    <img align="rigth" src="https://user-images.githubusercontent.com/88236219/226207844-846b7c7d-4f29-432f-a737-fa937a844d81.png" 
         width="400" title="Data repartition" hspace="20"/>
<!--     <h3 align="left">WordCloud</h3> -->
    <img align="left" src="https://user-images.githubusercontent.com/88236219/226318990-571f681a-38b4-47ba-8846-305049fd4d5e.png" 
         width="400" title="Names WordCloud"/>
</div>



## The data treatement

### The cleaning roadmap
1. Remove the emojes
2. Transform letters with attachments to their correspanding letter
3. Clean the names from punctuation, spaces, and lower them
4. translate names written in arabic to latin, and correct the translation errors 

### Encoding
1. Names
    - We encoded our names to matrix of 27x20
        * 27 rows := 26 is the alphabet + 1 the space
        * 20 columns := is the maximum length accepted for a name
    - How ?
        * every row is considered as a letter from the name and we put a 1 at the correspending position of the letter in the alphabet
    - Exemple : 
    ```
        Amine = [[1,..,0],
                [0,...,1,...,0],
                [0,...,1,...,0],
                [0,...,1,...,0],
                [0,0,0,0,1,...,0],
                ...,
                [0,...,0]]
    ```
2. Genders
    - We encoded the genders as following
    ```
        0 = 'Man'
        1 = 'Woman'
    ```
## Model Building

## Model Performance

# Productionisation

To have more vision about this part visit this repository : https://github.com/zidelmal/gender-predictor-webapp/

# References

* https://ceur-ws.org/Vol-2754/paper3.pdf
* https://www.geeksforgeeks.org/python-gender-identification-by-name-using-nltk/
* https://www.kaggle.com/code/karsteneckhardt/predicting-gender-from-first-names-with-an-lstm/notebook
 

