#   TABLES (HTML)

#### What's a Table?

A table represents information in a grid format. Examples of tables include financial reports, TV schedules, and sports results.

Grids allow us to understand complex data by referencing information on two axes.

Each block in the grid is referred to as a table cell. In HTML a table is written out row by row.

#### basic Table structure

### `<table>`

The `<table>` element is used to create a table. The contents of the table are written out row by row.

### `<tr>`

You indicate the start of each row using the opening `<tr>` tag. (The tr stands for table row.)

It is followed by one or more `<td>` elements (one for each cell in that row).

At the end of the row you use a closing `</tr>` tag.

### `<td>`

Each cell of a table is represented using a `<td>` element. (The td stands for table data.)

At the end of each cell you use a closing `</td>` tag.

#### Samples

```
<table> 
  <tr>
    <td>15</td> 
    <td>15</td> 
    <td>30</td>
  </tr> 
  <tr>
    <td>45</td> 
    <td>60</td> 
    <td>45</td>
  </tr> 
  <tr>
    <td>60</td> 
    <td>90</td>   
    <td>90</td>
  </tr>
</table>
```

`result`
<table> 
  <tr>
    <td>15</td> 
    <td>15</td> 
    <td>30</td>
  </tr> 
  <tr>
    <td>45</td> 
    <td>60</td> 
    <td>45</td>
  </tr> 
  <tr>
    <td>60</td> 
    <td>90</td>   
    <td>90</td>
  </tr>
</table>

### `<th>`
The `<th>` element is used just like the `<td>` element but its purpose is to represent the heading for either a column or a row. (The th stands for table heading.)

Even if a cell has no content, you should still use a `<td>` or `<th>` element to represent the presence of an empty cell otherwise the table will not render correctly. (The first cell in the first row of this example shows an empty cell.)

Using `<th>` elements for headings helps people who use screen readers, improves the ability for search engines to index your pages, and also enables you to control the appearance of tables better when you start to use CSS.

You can use the scope attribute on the `<th>` element to indicate whether it is a heading for a column or a row. It can take the values: row to indicate a heading for a row or col to indicate a heading for a column.

#### Sample

```
<table> 
  <tr>
    <th></th>
    <th scope="col">Saturday</th>  
    <th scope="col">Sunday</th>
  </tr>  
  <tr>
    <th scope="row">Tickets sold:</th> 
    <td>120</td>
    <td>135</td>
  </tr> 
  <tr>
    <th scope="row">Total sales:</th> 
    <td>$600</td>
    <td>$675</td>
  </tr>
</table>
```

`result`
<table> 
  <tr>
    <th></th>
    <th scope="col">Saturday</th>  
    <th scope="col">Sunday</th>
  </tr>  
  <tr>
    <th scope="row">Tickets sold:</th> 
    <td>120</td>
    <td>135</td>
  </tr> 
  <tr>
    <th scope="row">Total sales:</th> 
    <td>$600</td>
    <td>$675</td>
  </tr>
</table>

# Functions, Methods, and Objects (JS)

### CREATING OBJECTS USING CONSTRUCTOR SYNTAX

On the right, an empty object called hote1 is created using the constructor function.

Once it has been created, three properties and a method are then assigned to the object.

(If the object already had any of these properties, this would overwrite the values in those properties.)
To access a property of this object, you can use dot notation, just as you can with any object.

For example, to get the hotel's name you could use:
hotel .name

Similarly, to use the method, you can use the object name followed by the method name: hotel.checkAvailability()

#### Smaple 
```
var hotel = new Object();
hotel.name= 'Park';
hotel.rooms = 120;
hotel .booked = 77;
hotel .checkAvailability = function(){     
return this.rooms - this.booked; };
var elName = document.getElementByid('hotelName'); elName.textContent = hotel . name;
var elRooms = document.getElementByid('rooms'); elRooms.textContent = hotel .checkAvailability();
```