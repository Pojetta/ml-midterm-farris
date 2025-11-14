# Peer Review: Sabriya Sowers' Mushroom Classification Analysis  
[Sabriya Sowers – Mushroom Classification Notebook](notebooks/project01/classification_sowers.ipynb)

## 1. Clarity & Organization  
The notebook is easy to follow and the section labels make the workflow clear. The short reflection notes after each step were helpful.  
**Suggestion:** turning the “Reflection X” lines into actual Markdown headings would make them stand out more when scrolling.

## 2. Feature Selection & Justification  
Your choice to use all encoded features makes sense for this dataset, and you pointed out the ones you expected to matter most (odor, gill_size, spore_print_color).  
**Suggestion:** the mapping of `class` happens twice, and the `X_all` vs `X` naming got a bit confusing. Cleaning that up would make this section read more smoothly.

## 3. Model Performance & Comparisons  
Both models getting 100% accuracy fits what we expect from this dataset, and you explained the results clearly. The confusion matrices were a nice touch.  
**Suggestion:** running a quick cross-validation or trying a different train/test split would show whether the perfect accuracy holds beyond the single split.

## 4. Reflection Quality  
Your reflections were thoughtful and connected well to the steps you took. I especially liked the notes about handling many one-hot-encoded features.  
**Suggestion:** adding a sentence about what surprised you the most (about the data or the modeling) would make the reflection feel a bit more personal.
