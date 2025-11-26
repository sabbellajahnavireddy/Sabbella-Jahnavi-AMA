## Table of Contents
1. What is fav icon in HTML?
2. What is an iframe?
3. What is align-self ?
4. What is git merge?
5. What is full join in sql?
6. Why do we use primary key in sql?
7. Explain em, rem, px?
8. What is the difference between absolute and relative position?
9. Use of media queries ?
10. Difference between flex and grid?
11. Why do we use sudo ?
12. What is display in CSS ?


## 1. Favicon in HTML
- A favicon is a small image displayed next to the page title in the browser tab.
- Example:
```html
 <!DOCTYPE html>
<html>
<head>
  <title>My Page Title</title>
  <link rel="icon" type="image/x-icon" href="/images/favicon.ico">
</head>
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

</body>
</html> 
```

## 2. Iframe in HTML
- An HTML iframe is used to display a web page within a web page.
- Example:
```html
<iframe 
    src="https://example.com" 
    width="600" 
    height="400">
</iframe>
```
## 3. Align-self in CSS
- Align-self in Flexbox is a CSS property that allows a single flex item to override the container’s align-items value.
```css
.container {
  display: flex;
  align-items: center; /* all items centered */
  height: 200px;
  background: #f0f0f0;
}
```
```css
.item.special {
  align-self: flex-end; /* only this item moves to bottom */
}
```
## 4. What is git merge?
- git merge is a Git command used to combine changes from one branch into another branch.
- Syntax
```
git merge branch-name
```
## 5. Full Join in SQL
- The FULL OUTER JOIN keyword returns all records when there is a match in left (table1) or right (table2) table records.
- Example:
```sql
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
FULL OUTER JOIN Orders ON Customers.CustomerID=Orders.CustomerID
ORDER BY Customers.CustomerName;
```

## 6. primary key in SQL?
- The PRIMARY KEY constraint is used to uniquely identify each record in a table.
- Primary keys must contain unique values, and cannot contain NULL values.
- Each table can have only ONE primary key. The primary key can be a single column or a combination of columns.
- Example:
```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    PRIMARY KEY (ID)
); 
```

## 7. About em, rem, px?
**em (Relative to parent element)**
- em = relative unit based on the parent element’s font-size

```css
.parent {
  font-size: 20px;
}

.child {
  font-size: 2em;   /* = 2 × 20px = 40px */
}
```

**rem (Relative to root HTML element)**
- rem = root em
- It depends ONLY on the browser’s root font-size.
- Example:
```css
html {
  font-size: 16px;
}
```

**px (Pixel)**
- Fixed (absolute) unit.
- It does NOT change based on parent or root.
- 1px = one pixel on the screen
- Always stays the same size
- Good for borders, small icons, sharp spacing
```css
font-size: 20px;
```

## 8. Difference between absolute and relative position
**position: relative**
- The element stays in the normal flow, but you can shift it relative to its original position.
- It does NOT leave a gap in the layout.
- It simply moves slightly from where it originally was.

- Example:
```css
.box {
  position: relative;
  top: 10px;   /* move 10px down */
  left: 20px;  /* move 20px right */
}
```

**position: absolute**

- The element is removed from the normal flow (other elements act like it does not exist).
- It is positioned relative to the nearest positioned parent (parent with position: relative, absolute, or fixed).
- If no such parent exists → it is relative to the viewport (page).
```css
.child {
  position: absolute;
  top: 10px;
  left: 20px;
}
```
## 9. Media query
- A media query is a CSS rule used to make your website responsive. It allows you to apply different styles based on:

- Screen size (mobile, tablet, laptop)
- Screen orientation
- Resolution
- Device type

- Example:
```css
@media (max-width: 600px) {
  body {
    background: lightblue;
  }
}
```
## 10. Difference between flex and grid
**Flexbox (Flexible Box Layout)**
- One-dimensional layout system
- Flexbox works in one direction at a time:
- Row (left → right)
- Column (top → bottom)

- Example
```css
.container {
  display: flex;
}
```
**Grid**
- Two-dimensional layout system
- Grid works in both rows and columns at the same time.

- Example
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
```
## 11. SUDO
- SUDO means Superuser Do
- sudo allows a normal user to run commands that need administrative/root permission.
```bash
sudo apt install git
```

## 12. Display in CSS
- Display is a CSS property that controls how an element behaves in the layout — how it sits on the page and how it interacts with other elements.
```css
.box {
  display: block;
}
```