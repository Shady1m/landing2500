This code dynamically generates a navigation menu based on the sections of a webpage and highlights the active section as the user scrolls through the page.

How to Use
To use this code, follow these steps:

Add an id attribute to each section of the webpage that you want to include in the navigation menu.
Add a data-nav attribute to each section with the text that you want to display in the navigation menu.
Add an unordered list element with an id of navbar__list where you want the navigation menu to appear.
Include this JavaScript code in your webpage.
How it Works
The code starts by selecting the ul element of the navigation menu using document.querySelector(). It then creates a DocumentFragment to build the navigation menu more efficiently. The code loops through all the sections on the webpage using document.querySelectorAll(), creates a new li element and a element for each section, sets the text of the a element to the data-nav attribute of the corresponding section, sets the href attribute of the a element to the id of the corresponding section with a # prefix, adds a menu__link class to the a element, and attaches a click event listener to the a element that scrolls the page smoothly to the corresponding section. The li element is then appended to the DocumentFragment. Once all the li elements have been created, the DocumentFragment is added to the ul element using appendChild().

The code also defines a sectionActiveState() function that adds an active class to the section in view and highlights the corresponding navigation menu item. The function gets all the section elements on the page using document.querySelectorAll(), listens for scroll events on the window using window.addEventListener(), loops through each section element, gets the bounding rectangle of the section using getBoundingClientRect(), and checks if the top of the section is within the viewport. If the section is in view, the your-active-class is added to the section, and the corresponding navigation menu item is highlighted with the active__link class. If the section is not in view, the your-active-class is removed from the section.

The sectionActiveState() function is called at the end of the code to initialize the active section and navigation menu item.