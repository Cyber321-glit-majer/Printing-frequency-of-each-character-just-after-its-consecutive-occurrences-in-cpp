# Printing-frequency-of-each-character-just-after-its-consecutive-occurrences-in-cpp
c++

**PROBLEM STATEMENT**
Given a string in such a way that every character occurs in a repeated manner. Your task is to print the string by inserting the frequency of each unique character after it and also eliminating all repeated characters.

**INPUT**
aaabbbbbcccaaa

**OUTPUT**
a3b5c3a3

**code**

```

#include <iostream>
using namespace std;

void printRLE(string s)
{
	for (int i = 0; s[i] != '\0'; i++) {

		int count = 1;
		while (s[i] == s[i + 1]) {
			i++;
			count++;
		}
		cout << s[i] << count << " ";
	}

	cout << endl;
}


int main()
{
	string s;
	 cin>>s;
	  printRLE(s);
	return 0;
}

