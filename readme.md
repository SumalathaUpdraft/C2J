# MF File Sorter

MF File Sorter is a Java application that organizes files based on their content. It scans a specified directory, identifies the type of each file, and moves them to corresponding directories.


## Features

- Sorts files into different directories based on their content type, such as COBOL, Java, BMS, JSON, JCL, Copy Book, Cards, SQL, and Garbage.
- Creates a new directory named "sorted" in the specified directory to store the sorted files.
- Provides logging using the SLF4J and Logback libraries.


## File Sorting Rules

The MF File Sorter categorizes files into different directories based on the following rules:

- **COBOL Files**: Files containing the keyword "IDENTIFICATION DIVISION" are classified as COBOL files. They are moved to the "cob" directory.
- **Java Files**: Files containing the keywords "class", "import", and "package" are classified as Java files. They are moved to the "java" directory.
- **BMS Files**: Files containing the keywords "DFHMSD", "LENGTH", "POS", and "DFHMDF" are classified as BMS files. They are moved to the "bms" directory.
- **JSON Files**: Files containing the characters "{", "}", "[", and "]" are classified as JSON files. They are moved to the "json" directory.
- **JCL Files**: Files starting with the "//" comment indicator are classified as JCL files. Depending on the content, they are further categorized as "jcl/job" or "jcl/proc" files and moved accordingly.
- **Copy Book Files**: Files containing the keywords "INPLNA.COBOL", "INPLNA.COBOL.COPYLIB", "DCLGEN TABLE", or "PIC X" are classified as Copy Book files. They are moved to the "lib" directory.
- **Cards Files**: Files with exactly three lines starting with a space or the characters "DSN" are classified as Cards files. They are moved to the "cards" directory.
- **SQL Files**: Files containing keywords such as "SELECT", "INSERT", "CREATE TABLE", or "SET CURRENT" are classified as SQL files. They are moved to the "sql" directory.
- **Garbage Files**: Files that do not match any of the above rules are classified as Garbage files. They are moved to the "garbage" directory.


## Usage

1. Clone or download the project.
2. Open the project in your preferred Java IDE.
3. Modify the `Test.java` file to specify the directory path you want to sort.
4. Build the project to generate the executable JAR file.
5. Run the JAR file, and the files in the specified directory will be sorted into the "sorted" directory.


## Configuration

The logging configuration is specified in the `logback.xml` file. You can customize the logging format and destination by modifying this file.



