database create --> CREATE DATABASE student_db;

table create --> 
CREATE TABLE students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100),
    course VARCHAR(50)
);


without --> FETCH_ASSOC 
[
  0 => 1,
  "id" => 1,
  1 => "Aditi",
  "name" => "Aditi"
]

echo $row[1];  // works, but unclear
echo $row["name"]; // also works

with --> FETCH_ASSOC 
[
  "id" => 1,
  "name" => "Aditi",
  "email" => "aditi@example.com"
]

echo $row["name"]; // Aditi


CREATE TABLE all_data (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL,
    age INT,
    gender VARCHAR(10),
    hobbies TEXT,
    course VARCHAR(50),
    dob DATE,
    address TEXT,
    profile_pic VARCHAR(255),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);


task :- 
-- prevent duplicate emails in the students table.