# HTML5

## HTML5 Structure

HTML5 with CSS provides an effective way to structure web pages. There are specific elements that can be used to define the document structure contain structure. 

These are:
- header - top of the element or page
- footer - bottom of the element or page
- main - content of the page
- nav - navigation links
- section - portion or area of the page and groups things together
- article - content accompaying the main content
- aside - content that is supplementary 

```
-------------------------------------
|             header                |
-------------------------------------
|              main                 |
|-----------------------------------|
|         |   section   |           |
|         |-------------|   aside   |
|         |   article   |           |
|   nav   |-------------|-----------|  
|         |   article   |           |
|         |-------------|   aside   |
|         |   section   |           |
-------------------------------------
|              main                 |
|-----------------------------------|
|             footer                |
-------------------------------------
```

The structure elements can contain each other to help structure the page. The following table lays out if the element can be a child or parent of other elements:

Top Row is 'As Parent' 
Side Row is 'As Child'


|         | header  | nav     | main    | section | article | aside   | footer  | 
| :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: |
| header  |         |    X    |    X    |    X    |    X    |    X    |         |
| nav     |    X    |         |         |    X    |         |         |         |
| main    |         |         |         |    X    |         |         |         |
| section |         |         |         |    X    |    X    |         |         |
| article |         |         |    X    |    X    |         |         |         |
| aside   |         |         |         |    X    |         |         |         |
| footer  |         |    X    |    X    |    X    |    X    |    X    |         |
