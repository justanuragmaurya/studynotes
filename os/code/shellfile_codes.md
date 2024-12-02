# OS Lab Practical Solutions

## Exercise 1: Basic Directory and File Operations
1. **Create a new directory named `project` in your home directory.**
    ```bash
    mkdir ~/project
    ```

2. **Inside the `project` directory, create two subdirectories: `src` and `bin`.**
    ```bash
    mkdir ~/project/src ~/project/bin
    ```

3. **Create a new file named `main.cpp` inside the `src` directory and a file named `compile.sh` inside the `bin` directory.**
    ```bash
    touch ~/project/src/main.cpp ~/project/bin/compile.sh
    ```

4. **Copy `compile.sh` to the `src` directory and rename the copy to `build.sh`.**
    ```bash
    cp ~/project/bin/compile.sh ~/project/src/build.sh
    ```

5. **Move `main.cpp` from the `src` directory to the `bin` directory.**
    ```bash
    mv ~/project/src/main.cpp ~/project/bin/
    ```

6. **Remove the `src` directory.**
    ```bash
    rm -r ~/project/src
    ```

---

## Exercise 2: File Operations
1. **Create a file named `data.txt` with some sample content.**
    ```bash
    echo "Sample content" > ~/data.txt
    ```

2. **Create another file named `backup.txt` by copying `data.txt`.**
    ```bash
    cp ~/data.txt ~/backup.txt
    ```

3. **Use `head` and `tail` commands to display the 11th to 20th lines of `data.txt`.**
    ```bash
    head -n 20 ~/data.txt | tail -n 10
    ```

4. **Rename `backup.txt` to `data-backup.txt`.**
    ```bash
    mv ~/backup.txt ~/data-backup.txt
    ```

5. **Change the permissions of `data.txt` to be read and writable only by the owner.**
    ```bash
    chmod 600 ~/data.txt
    ```

6. **Change the ownership of `data-backup.txt` to a user named `student` and group `group1`.**
    ```bash
    sudo chown student:group1 ~/data-backup.txt
    ```

---

## Exercise 3: Symbolic and Hard Links
1. **Create a file named `original_file.txt` and add some content to it.**
    ```bash
    echo "This is the original file." > ~/original_file.txt
    ```

2. **Create a symbolic link named `symlink_to_original`.**
    ```bash
    ln -s ~/original_file.txt ~/symlink_to_original
    ```

3. **Create a hard link named `hardlink_to_original`.**
    ```bash
    ln ~/original_file.txt ~/hardlink_to_original
    ```

4. **Display inode numbers of all three files.**
    ```bash
    ls -li ~/original_file.txt ~/symlink_to_original ~/hardlink_to_original
    ```

---

## Exercise 4: Grep Practice
1. **Create a directory `grep-practice` with a file `sample.txt` containing at least 50 lines.**
    ```bash
    mkdir ~/grep-practice
    for i in {1..50}; do echo "This is line $i. Linux is awesome." >> ~/grep-practice/sample.txt; done
    ```

2. **Find all lines containing the word `Linux`.**
    ```bash
    grep "Linux" ~/grep-practice/sample.txt
    ```

3. **Find lines case-insensitively containing the word `linux`.**
    ```bash
    grep -i "linux" ~/grep-practice/sample.txt
    ```

4. **Display the line numbers containing the word `Linux`.**
    ```bash
    grep -n "Linux" ~/grep-practice/sample.txt
    ```

---

## Exercise 5: File Permissions
1. **Create a file `permissions_file.txt` in your home directory.**
    ```bash
    touch ~/permissions_file.txt
    ```

2. **Change the file permissions to be readable, writable, and executable by the owner, but readable only by others.**
    ```bash
    chmod 744 ~/permissions_file.txt
    ```

3. **Change the ownership of `permissions_file.txt` to a user `newuser` and group `newgroup`.**
    ```bash
    sudo chown newuser:newgroup ~/permissions_file.txt
    ```

---

## Shell Scripting Exercises
1. **Factorial of a number using a `for` loop:**
    ```bash
    #!/bin/bash
    read -p "Enter a number: " num
    fact=1
    for ((i=1; i<=num; i++)); do
      fact=$((fact * i))
    done
    echo "Factorial of $num is $fact"
    ```

2. **Multiplication table for a number:**
    ```bash
    #!/bin/bash
    read -p "Enter a number: " num
    for i in {1..10}; do
      echo "$num * $i = $((num * i))"
    done
    ```

3. **Reverse a number using a `while` loop:**
    ```bash
    #!/bin/bash
    read -p "Enter a number: " num
    rev=0
    while [ $num -gt 0 ]; do
      digit=$((num % 10))
      rev=$((rev * 10 + digit))
      num=$((num / 10))
    done
    echo "Reversed number is $rev"
    ```
