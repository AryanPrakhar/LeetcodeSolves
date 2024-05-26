1. Mutlisets
  - Time- O(nlogn)
  - Space- O(2n)=O(n)

          class Solution {
          public:
              bool isAnagram(string s, string t) {
                  //O(1)       
                  multiset<char> word1;
                  multiset<char> word2;
          
          //O(nlogn)
                  for (char c: s){
                      word1.insert(c);
                  }
          //O(nlogn)
                  for (char d:t){
                      word2.insert(d);
                  }
          //O(n)
                  if (word1==word2){
                      return true;
                  }
                  else{
                      return false;
                  }
          
              }
          };

2. Arrays
   - Time- O(n)
   - Space- O(1)
  
               class Solution {
          public:
              bool isAnagram(string s, string t) {
                  // If the lengths of the strings are not equal, they cannot be anagrams
                  if (s.length() != t.length()) {
                      return false;
                  }
          
                  // Create a count array to store the frequency of each character
                  int count[26] = {0};
          
                  // Traverse both strings simultaneously
                  for (int i = 0; i < s.length(); ++i) {
                      count[s[i] - 'a']++;
                      count[t[i] - 'a']--;
                  }
          
                  // Check if all counts are zero
                  for (int i = 0; i < 26; ++i) {
                      if (count[i] != 0) {
                          return false;
                      }
                  }
          
                  return true;
              }
          };
