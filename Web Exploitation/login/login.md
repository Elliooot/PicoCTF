# Login
## Overview
Points: 100    Category: Web Exploitation

## Description
My dog-sitter's brother made this website but I can't get in; can you help?

http://login.mars.picoctf.net

## Hints
(none)

## Solution
1. Press F12, the clue is in `index.js`

![image](https://user-images.githubusercontent.com/91111108/217207923-6442827d-ef40-4ed5-a885-cdc7ca50acbe.png)

  2. There is a btoa() function, seems the Username and Password were turn into Base64 from ASCII.
  3. Use Linux's base64 decode command to decode the flag.
  
    echo "cGljb0NURns1M3J2M3JfNTNydjNyXzUzcnYzcl81M3J2M3JfNTNydjNyfQ" | base64 -d
    
## Flag
`picoCTF{53rv3r_53rv3r_53rv3r_53rv3r_53rv3r}`
