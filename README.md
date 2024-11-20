## code source :
``` ts
from random import randint
from random import *
import os
import platform


def find_passwords_with_part(passwords_file, part):
    try:
        with open(passwords_file, 'r') as pf:
            passwords = pf.read().splitlines()
        
        matching_passwords = [pwd for pwd in passwords if part in pwd]

        if matching_passwords:
            print("\nPassword found!")
            for pwd in matching_passwords:
                print(pwd, "\n")
        else:
            print("\nNo password found with the given party.")
    except FileNotFoundError:
        print(f"Arquivo {passwords_file} não encontrado.")

if __name__ == "__main__":
    passwords_file = 'password.txt' 

    print(" _ __   __ _ ___ ___    _ __  _   _ ")
    print("| '_ \ / _` / __/ __|  | '_ \| | | |")
    print("| |_) | (_| \__ \__ \ _| |_) | |_| |")
    print("| .__/ \__,_|___/___/(_) .__/ \__, |")
    print("|_|                    |_|    |___/ ")
 
    print("version      :  1.0.0");
    print("author       :  whmer - sam");
    print("creator      :  dreqxy")
    print("description  :  download the file and name it password.txt")
    part = input("\n[-] Possible password: "); 
    find_passwords_with_part(passwords_file, part)
```