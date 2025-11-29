# SkyAirlines – Airport Ticket Reservation System (MEVN)
## Author 
Panagiotis Leftheriotis

## Contact
[p.leftheriotis@gmail.com](mailto:p.leftheriotis@gmail.com)

## Contents

- [Technologies Used](#technologies-used)
- [File Description](#file-description)
- [User Manual](#user-manual)

## Technologies Used
The technology stack that defined the implementation of the airline's application is MEVN. The MEVN stack consists of MongoDB, Express.js, Vue.js and Node.js technologies which combine seamlessly to create excellent web applications.
### MongoDB
MongoDB is a NoSQL, document-oriented open source database. It was chosen because it allows for a lot of flexibility in storing data because it is stored directly in the form of records within collections. It provides the ability to model complex data structures, such as flight itineraries and customer tickets, and store them in real time. In this particular application, MongoDB Atlas, a cloud-based database service provided by MongoDB, was used as it best served the connectivity and development needs of the application's database. The application's connection to the database is done using Node.js, while the management of requests to the database is done with Express.js.

### Express.js
Express.js is a lightweight and flexible Node.js framework for developing web applications. It offers a multitude of functions and in the case of the airline application it helps in managing routes and HTTP requests. Using Express.js, the application interacts with the MongoDB database to make ticket reservations, create accounts and flights. Specifically, the Express.js framework is used in the flights.js, tickets.js, transactions.js and users.js files of the “routes” folder to create routes from which the application exchanges data with the database, where each file corresponds to a “collection” of the database as the file name indicates.

### Vue.js
Vue.js is a JavaScript framework that provides functions for creating dynamic interfaces. Compared to the corresponding React and Angular frameworks, it was chosen as it is a combination of these two technologies, offering excellent results and an extensive set of tools. A large part of the Front-End of the application has been based on Vue.js as it is easy to use and its simple code structure provided the possibility of reusing it in many pages of the application.
This framework is used in all HTML files except “homepage.html” to implement the “Dark Mode” function that allows the user to switch the colors of the application to darker tones. The framework is also used in the “user_ticketHistory.html” file to create a table containing the user's transaction data and in the “user_transaction.html” file to dynamically display an image based on the user's selection from the “user_homepage.html” page.
### Node.js
Node.js provides an environment for executing JavaScript code mainly on the server side and is an efficient way to develop applications. In combination with the Express.js framework, it constitutes the server of the airline application as it manages the requests that occur in real time.
In the application files, Node.js is used in “app.js” to create the server through the Express framework, define the application “routes”, configure the Nodemailer package that allows sending emails from the application and connect to the MongoDB database through the Mongoose library. In the application HTML files, Node.js is not used directly but the server services are called through the Fetch API requests made by the client depending on the user’s actions.

### Additional technologies
In addition to the MEVN technology stack used for the development of the application, other technologies were used to implement both the Front-End part of the application and the execution of requests to the server.

### HTML
HTML is the basic text language used to create the structure of each page of the application. All HTML files follow a similar structure, using the header to declare the file type via Doctype, the metadata declaration for the specific file and the connection of external libraries and files such as CSS, Bootstrap, Vue.js and jQuery. The body includes the content of each page such as the company logo, the navigation bar for easy user navigation in the application, etc. Finally, the footer includes information related to the copyrights of the application. Specifically, on the pages “homepage.html” and “user_homepage.html” images are used to display a map to the user and the map element for the user to interact with the map in order to display relevant information. Additionally, on the pages “signUp.html”, “signIn.html”, “user_transaction.html”, “admin_users.html” and “admin_flights.html” fields, buttons and radio buttons are used so that the user can execute requests to the application server to register or log in to the application and book tickets, while the administrator can edit the users and flights registered in the database.

### CSS
CSS is a programming language used to format and better display the content of HTML files. Its use was necessary as the well-designed presentation of the application is a key factor in attracting new customers to the airline. It was used in all HTML pages to modify them mainly as an external “style.css” file and by linking it to the head of each page.
The role of the CSS language was particularly important for creating responsive elements on the application pages through media queries that allow the size of the logo and fonts to be changed depending on the size of the user’s screen, making the application accessible from all devices.

### Bootstrap
Bootstrap is a Front-end framework that contains CSS elements and other tools for creating dynamic web applications. The airline application owes its dynamic design to Bootstrap as all HTML pages used the grid system and the containers it provides for the structured and dynamic representation of the elements of each page. Specifically, the classes “row”, “col-2”, “col-md” and “col-md-6” were used, which adapt their content depending on the screen size. On the pages “homepage.html” and “user_homepage.html” the classes “rounded” were used to format the images so that their edges are rounded and the “mx-auto” and “d-block” were used to align the image in the center of the column in which it is located. In addition, predefined classes for buttons offered by Bootstrap such as “btn”, “btn-dark”, “btn-primary” etc. were used as their formatting matched the design of the application. The “flights.html” and “user_transaction.html” pages use the default “card” format to present flights, as it provides a concise and easy-to-read representation of the basic details of each flight, allowing the user to browse through the available flights effortlessly. The “admin_flights.html”, “admin_users.html” and “user_ticketHistory.html” pages use the table class to present flight, user and transaction information in a table format, respectively. This structure was chosen because all three pages contain a large amount of information and it was necessary to present it in an organized manner so that it is accessible to all users and to use filters for better data management.

### JavaScript
JavaScript is a programming language used to add dynamic elements, perform functions based on user input, and communicate with the server to send requests. In the airline application, it is used on all pages in the form of a script within the HTML code, while JavaScript code is also used through external files, specifically “script.js” which contains the “Sign-Out” button function for logging out the user, and “gameScript.js” which contains the anagram game function. Within the HTML code, the Fetch API offered by simple JavaScript is used to create HTTP requests to the Node.js and Express.js application servers. In particular, the “user_transaction.html” page uses the asynchronous request feature through the async / await and promise syntax of JavaScript for functions that use the results of other functions as parameters so that many functions can be executed serially without problems. The functions mentioned are the functions createTicket, getTickets, createTransaction, reserveSeats, sendTicketEmail and deleteDiscountCode. This JavaScript function was also used in other scripts to ensure the smooth operation of the functions of each page. On the “signUp.html” page, a script is used to register the user in the application by sending the information they filled in on the page and storing it in the database. On the “signIn.html” page, a script is used to connect the user to the application by sending the user's login information and confirming the information from the database. An important role in the operation of the application was also played by session variables that allow values ​​to be stored in temporary variables and in this way the user's information and choices are stored until they are disconnected from the application.
JavaScript is an important part of the application as the Node.js, Express.js and Vue.js technologies are based on it and provide it with functions. All files that make up the application's routes are written in JavaScript code, as is the "app.js" file in which the core of the application is located.

### jQuery
JQuery is a JavaScript library that simplifies certain functions for easier interaction between HTML pages and the Server. In the airline application, its use was chosen because it simplifies certain functions used by multiple files and thus it was easy to reuse code for faster application development. Specifically, it is used in the “homepage.html” file to implement the “Dark Mode” function and the interactive map and in “flights.html” to retrieve available flights from the database and their structured representation in cards from Bootstrap. It is also used in the “signUp.html” file to send the user's details to register in the database and then connect to the application, in “signIn.html” to send the user's login details and confirm them from the database, and in “user_homepage.html” to display a message according to the user's name and for the operation of the interactive map and saving the country selected by the user.

## File Description
## User Manual

## Application Requirements
- Promotion of the company and its services: The main objective of the application is to increase the visibility of the company, its services, the countries it connects, the number of flights and the ticket prices it offers to a wider audience
- Online ticket purchase: Through the electronic application, users will be able to choose their flights and buy their tickets easily with just a few "clicks"
- Attracting customers due to competitive prices: The application will offer the possibility of a discount through a simple game that customers can easily win
- Reduction of staff: Online customer service will lead to a reduction in the staff involved in issuing tickets, providing information, etc.
- Ticket history: Full information to the customer about current and previous transactions
- Attract partners: Easy access to itineraries will make it easier for partners such as tourist offices and travel agents to choose the specific company
- Statistics: Storing tickets in the company's database will help in decision-making with the statistical study of customer preferences
## Modern Web Application Trends

## Application Technologies

## User Manual
  
## Επιπλέον Παραδοχές
- Όλες οι φόρμες χρήσης (κρατήσεις, αναζήτηση πτήσεων, είσοδος, εγγραφή) έχουν ελέγχους εγκυρότητας.

Τα δεδομένα των πτήσεων θεωρούνται έγκυρα και ενημερώνονται μόνο από τον διαχειριστή.

Τα usernames είναι μοναδικά.

Η τιμή των εισιτηρίων και η διαθεσιμότητα ενημερώνονται σε πραγματικό χρόνο κατά τη διάρκεια της κράτησης.

Τεχνολογίες που χρησιμοποιήθηκαν
Backend

Node.js – Εκτέλεση του server

Express.js – REST API routes & επιχειρησιακή λογική

MongoDB – Αποθήκευση χρηστών, πτήσεων και κρατήσεων

Mongoose – Μοντελοποίηση δεδομένων και schema validation

Frontend

Vue.js – Διεπαφή χρήστη

HTML5 / CSS3

Bootstrap – Σχεδιασμός & responsive στοιχεία

Axios – Επικοινωνία με το REST API

Other

RESTful API Architecture

JSON-based communication

npm για διαχείριση πακέτων

Περιγραφή των αρχείων

backend/app.js
Ο πυρήνας της εφαρμογής. Περιέχει τον Express server, σύνδεση με MongoDB και τα API routes.

backend/models/
Τα Mongoose models για:

Χρήστες

Πτήσεις

Κρατήσεις

backend/routes/
Περιέχει όλα τα REST API endpoints για:

Authentication

Flights

Bookings

backend/package.json
Βιβλιοθήκες & scripts του backend.

frontend/src/
Κύριος κώδικας Vue.js (σελίδες, components, views).

frontend/public/
Static αρχεία του front-end.

frontend/package.json
Βιβλιοθήκες & scripts του frontend.

docs/report.pdf
Προαιρετικό – αναλυτική τεκμηρίωση της εφαρμογής.

README.md
Το παρόν αρχείο που περιγράφει το σύστημα SkyAirlines.

Τρόπος Εκτέλεσης
1) Κατέβασμα του Project

Κατεβάζουμε ή κάνουμε clone το repository:

git clone https://github.com/your-username/your-repo.git
cd your-repo

2) Εκτέλεση Backend
cd backend
npm install
npm start


Ο server εκτελείται στο:
http://localhost:3000

3) Εκτέλεση Frontend
cd frontend
npm install
npm run serve


Το web interface εκτελείται στο:
http://localhost:8080

Τρόπος Χρήσης
Ως Χρήστης

Εγγραφή νέου χρήστη
Ο χρήστης μπορεί να δημιουργήσει λογαριασμό εισάγοντας τα στοιχεία του μέσω της σχετικής φόρμας.

Screenshot Placeholder

Σύνδεση στον λογαριασμό
Ο χρήστης συνδέεται εισάγοντας το username και τον κωδικό του.

Αναζήτηση πτήσεων
Ο χρήστης εισάγει:

Ημερομηνία

Προορισμό

Αεροπορική εταιρεία (προαιρετικά)

και εμφανίζονται οι διαθέσιμες πτήσεις.

Screenshot Placeholder

Κράτηση εισιτηρίου
Στην οθόνη μίας πτήσης μπορεί να γίνει κράτηση θέσης και επιβεβαίωση εισιτηρίου.

Screenshot Placeholder

Προβολή κρατήσεων
Ο χρήστης βλέπει όλες τις μελλοντικές κρατήσεις του και μπορεί να δει λεπτομέρειες.

Ακύρωση κράτησης
Ο χρήστης μπορεί να ακυρώσει μία κράτηση, με άμεση ενημέρωση των διαθεσίμων θέσεων.

Αποσύνδεση
Από το μενού μπορεί να γίνει logout.

Ως Διαχειριστής

Ο λογαριασμός του διαχειριστή καθορίζεται μέσα στη βάση ή στο αρχείο αρχικοποίησης.

Σύνδεση admin
Ο διαχειριστής συνδέεται με τα δικά του credentials.

Διαχείριση πτήσεων

Προσθήκη νέας πτήσης

Επεξεργασία υπαρχουσών

Διαγραφή πτήσεων

Screenshot Placeholder

Διαχείριση χρηστών
Ο admin μπορεί να δει χρήστες και κρατήσεις.

Προβολή όλων των κρατήσεων
Πλήρης λίστα όλων των εισιτηρίων που έχουν εκδοθεί.

Αποσύνδεση διαχειριστή

Αναφορές

Κατά την ανάπτυξη χρησιμοποιήθηκαν βασικές τεχνικές MEVN stack, επίσημη τεκμηρίωση των βιβλιοθηκών και παραδείγματα REST API αρχιτεκτονικής.
