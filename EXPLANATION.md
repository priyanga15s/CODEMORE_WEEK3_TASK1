# Explanation of Java Concepts Used

## Objective

This program reads data from a text file and demonstrates exception handling by catching `FileNotFoundException` and `IOException`.

---

# 1. File Handling

Java provides classes in the `java.io` package to work with files.

This program uses:

- `FileReader`
- `BufferedReader`

Example:

```java
BufferedReader reader = new BufferedReader(new FileReader(fileName));
```

`FileReader` opens the file, and `BufferedReader` reads it line by line.

---

# 2. Scanner Class

The `Scanner` class is used to read the file name from the user.

```java
Scanner sc = new Scanner(System.in);
```

Method used:

```java
nextLine()
```

---

# 3. Reading a File

The program reads the file one line at a time.

```java
while ((line = reader.readLine()) != null)
```

Each line is displayed using:

```java
System.out.println(line);
```

---

# 4. Exception Handling

The program uses a `try-catch-finally` block.

```java
try {
    ...
}
catch (...) {
    ...
}
finally {
    ...
}
```

This prevents the program from terminating unexpectedly.

---

# 5. FileNotFoundException

This exception occurs if the specified file does not exist.

```java
catch (FileNotFoundException e)
```

Example output:

```
Error: File not found.
```

---

# 6. IOException

This exception occurs if an error happens while reading or closing the file.

```java
catch (IOException e)
```

Example output:

```
Error reading the file.
```

---

# 7. Finally Block

The `finally` block always executes whether an exception occurs or not.

It is used to close resources.

```java
reader.close();
```

---

# 8. Resource Management

The program closes both the file reader and the `Scanner`.

```java
reader.close();
sc.close();
```

This prevents resource leaks.

---

# Program Flow

1. Read the file name from the user.
2. Open the file using `FileReader`.
3. Read the file line by line using `BufferedReader`.
4. Display each line.
5. Catch `FileNotFoundException` if the file does not exist.
6. Catch `IOException` if an error occurs while reading the file.
7. Close the file and the `Scanner`.
8. End the program.

---

# Java Concepts Covered

- File Handling
- FileReader
- BufferedReader
- Scanner Class
- Exception Handling
- try-catch-finally
- FileNotFoundException
- IOException
- Loops
- User Input
- Resource Management
