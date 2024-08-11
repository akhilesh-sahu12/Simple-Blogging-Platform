# Simple Blogging Platform

## Project Overview
The Simple Blogging Platform is a full-stack web application that allows users to view, create, and comment on blogs. This project is designed to provide hands-on experience in full-stack development, incorporating HTML/CSS, JavaScript, DOM manipulation, server-side programming with Node.js, and databases using PostgreSQL.

## Features
- **Landing Page**: Displays a list of all available blogs.
- **Blog Creation Page**: A form that allows users to create a new blog with a title and content.
- **Blog Detail Page**: Shows the full content of a selected blog and lists comments.
- **Comment Section**: Allows users to post comments on a specific blog.

## Installation and Setup

### Prerequisites
- Node.js and npm
- PostgreSQL

### Step-by-Step Guide

#### 1. Setup 
- Install Node.js and npm from [Node.js official site](https://nodejs.org/).
- Install PostgreSQL from [PostgreSQL official site](https://www.postgresql.org/download/).

#### 2. Database Setup
- Open PostgreSQL and create a new database named `BlogPlatform`.
- Create the necessary tables using the following SQL:

    ```sql
    CREATE TABLE blogs (
      id SERIAL PRIMARY KEY,
      title VARCHAR(255) NOT NULL,
      content TEXT NOT NULL
    );

    CREATE TABLE comments (
      id SERIAL PRIMARY KEY,
      blog_id INTEGER REFERENCES blogs(id),
      content TEXT NOT NULL
    );
    ```

#### 3. Run Web Application
- **Step 1:** Create the database and tables in PostgreSQL using the queries provided in the `SqlFile.txt`.
- **Step 2:** Run the command: `node server.js`.
- **Step 3:** Open `http://localhost:3000/` in your browser.

## Screenshots

![Landing Page](https://github.com/akhilesh-sahu12/Simple-Blogging-Platform/blob/master/Screensorts/1.png)
![Blog Creation Page](https://github.com/akhilesh-sahu12/Simple-Blogging-Platform/blob/master/Screensorts/2.png)
![Blog Detail Page](https://github.com/akhilesh-sahu12/Simple-Blogging-Platform/blob/master/Screensorts/3.png)
![Comment Section](https://github.com/akhilesh-sahu12/Simple-Blogging-Platform/blob/master/Screensorts/4.png)
![Blog List](https://github.com/akhilesh-sahu12/Simple-Blogging-Platform/blob/master/Screensorts/5.png)
![Create Blog Form](https://github.com/akhilesh-sahu12/Simple-Blogging-Platform/blob/master/Screensorts/6.png)
![Comment Submission](https://github.com/akhilesh-sahu12/Simple-Blogging-Platform/blob/master/Screensorts/7.png)