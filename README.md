# MVC with Node.js
This repository is a small playground for learning MVC in Node.js using Typescript, Express, Prisma, and PostgreSQL.

## Project context
The end goal is to have an application that allows borrowers to take books out of a library. There are three tables in the database: borrowers, books, and loans. A loan has one book and one borrower, but a borrower can have many loans. I'm trying to keep the scope of the project down right now. In a real world database, I would have a table for users (standard, admin) where an admin could add, edit, and delete books/loans/borrowers and a standard user could only read the data. I would also break the books into multiple tables for genre, author, etc. However, this project is very simple and I would like to just have books, borrowers, and loans.

## Goals in this project

I would like to learn how MVC works in Node.js. I've never spent a lot of time with MVC and I would really like to understand this architecture because it's commonly used in software everywhere. I also have a fundamental understanding of OOP and would like to take a deeper dive to really understand all of the moving parts.

Please let me know of any design issues or bad practice. This is strictly for my learning and part of learning is being told where you're wrong.

---

### Issues
- GET localhost:3000/books 404 - { "error": "Cannot read properties of undefined (reading 'service')" }
		- I'm told that service is undefined in src/controllers/book.controller.ts and I can't figure out why. In src/routes/book.routes.ts, I'm creating a new BookService by passing client in and creating a new BookController by passing that service in.