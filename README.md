# creative-recipe
A group project to generate a creative recipe-poem with NLP

The system in given a collection of recipes available to use on Wikibooks (https://en.wikibooks.org/wiki/Cookbook:Recipes). From Wikibooks it is possible to extract the recipes into a xlm file which is cleaned from links and other irrelevant elements, then preprocessed in order to get a list or recipes. A random recipe is then picked from the list and a list of ingredients is extracted from the recipe.

The list of ingredients is then transformed into a list of meronyms based on a given word. If an input word is given, the program finds the semantically most similar word with at least as many meronyms in WordNet as the number of ingredients given.
If an input word is not given, the program picks a word randomly with at least as many meronyms in WordNet as the number of ingredients given.

The system will substitute ingredients in the original recipe with the found meronyms and insert an adjective before the meronym to add a poetic feature with alliterations. The adjective are fetched from a json file and their first three characters are compared with the first three characters of the meronym.
