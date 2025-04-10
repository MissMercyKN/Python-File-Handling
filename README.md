# Python-File-Handling
week4 Python Assignment

File Read & Write Challenge 🖋️: Create a program that reads a file and writes a modified version to a new file.
Error Handling Lab 🧪: Ask the user for a filename and handle errors if it doesn’t exist or can’t be read.
def main():
    # Step 1: Asking the user for a filename
    
    filename = input("Enter the name of the file to read: ")

    try:
        # Step 2: Try to open the file and read its content
        
        with open(filename, 'r') as file:
            content = file.read()

        # Step 3: Modify the content (make all text uppercase)
        modified_content = content.upper()

        # Step 4: Write the modified content to a new file
        new_filename = "modified_" + filename
        with open(new_filename, 'w') as new_file:
            new_file.write(modified_content)

        # Step 5: Let the user know it worked
        print(f"Success! Modified content saved in '{new_filename}'.")

    # Step 6: Error handling if file doesn't exist
    
    except FileNotFoundError:
        print("Oops! That file doesn't exist.")
    
    # Step 7: Handle other reading/writing issues
    
    except IOError:
        print("Sorry, something went wrong while reading or writing the file.")



