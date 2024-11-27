Requirement.md
####Address Book
###Requirements:
I am trying to create a simple address book using HTML, CSS, and
JavaScript.
###Features:
- Add a new contact
- Delete a contact
- Search for a contact
- View all contacts
###Technologies:
Front end:
- HTML
- CSS
- JavaScript
Pages:
- index.html
I want 3 sections:
-Header:
i want the title Address Book on the left and 3 buttons on the right:
Home, AddContact, ViewContacts. Align the title to the left and the
buttons to the right.
-main section:
A header "Welcome to Address Book application"
A paragraph "You can add, delete, search and view contacts here"
Two cards with a button each: Add Contact, View Contacts. Each
card hasa small description and a button. the cards must be aligned in
the center of the page.
Each of the elements must be aligned in the center of the page and
must be
one below the other.
-footer:
A paragraph "Address Book. Copyright 2024"
- add.html
- A form with the following fields:
- First Name
- Last Name
- Email
- Phone
- Address
- notes
- A submit button
- A clear button
- The form must be aligned in the center of the page.
the header and footer must be same as in index.html
- view.html
- A table called as contactListwith the following columns:
- First Name
- Last Name
- Email
- Phone
- Address
- Action (Delete) (Edit)
- The table must be aligned in the center of the page.
- The header and footer must be same as in index.html
-edit.html
- A form with the same fields as in add.html name editContact
- The form must be aligned in the center of the page.
- The header and footer must be same as in index.html
- The form must be prefilled with the contact data to be edited
Back end:
- Create a model class (POJO) called Contact with the following fields:
- id (primary key)
- firstName
- lastName
- email
- phone
- address
- notes
- Create a DAO class called ContactDAO with the following methods:
- addContact(Contact contact)
- deleteContact(int id)
- getContactById(int id)
- getAllContacts()
- updateContact(Contact contact)
- also make sure the dao class has the jdbc connection code to
connect to the database
- i am using mysql connector jar file to connect to the database
- username: root
- password: root
- dont forget to use class.forname() to load the mysql connector jar file
Servlet
JSP
JDBC
Database:
- MySQL
- create a database called addressbook
-create a table called contacts with the following columns:
- id (primary key)
- firstName
- lastName
- email
- phone
- address
- notes
- 5 rows of data must be inserted in the table and names must indian.
Styleguide.md
# Address Book Style Guide
This style guide outlines the design principles, color schemes, typography, and
component styles for the Address Book application. The aim is to create a
**dark mode** interface that is **aesthetic**, **bold**, and **modern**,
ensuring a consistent look and feel across the application.
---
## Color Palette
### Primary Colors
- **Background Color**: `#121212` (Dark Gray)
- **Primary Accent Color**: `#BB86FC` (Light Purple)
- **Secondary Accent Color**: `#03DAC6` (Teal)
### Text Colors
- **Primary Text**: `#FFFFFF` (White)
- **Secondary Text**: `#B0B0B0` (Light Gray)
- **Disabled Text**: `#666666` (Dark Gray)
### Button Colors
- **Primary Button Background**: `#03DAC6` (Teal)
- **Primary Button Text**: `#000000` (Black)
- **Secondary Button Background**: `#BB86FC` (Light Purple)
- **Secondary Button Text**: `#000000` (Black)
### Border and Divider Colors
- **Border Color**: `#333333` (Dark Gray)
- **Divider Color**: `#444444` (Medium Gray)
---
## Typography
### Font Family
- **Primary Font**: `'Roboto', sans-serif`
### Font Weights
- **Light**: 300
- **Regular**: 400
- **Medium**: 500
- **Bold**: 700
### Font Sizes
- **Heading 1 (h1)**: 36px
- **Heading 2 (h2)**: 30px
- **Heading 3 (h3)**: 24px
- **Heading 4 (h4)**: 20px
- **Body Text**: 16px
- **Small Text**: 14px
---
## Layout and Spacing
### Grid System
- Use a **12-column grid system** for layout consistency.
- **Gutter Width**: 24px
- **Margin**: 16px
### Spacing Units
- **Base Unit**: 8px
- **Example Spacing**:
- **Extra Small (xs)**: 4px
- **Small (s)**: 8px
- **Medium (m)**: 16px
- **Large (l)**: 24px
- **Extra Large (xl)**: 32px
---
## Components
### Header
- **Background Color**: Same as primary background (`#121212`)
- **Height**: 80px
- **Title (Address Book)**:
- **Font Size**: Heading 1 (36px)
- **Font Weight**: Bold (700)
- **Color**: Primary Text (`#FFFFFF`)
- **Alignment**: Left
- **Navigation Buttons**:
- **Font Size**: Body Text (16px)
- **Font Weight**: Medium (500)
- **Color**: Primary Text (`#FFFFFF`)
- **Background**: Transparent
- **Hover State**: Underline text
- **Alignment**: Right
- **Layout**: Use Flexbox to align title to the left and buttons to the right.
#### Example CSS for Header
```css:styles/header.css
/* Header Styles */
header {
background-color: #121212;
height: 80px;
display: flex;
align-items: center;
padding: 0 16px;
}
header h1 {
font-size: 36px;
font-weight: 700;
color: #FFFFFF;
flex-grow: 1;
}
header nav {
display: flex;
}
header nav button {
background: none;
border: none;
color: #FFFFFF;
font-size: 16px;
font-weight: 500;
margin-left: 16px;
cursor: pointer;
}
header nav button:hover {
text-decoration: underline;
}
```
### Main Section
- **Alignment**: Centered horizontally.
- **Header ("Welcome to Address Book application")**:
- **Font Size**: Heading 2 (30px)
- **Font Weight**: Bold (700)
- **Color**: Primary Text (`#FFFFFF`)
- **Paragraph**:
- **Font Size**: Body Text (16px)
- **Font Weight**: Regular (400)
- **Color**: Secondary Text (`#B0B0B0`)
- **Cards**:
- **Display**: Flexbox, centered.
- **Width**: 300px
- **Background Color**: `#1E1E1E` (Slightly lighter than background)
- **Border Radius**: 8px
- **Padding**: 16px
- **Margin**: 16px
- **Shadow**: `0 4px 6px rgba(0, 0, 0, 0.1)`
- **Card Titles**:
- **Font Size**: Heading 3 (24px)
- **Font Weight**: Bold (700)
- **Color**: Primary Text (`#FFFFFF`)
- **Card Text**:
- **Font Size**: Body Text (16px)
- **Font Weight**: Regular (400)
- **Color**: Secondary Text (`#B0B0B0`)
- **Buttons**:
- **Style**: Primary button styles.
#### Example CSS for Main Section
```css:styles/main.css
/* Main Section Styles */
main {
text-align: center;
padding: 32px 16px;
}
main h2 {
font-size: 30px;
font-weight: 700;
color: #FFFFFF;
margin-bottom: 16px;
}
main p {
font-size: 16px;
font-weight: 400;
color: #B0B0B0;
margin-bottom: 32px;
}
.cards {
display: flex;
justify-content: center;
flex-wrap: wrap;
}
.card {
background-color: #1E1E1E;
border-radius: 8px;
width: 300px;
padding: 16px;
margin: 16px;
box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
.card h3 {
font-size: 24px;
font-weight: 700;
color: #FFFFFF;
margin-bottom: 8px;
}
.card p {
font-size: 16px;
font-weight: 400;
color: #B0B0B0;
margin-bottom: 16px;
}
.card button {
width: 100%;
padding: 12px;
background-color: #03DAC6;
color: #000000;
border: none;
border-radius: 4px;
font-size: 16px;
font-weight: 500;
cursor: pointer;
}
.card button:hover {
background-color: #00C4B4;
}
```
### Footer
- **Background Color**: Same as primary background (`#121212`)
- **Text**:
- **Font Size**: Small Text (14px)
- **Font Weight**: Regular (400)
- **Color**: Secondary Text (`#B0B0B0`)
- **Alignment**: Centered
- **Height**: 60px
#### Example CSS for Footer
```css:styles/footer.css
/* Footer Styles */
footer {
background-color: #121212;
height: 60px;
display: flex;
align-items: center;
justify-content: center;
}
footer p {
font-size: 14px;
font-weight: 400;
color: #B0B0B0;
}
```
---
## Buttons
### Primary Button
- **Background Color**: `#03DAC6` (Teal)
- **Text Color**: `#000000` (Black)
- **Border**: None
- **Border Radius**: 4px
- **Padding**: 12px 24px
- **Font Size**: 16px
- **Font Weight**: Medium (500)
- **Cursor**: Pointer
- **Hover State**:
- **Background Color**: Darker Teal
- **Effect**: Slight elevation or shadow
### Secondary Button
- **Background Color**: `transparent`
- **Text Color**: `#BB86FC` (Light Purple)
- **Border**: `1px solid #BB86FC`
- **Border Radius**: 4px
- **Padding**: 12px 24px
- **Cursor**: Pointer
- **Hover State**:
- **Background Color**: `#BB86FC` (Light Purple)
- **Text Color**: `#000000` (Black)
---
## Forms and Inputs
- **Background Color**: `#1E1E1E` (Dark Gray)
- **Border**: `1px solid #333333` (Dark Gray)
- **Border Radius**: 4px
- **Padding**: 12px
- **Font Size**: 16px
- **Font Weight**: Regular (400)
- **Text Color**: Primary Text (`#FFFFFF`)
- **Placeholder Text Color**: `#666666` (Dark Gray)
- **Focus State**:
- **Border Color**: `#03DAC6` (Teal)
- **Outline**: None
---
## Icons
- Use icons from the **Material Design Icons** library.
- **Icon Color**: Primary Text (`#FFFFFF`)
- **Size**: 24px
---
## Effects
### Shadows
- **Card Shadows**: `0 4px 6px rgba(0, 0, 0, 0.1)`
- **Button Hover Shadows**: `0 2px 4px rgba(0, 0, 0, 0.2)`
### Transitions
- Apply smooth transitions for interactive elements.
- **Duration**: 200ms
- **Properties**: `background-color`, `box-shadow`, `color`
Example:
```css
button {
transition: background-color 200ms ease, box-shadow 200ms ease;
}
```
---
## Imagery
- Use flat illustrations or subtle animations that match the modern and bold
aesthetic.
- Avoid overly complex images that can clutter the interface.
---
## Accessibility
- Ensure sufficient color contrast between text and background.
- Use ARIA labels where necessary for screen readers.
- Provide focus states for interactive elements.
---
## Responsive Design
- The application should be fully responsive and optimized for various screen
sizes including desktops, tablets, and mobile devices.
- Use media queries to adjust layouts and font sizes.
---
## Example Implementation
### index.html
```html:AddressBook/index.html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Address Book</title>
<link rel="stylesheet" href="styles/header.css">
<link rel="stylesheet" href="styles/main.css">
<link rel="stylesheet" href="styles/footer.css">
</head>
<body>
<!-- Header Section -->
<header>
<h1>Address Book</h1>
<nav>
<button>Home</button>
<button>Add Contact</button>
<button>View Contacts</button>
</nav>
</header>
<!-- Main Section -->
<main>
<h2>Welcome to Address Book application</h2>
<p>You can add, delete, search and view contacts here</p>
<!-- Cards Section -->
<div class="cards">
<!-- Add Contact Card -->
<div class="card">
<h3>Add New Contact</h3>
<p>Create a new contact with name, phone, email and address
details</p>
<button>Add Contact</button>
</div>
<!-- View Contacts Card -->
<div class="card">
<h3>View All Contacts</h3>
<p>See all your contacts, search, edit or delete them</p>
<button>View Contacts</button>
</div>
</div>
</main>
<!-- Footer Section -->
<footer>
<p>Address Book. Copyright 2024</p>
</footer>
</body>
</html>
```
---
## Conclusion
By following this style guide, the front-end developers can implement a dark
mode interface that is both aesthetic and modern. Consistency in design
elements such as color, typography, and component styling will ensure a
seamless user experience across the Address Book application.
---
**Note**: All colors, font sizes, and other measurements are specified in pixels
(px) for clarity but can be adapted to use relative units like `rem` or `em` as
per best practices.
---
Feel free to reach out for any clarifications or further assistance with the
design implementation.