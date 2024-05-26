is vowel check:

      bool isVowel(char ch) {
          // Define vowels in both uppercase and lowercase
          string vowels = "aoyeuiAOYEUI";
          return vowels.find(ch) != string::npos;
      }
      
- The if(!vowels.find(ch)) condition is incorrect because std::string::find returns the position of the first occurrence of the character, or std::string::npos if the character is not found. Instead, we should check if the result is not std::string::npos.
- 
inputL=:

      getline(cin, input);  // Read the input string

