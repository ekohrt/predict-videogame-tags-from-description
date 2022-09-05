# Predict a Game's Tags from its Description
Each video game on the online Steam store has a text description and a set of user-defined tags. Is it possible to predict a game's tags from just the text description? We test this hypothesis on a heavily-cleaned dataset of [80000 Steam Games](https://www.kaggle.com/datasets/deepann/80000-steam-games-dataset) from Kaggle.  
  
To predict the tags, we vectorize the text using TF-IDF and train a scikit-learn MultiOutputClassifier, which uses a separate Linear Regression classifier for each tag. The dataset contains 424 unique tags, which is far too many for this kind of model, but since most tags are used only a few times, we chose to limit the set to just the top 30 most frequent tags.  
  
<img src="example_image.png" width="600" height="200" title="Art made with Disco Diffusion"/>
