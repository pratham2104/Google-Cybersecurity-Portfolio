# Algorithm for File Updates in Python
*Cybersecurity Portfolio Activity*

---

## Project Description

As a security professional at a health care company, I was tasked with maintaining an allow list of IP addresses that controls which employees can access restricted patient records. Employees who no longer need access must be removed from this list on a regular basis. I developed a Python algorithm that opens the allow list file, reads its contents, removes any IP addresses found on a separate remove list, and then rewrites the updated list back to the file. This process helps ensure that only authorized personnel can access sensitive patient information at any given time. The algorithm uses Python file handling, string methods, list operations, and iteration to accomplish this task efficiently.

---

## Open the File That Contains the Allow List

To open the file I used a `with` statement combined with the `open()` function. The `import_file` variable stores the name of the file as a string. The `open()` function takes two arguments: the file name and the parameter `"r"` which tells Python to open the file in read mode. The `with` keyword manages the file automatically, meaning Python closes the file once the indented block finishes running, even if an error occurs. The file object is stored in the variable `file` using the `as` keyword.

```python
import_file = "allow_list.txt"

with open(import_file, "r") as file:
    ip_addresses = file.read()
```

---

## Read the File Contents

Inside the `with` statement I used the `.read()` method on the file object to read the entire contents of the file and convert it into one string. That string was then stored in the variable `ip_addresses`. At this point `ip_addresses` holds all the IP addresses from the file as a single long string with spaces between each address.

```python
with open(import_file, "r") as file:
    ip_addresses = file.read()

print(ip_addresses)
```

---

## Convert the String into a List

In order to remove individual IP addresses from the allow list, the data needed to be in list format rather than one big string. I used the `.split()` method on `ip_addresses` to accomplish this. When called with no arguments, `.split()` breaks the string apart at every whitespace character and returns a list where each IP address is its own individual element. The result is reassigned back to `ip_addresses` so the variable now holds a list instead of a string.

```python
ip_addresses = ip_addresses.split()

print(ip_addresses)
```

---

## Iterate Through the Remove List

To check each IP address against the remove list I built a `for` loop. The `for` keyword starts the loop, `element` is the loop variable that holds one IP address per iteration, and `in ip_addresses` tells Python to go through every item in the `ip_addresses` list one at a time. On each pass through the loop, `element` takes the value of the next IP address in the list.

```python
for element in ip_addresses:
    print(element)
```

---

## Remove IP Addresses That Are on the Remove List

Inside the `for` loop I added a conditional statement using the `if` keyword. The condition checks whether the current `element` is found inside the `remove_list` using the `in` operator. If the condition is `True`, the `.remove()` method is applied to `ip_addresses` to remove that specific IP address from the list. Applying the `.remove()` method in this way is possible because there are no duplicate IP addresses in the `ip_addresses` list, so `.remove()` will always find and delete exactly one match without accidentally removing the wrong entry.

```python
for element in ip_addresses:
    if element in remove_list:
        ip_addresses.remove(element)
```

---

## Update the File with the Revised List of IP Addresses

After removing the unwanted IP addresses from the list I needed to write the updated list back to the file. Since `.write()` only works with strings and not lists I first used the `.join()` method to convert `ip_addresses` back into a string. I applied `.join()` to the string `"\n"` so that each IP address would be separated by a new line in the file, making it easier to read. Then I opened the file again using a `with` statement with the parameter `"w"` for write mode, which clears the existing file contents and replaces them with the new string using the `.write()` method.

```python
ip_addresses = "\n".join(ip_addresses)

with open(import_file, "w") as file:
    file.write(ip_addresses)
```

---

## Complete Algorithms

The two sections below show the full working code for both labs completed in this activity. Each algorithm is presented in its entirety so the complete logic and structure is visible in one place.

### Algorithm 1: Write and Read an Allow List File (Lab 1 - Task 7)

This algorithm assigns a string of IP addresses, writes them to a text file using the `open()` function with the `"w"` parameter, and then reads the file back using the `"r"` parameter storing the contents in a variable called `text`. Two fixes were applied: `open(import_file, "r")` is used instead of `open(ip_addresses, "r")` so the filename is passed correctly, and `file.read()` is called with no arguments instead of `file.read(ip_addresses)` since `.read()` does not accept a string argument.

```python
# Assign import_file to the name of the text file to create
import_file = "allow_list.txt"

# Assign ip_addresses to a string of allowed IP addresses
ip_addresses = "192.168.218.160 192.168.97.225 192.168.145.158 192.168.108.13 192.168.60.153 192.168.96.200 192.168.247.153 192.168.3.252 192.168.116.187 192.168.15.110 192.168.39.246"

# Open the file in write mode and write the IP addresses to it
with open(import_file, "w") as file:
    file.write(ip_addresses)

# Open the file in read mode and store the contents in text
with open(import_file, "r") as file:
    text = file.read()

# Display the contents of text
print(text)
```

### Algorithm 2: Update Allow List Using a Reusable Function (Lab 2 - Task 10)

This algorithm defines a reusable function called `update_file()` that takes a filename and a remove list as parameters. Inside the function it reads the file, splits the contents into a list, removes any IP addresses found in the remove list, joins the list back into a string, and rewrites the file. The function is then called with the allow list file and a new set of IP addresses to remove. After the function runs a `with` statement reads and displays the updated file to verify the changes.

```python
# Define update_file() to take import_file and remove_list as parameters
def update_file(import_file, remove_list):

    # Open the file in read mode and store contents in ip_addresses
    with open(import_file, "r") as file:
        ip_addresses = file.read()

    # Convert ip_addresses from a string to a list
    ip_addresses = ip_addresses.split()

    # Loop through ip_addresses and remove any element found in remove_list
    for element in ip_addresses:
        if element in remove_list:
            ip_addresses.remove(element)

    # Convert ip_addresses back to a string
    ip_addresses = " ".join(ip_addresses)

    # Open the file in write mode and rewrite with updated ip_addresses
    with open(import_file, "w") as file:
        file.write(ip_addresses)

# Call update_file() with the allow list and the IPs to remove
update_file("allow_list.txt", ["192.168.25.60", "192.168.140.81", "192.168.203.198"])

# Open the updated file in read mode and store contents in text
with open("allow_list.txt", "r") as file:
    text = file.read()

# Display the contents of text
print(text)
```

---

## Summary

In this project I built a Python algorithm to automate the process of updating an IP address allow list for a health care company. The algorithm starts by opening the allow list file using a `with` statement and the `open()` function with the `"r"` parameter, then reads its contents into a string using the `.read()` method. The `.split()` method converts that string into a list so individual IP addresses can be accessed and removed. A `for` loop iterates through the list, and an `if` statement inside the loop checks whether each IP address appears in the remove list. If it does, the `.remove()` method deletes it from the allow list. Finally the `.join()` method converts the updated list back into a string, and a second `with` statement using the `"w"` parameter rewrites the file with the cleaned list. This algorithm fully automates a task that would otherwise need to be done manually and reduces the risk of human error when managing access to sensitive patient information.
