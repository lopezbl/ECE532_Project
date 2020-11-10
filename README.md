# Update

Update 11/06/2020

Using nasa_sort.csv, the least squared algorithm was used to see which features were the most important. Using all the features, the expected classification error is 9.39%. A method of ranking the features by their impact on the expected error was used. This technique concluded there were 7 features that allowed for a expected classification error of 9.34% which means the other features had little to no impact on the classification. The 7 features are "Absolute Magnitude", "Est Dia in KM(max)", "Orbit Uncertainty", "Minimum Orbit Intersection", "Semi Major Axis", and "Perihelion Distance". The code used for this determine can be found under Least Squared.ipynb.

Update 11/02/2020

The data file and the corresponding code to load the data has been uploaded. The Load Data.ipynb removes unnecessary columns such as ID numbers and dates of discovery/calculations and columns that have repeat information in different units/scales. This brought the number of features from 39 to 19. A new nasa_sort.csv was created for later use from the selected features. Using this csv, then the study of the three different algorithms can be conducted.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/lopezbl/ECE532_Project/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
