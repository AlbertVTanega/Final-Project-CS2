✅ 1. REVISED & IMPROVED PROJECT PROPOSAL (Final Draft)
📌 Project Title
Library Borrowing Record System
🔍 Problem Statement
Many school libraries still record book borrowings manually using paper logs. This process makes it difficult to track who borrowed which books, when they borrowed them, and whether the books were returned. As a result, librarians experience confusion, delays, missing records, and difficulty identifying overdue books.
This project solves the problem by developing a digital library borrowing system using Python and JSON data. The dataset will store student borrowers, their borrower IDs, and details about the books they borrowed (title, author, borrow date, return date). The system will allow efficient tracking and monitoring of library borrowing transactions.
🎯 Project Objectives
To analyze and summarize data from a library borrowing JSON dataset.
To help librarians monitor borrowed and returned books easily.
To apply JSON handling and Python programming concepts to solve a real-world problem.
To identify overdue books automatically using date calculations.
To improve library management by providing quick search and listing features.
⚙️ Planned Features
Feature 1 – Display all borrowers and their borrowed books
Shows student name, borrower ID, and the list of books they borrowed.
Feature 2 – Show all unreturned books
Filters entries where return_date = null or empty.
Feature 3 – Count total books borrowed per student
Displays:
Student Name – Total Books Borrowed
Feature 4 – Display overdue books
Compares today’s date with borrow_date + allowed days (ex: 7 days).
Feature 5 – Search for a book or a student
Input may be:
Book title
Student name
Borrower ID
Shows matching records.
⌨️ Planned Inputs and Outputs
Inputs
Borrower ID
Student name
Book title
Date (system will use Python’s datetime)
Outputs
List of borrowed books per student
List of unreturned books
List of overdue book
Total books borrowed per student
Search results
✅ 2. COMPLETE PSEUDOCODE 
📘 Pseudocode for Library Borrowing Record System
START PROGRAM

Load JSON file containing library borrowers and their books

REPEAT
    Display menu:
        1. Show all borrowers and their borrowed books
        2. Show all unreturned books
        3. Count total books borrowed per student
        4. Show overdue books
        5. Search for a borrower or book
        6. Exit program

    Ask user to enter a choice

    IF choice == 1 THEN
        For each borrower in JSON:
            Display borrower name, ID, and their books

    ELSE IF choice == 2 THEN
        For each borrower:
            For each book borrowed:
                IF return_date is empty THEN
                    Display book as "Unreturned"

    ELSE IF choice == 3 THEN
        For each borrower:
            Count number of books in their “borrowed_books” list
            Display borrower name and total

    ELSE IF choice == 4 THEN
        For each borrower:
            For each book:
                Convert borrow_date to date format
                Compute due_date = borrow_date + 7 days
                IF return_date is empty AND today > due_date THEN
                    Display book as "Overdue"

    ELSE IF choice == 5 THEN
        Ask user: "Search by book title or student name?"
        Get search input
        Search JSON for matching book title OR student name
        Display results OR "No results found"

    ELSE IF choice == 6 THEN
        Display "Exiting program..."
        BREAK LOOP

    ELSE
        Display "Invalid choice. Try again."

END REPEAT

END PROGRAM

<img width="200" height="500" alt="image" src="https://github.com/user-attachments/assets/9915bd99-2a04-4015-88d6-54146032866a" />
