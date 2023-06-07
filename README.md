# PythonTask
1.def flat(lis):
	flatList = []
	
	for element in lis:
		if type(element) is list:
			
			for item in element:
				flatList.append(item)
		else:
			flatList.append(element)
	return flatList


lis = [1,2,3,4, [44,55,66, True], False, (34,56,78,89,34), {1,2,3,3,2,1}, {1:34, "key2": [55, 67, 78, 89], 4: (45,
22, 61, 34)}, [56, 'data science'], 'Machine Learning']
print('List', lis)
print('Flat List', flat(lis))


2. def encrypt_message(message):
    encrypted_message = ""
    for char in message:
        if char.isalpha():
            char = char.lower()
            encrypted_char = chr(ord('z') - (ord(char) - ord('a')))
        elif char.isspace():
            encrypted_char = '$'
        else:
            encrypted_char = char
        encrypted_message += encrypted_char
    return encrypted_message.lower()

message = input("I want to become a Data Scientist: ")
encrypted_message = encrypt_message(message)
print("Encrypted message:", encrypted_message)
