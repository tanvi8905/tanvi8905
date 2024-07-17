string programs
1.def count_vowels_consonants(string):
    vowels = 0
    consonants = 0
    vowels_list = "aeiouAEIOU"
    
    for char in string:
        if char.isalpha():
            if char in vowels_list:
                vowels += 1
            else:
                consonants += 1
    
    return vowels, consonants

input_string = "Hello World"
v, c = count_vowels_consonants(input_string)
print(f"Vowels: {v}, Consonants: {c}")

2.def reverse_string(string):
    return string[::-1]

input_string = "Hello World"
reversed_string = reverse_string(input_string)
print(f"Reversed string: {reversed_string}")

3.def is_palindrome(string):
    return string == string[::-1]

input_string = "madam"
if is_palindrome(input_string):
    print(f"{input_string} is a palindrome")
else:
    print(f"{input_string} is not a palindrome")

4.def remove_duplicates(string):
    unique_chars = []
    for char in string:
        if char not in unique_chars:
            unique_chars.append(char)
    return ''.join(unique_chars)

input_string = "hello"
result = remove_duplicates(input_string)
print(f"String after removing duplicates: {result}")

5.from collections import Counter

def are_anagrams(str1, str2):
    return Counter(str1) == Counter(str2)

word1 = "listen"
word2 = "silent"
if are_anagrams(word1, word2):
    print(f"{word1} and {word2} are anagrams")
else:
    print(f"{word1} and {word2} are not anagrams")
