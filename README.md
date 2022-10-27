# Back-End Banking Project

## Why this project?

I wanted to do a Banking application to figure out how that could be, because I would like to work for a bank as back-end developer. I used the instructions and best practices that I learnt at CodeClan.

## Technical Review

This is a back-end desktop application built with Maven, written in Java 8 and Spring. The project was initialized with the Spring Boot initializr tool and 4 main dependences were added to it: Spring Web, Spring Data JPA, Spring Boot DevTools and PostGreSQL driver. The application works with a 'banking' database, previously created with the command 'createdb banking' on terminal.

<img width="150" alt="image" src="https://user-images.githubusercontent.com/85517520/196668778-37caaf09-ce49-44be-a343-2a725c05d4d5.png">

This database has got two main tables, 'accounts' and 'customers'. 

<img width="330" alt="image" src="https://user-images.githubusercontent.com/85517520/196669063-e126312e-b08b-433d-b1b0-618dad839f49.png">

The 'accounts' table is @manyToOne relationship and the 'customers' table is @oneToMany relationship. The foreign key in the 'accounts' table is 'customer_id' this behaviour is given by the annotation @JoinColumn.

I used the Insomnia application to connect with the server to comunicate with the database.

<img width="430" alt="Screenshot 2022-10-19 at 12 02 02" src="https://user-images.githubusercontent.com/85517520/196674480-c4785cb0-8813-489b-bcbf-e70a333254f7.png">


## Functionality

The program creates, modifies, deletes and retrieves bank accounts from the 'customers' table, the same way works for the 'accounts' table. These operations are made using the unique and single identifier 'id' of every account, except for creating a new account or new customer.

## Learning points

I learnt how to test our program using Insomnia -this program is very alike to Postman-, making calls to the webserver to try what data returns these calls. I learnt how to make calls with different endpoints, like the use of query strings. I learnt the difference between @RequestParam and @PathVariable, this last one extracts values from the URI path, @RequestParam extracts values from the query string. We can not make use of query string with @PathVariable.

<img width="600" alt="image" src="https://user-images.githubusercontent.com/85517520/196667541-5b282986-584a-4804-aa26-ccf5405bbc39.png">

