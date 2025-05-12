 /*10px as default size. browser is 16px --> then, 1rem is 10px*/
    font-size: 62.5%;

If you wanted to add more social icons, but keep them on the same row, you would need to update grid-template-columns to create additional columns. As an alternative, you can use the grid-auto-flow property.
This property takes either row or column as the first value, with an optional second value of dense. grid-auto-flow uses an auto-placement algorithm to adjust the grid layout. Setting it to column will tell the algorithm to create new columns for content as needed. The dense value allows the algorithm to backtrack and fill holes in the grid with smaller items, which can result in items appearing out of order.

 grid-auto-flow: column;

Now the auto-placement algorithm will kick in when you add a new icon element. However, the algorithm defaults the new column width to be auto, which will not match your current columns.


You can override this with the grid-auto-columns property.

grid-auto-columns: 1fr;

Much like Flexbox, with CSS Grid you can align the content of grid items with align-items and justify-items. 
--> align-items: column axis (hoch / runter)
--> justify-items:  row axis.

you can create columns within an element without using Grid by using the column-width property.
===> Zeitungsoptik
--> Spalten: column-width: 25rem;
--> Spalten glätten: text-align: justify


target first letter:
.first-paragraph::first-letter {
    font-size: 6rem;
}

correct moving of the text:
float: left;
margin-right: 1rem;
(same selector)

To give the hr a color, you need to adjust the border property. 
hr {
    margin: 1.5rem 0;
    border: 1px solid rgba(120, 120, 120, 0.6);
}


styling the quote:
.quote {
    color: #00beef;
    font-size: 2.4rem;
    text-align: center;
    font-family: Raleway, sans-serif;
}

place-items: align-items und justify-items at the same time. 
