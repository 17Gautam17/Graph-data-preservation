# Graph-data-preservation



A large number of social networks data have been publicly made available. The data consists of DOB, location, contacts, photos and bookmarks. These data can not only lead to leak of the social account of a user, but also lead to the link to his friends accounts too connected via his social networking account.

The problem comes when the adversary finds the name of the user while it is meant to be kept private according to the company policies. That’s why we need to make changes in the data so that the identity of any user is not revealed.

In parallel, several definitions and methods have been proposed to protect user privacy when publicly releasing these data. But here we use or represent the social network data via graph data consisting of user accounts as the nodes and links as edges. We explain the base of methods an adversary uses for the identification of these nodes before he attacks. We also explain the several methods for anonymization of our graph data and also apply here one of the graph modification techniques to anonymize our data without having any information loss such that the perturbed data has no less data than our actual data.
 


We are going to take a dataset of 10,000 edges of Github users and then apply k-anonymous algorithm on the dataset. We write code in python. We collect all the dataset in a dataframe (it is a multidimensional data structure that is provided by pandas library of python) that was given in a .csv file. Now, we applied algorithms in the dataset by finding the quasi identifier. Quasi-identifiers are pieces of information that are not of themselves unique identifiers, but are sufficiently well correlated with an entity that they can be combined with other quasi-identifiers to create a unique identifier. Quasi-identifiers can thus, when combined, become personally identifying information. This process is called re-identification. As an example, Latanya Sweeney has shown that even though neither gender, birth dates nor postal codes uniquely identify an individual, the combination of all three is sufficient to identify 87% of individuals in the United States. And in graphical data quasi identifiers are the vertices who have unique degree. For example in a sample graph of 8 vertices with vertex_id=[0,1,2,3,4,5,6,7] they have vertex_degree=[3,3,5,1,2,2,6,6] respectively then degree 5 of vertex_id=2 and degree 1 of vertex_id=3 are unique degrees that are quasi identifiers which we will be hiding by the use k-anonymous algorithm.   


