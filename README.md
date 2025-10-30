import string
import time
import base64
encoded = b'aGVsbG8gd29ybGQgaW0gZ2F5aGFyaq=='
text = base64.b64decode(encoded).decode()
temp = ''
for ch in text:
    for i in string.printable:
        if i == ch or ch == ' ':
            time.sleep(0.02)
            print(temp + i)
            temp += ch
            break
        else:
            time.sleep(0.02)
            print(temp + i)
