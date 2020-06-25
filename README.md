1. Be built using a mobile first approach (This should be reflected in the structure of the CSS).

mobile first, @media used for min-width 1024px

2. Be responsive.The page should have two layout versions: one for smartphone and small tablet, and one for large tablet, notebook and desktop as shown in the mockups. Responsiveness should be achieved using media queries.

smartphone and small tablet - Max Width: 1024px
large tablet, notebook and desktop - Min Width: 1024px

3. Be cross browser compatible with the latest versions of Chrome, Firefox and Internet Explorer, as well as with IE9 and IE10. To ensure maximum cross browser compatibility you should include an example of CSS reset, an example of the use of feature queries and an example of the use of a vendor specific prefix.

Used Normalize.css

4. Be predominantly laidout using CSS grid.

CSS Grid used

5. Include examples of at least three of the following CSS 3 techniques:


a. Child combinator. 

.news__shop ul > li > p {
  color: #016008;
}

.news__shop ul > li > p span {
  color: #000;
}

b. Sibling combinator

section + footer {
  margin-top: 20px;
}

c. Attribute selector
        label {
          &[for="email"] span {
            color: #ff0000;
          }
        }
d. Position pseudo classes

@media screen and (min-width: 1024px) {
  .header .header__logo span:last-child {
    font-size: 5rem;
    margin-top: 0.18em;
  }
}

6. Be standards compliant.


7. Conform as closely as possible to the design provided in the mockups.


2.2 Critique of Grid Layout
Write a short evaluation of CSS grid layout. This should include a description of the grid layout technique. Advantages and disadvantages of the technique. Plus, a comparison with other layout techniques. The evaluation should be between 600 and 700 words.

CSS Grid layout is a two-dimensional system for CSS.  It divides the page into different regions and define their relationships with sizes, positions and layers, and it also allows the authors to divide elements into columns and row
A grid is a set of intersecting horizontal (rows) and vertical (columns) lines. Grids can be created with fixed track (i.e. by using pixels – these stay fixed and not resize based on the size of the page) and flexible sizes (i.e. percentages or fr, resizing the grid based on the screen size or it’s parent size)

The items can be placed into precise location using line number, names or by creating grid areas. The grid layout can have explicit grids, it is flexible to add additional rows and columns when needed
When it comes to the items, grid has alignment features that can control how the items align into a grid, and how the entire grid itself is aligned. It also has great control for overlapping content, by using the z-index property. The content of the pages can be layered on top if each other.
A grid starts with a container by declaring display: grid or display: inline-grid on an element. This will make all direct children of that container to become the grid items.

Rows and columns will then need to be defined by declaring grid-template-columns and grid-template-row properties which will define the grid tracks which can then have their own unit of length – whether it be by percentage or pixels. Although, the best way to do it is by using the fr which represents the fraction of the area in the container, which changes depending on the screen size of the page.

As opposed to writing the fr when there are multiple, it can also be repeatead by using the repeat() notation. i.e. as opposed to grid-template-columns: 1fr 1fr 1fr it could be repeated as grid-template-columns: repeat(3, 1fr).

Grids can also be nested within grids, this is when an item of a grid container element has been turned into a grid itself. The grid items can be positioned in the grid based on the cell lines. i.e. a 3x3 grid would have 4 lines. An item with using grid-column-start: 1; grid-column-end: 4 will fill the first row. Rows would use grid-row-start and grid-row-end 
With responsive grids, grid-template areas can be used to define the grid item column and row position based on the screen size via media queries.
justify-items and align-items can be used to align the items within the grid. Justify items is used for horizontal alignment while align items is used to vertically align items. 

Advantages and disadvantages:
An advantage of using grid is that it reduces the amount of code needing of writing. Instead of creating more HTML elements to create the grids, then its columns and its rows, the styles sheet would create it for you. It’s also native, which means there aren’t other files needed to be included within the project.
Another advantage is, the semantics are clearer and stays in the CSS file. As opposed to something like Bootstrap, less class names are needed to be written to individual elements to create the grid, and it’s also fast and efficient as you wouldn’t need to learn class names that then needs to be put in elements.
A disadvantage of grids is that it differs on how grids were done before it was introduced  as it uses properties and values in CSS, while previously, frameworks such as Bootstrap was used which is done via adding class names to the HTML elements; therefore, some may find it difficult to learn or adapt


Grids and Flexbox comparison: The main difference between Grid and Flexbox is that Grid is used to design two-dimensional layout, while Flexbox is used for one dimensional layout.

Another difference between the two is, flexbox focuses more on the content. It would work by creating the layout based on the content that can evenly fill a container. While with grids, it would with the layout first, before the contents. It defines what the layout of the grid would be like, and then the contents are added in.
