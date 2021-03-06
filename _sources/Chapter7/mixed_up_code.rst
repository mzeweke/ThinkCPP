Mixed Up Code Practice
----------------------

.. parsonsprob:: mucp_7_1
   :numbered: left
   :adaptive:
   :noindent:
   :practice: T

   Write a program that prints the 4th character of ``string``, 
   and finds and replaces all instances of 'i' with 'e'.
   Finally, print out the string. Put the necessary blocks in the correct order.
   -----
   int main() {
   =====
      string word = "irritating";
   =====
      cout << word[3] << endl;
   =====
      cout << irritating[3] << endl;  #distractor
   =====
      cout << word.at(4) << endl;  #distractor
   =====
      cout << word[4] << endl;  #distractor
   =====
      while ((int)word.find('i') != -1) {
   =====
      while ((int)word.find('e') != -1) {  #distractor
   =====
      while ((int)word.find('i')) {  #distractor
   =====
         word[word.find('i')] = 'e';
      }
   =====
         word[word.find('e')] = 'i';  #distractor
      }
   =====
      cout << word << endl;
   =====
   }

.. parsonsprob:: mucp_7_2
   :numbered: left
   :adaptive:
   :noindent:
   :practice: T

   An anagram is a play on words by rearranging the letters of the original words
   to form new words. For example, the letters in "listen" can be rearranged to
   make "silent". Write a program that rearranges "night" into "thing" and prints the anagram.
   Put the necessary blocks in the correct order.
   -----
   int main() {
   =====
      string original = "night";
   =====
      string original = "thing";  #paired
   =====
      string anagram = original;
   =====
      anagram[0] = original[original.find('t')];
   =====
      anagram[1] = original[original.find('h')];
   =====
      anagram[2] = original[original.find('i')];
   =====
      anagram[3] = original[original.find('n')];
   =====
      anagram[4] = original[original.find('g')];
   =====
      cout << anagram;
   =====
   }

.. parsonsprob:: mucp_7_3
   :numbered: left
   :adaptive:
   :noindent:
   :practice: T

   Let's write the function ``longerString``, which takes two ``strings``
   as parameters, ``first`` and ``second``. If ``first`` has more letters
   than ``second``, ``longerString`` prints "``first`` is longer than ``second``",
   and vice versa. If they have the same number of letters, ``longerString`` 
   prints "``first`` and ``second`` are the same length".
   Put the necessary blocks in the correct order.
   -----
   void longerString (string first, string second) {
   =====
   string longerString (string first, string second) {  #paired
   =====
      if (first.length() > second.length()) {
   =====
      if (first.length() >= second.length()) {  #paired
   =====
         cout << first << " is longer than " << second << endl;
      }
   =====
      else if (first.length() < second.length()) {
   =====
         cout << second << " is longer than " << first << endl;
      }
   =====
         cout << second << " is longer than " << second << endl;  #paired
      }
   =====
      else {
   =====
      else (first.length() == second.length()) {  #distractor
   =====
         cout << first << " and " << second << " are the same length" << endl;
      }
   =====
   }

.. parsonsprob:: mucp_7_4
   :numbered: left
   :adaptive:
   :practice: T

   Let's write the code for the ``cipherText`` function. ``cipherText`` 
   should be a void function that takes a string input as a parameter,
   increases the value of each character by 1 (i.e. "bad" turns into "cbe"),
   and outputs the encrypted string.
   -----
   void cipherText (string input) {
   =====
   string cipherText (string input) {  #paired
   =====
      int i = 0;
   =====
      while (i < input.length()) {
   =====
      while (i < input.length() - 1) {  #paired
   =====
         input[i] = input[i] + 1;
   =====
         input[i] = input[i] - 1;  #paired
   =====
         i++;
      }
   =====
      cout << input;
   }
   =====
      return input;  #paired
   }

.. parsonsprob:: mucp_7_5
   :numbered: left
   :adaptive:
   :practice: T

   The program below should print out the number of occurences of the character 't'
   in the string tongue_twister but the code is mixed up. Put the necessary blocks 
   in the correct order, with declaration in the order of tongue_twister, count, and i.
   -----
   int main() {
   =====
      string tongue_twister = "twelve twins twirled twelve twigs";
   =====
      int count = 0;
   =====
      int count = 1;  #paired
   =====
      int i = 0;
   =====
      while (i < (int)tongue_twister.length()) {
   =====
         if (tongue_twister[i] == 't') {
   =====
         if (tongue_twister[i] = 't') {  #paired
   =====
            count++;
         }
   =====
         i++;
      }
   =====
      cout << count;
   }

.. parsonsprob:: mucp_7_6
   :numbered: left
   :adaptive:
   :practice: T

   The program below should print out the index of the second instance of the 
   character 'i' but the code is mixed up and contains extra blocks. 
   Put the necessary blocks in the correct order.
   -----
   int main() {
   =====
      string quote = "Your time is limited, so don't waste it living someone else's life.";
   =====
      int i = 0;  #distractor
   =====
      while (i < quote.length()) {  #distractor
   =====
      int first = quote.find("i");
   =====
      int index = find (quote, 'i', first + 1);
   =====
      int index = find (quote, 'i', first);  #paired
   =====
      cout << index;
   }
   =====
      cout << first;  #paired
   }

.. parsonsprob:: mucp_7_7
   :numbered: left
   :adaptive:
   :practice: T

   Deep in the forest live the 7 dwarves named Sorty, Torty, Vorty,
   Worty, Xorty, Yorty, and Zorty. The program below should print 
   out each of their names but the code is mixed up and contains extra blocks. 
   Put the necessary blocks in the correct order.
   -----
   int main() {
   =====
      string name = “Sorty”; #distractor
   =====
      string suffix = "orty";
   =====
      char letter = 'S';
   =====
      while (letter <= 'Z') {
   =====
         if (letter != 'U') {
   =====
         if (letter == 'U') {  #paired
   =====
         cout << letter + suffix << endl;
         }
   =====
         letter++;
      }
   }
   =====
         suffix++;  #paired
      }
   }

.. parsonsprob:: mucp_7_8
   :numbered: left
   :adaptive:
   :practice: T

   On the strange planet of Noes, there's a law that prohibits the usage of the letter "e". 
   As a result, they hired you to write a function called ``censorE`` that replaces all occurences
   of the letter "e" in a string with an asterisk and returns the censored string. For example, 
   if the input is "hello world", the function returns "h*llo world".
   -----
   string censorE (string input) {
   =====
   void censorE (string input) {  #paired
   =====
      string copy = input;  #distractor
   =====
      int i = 0;
   =====
      while (i < input.length()) {
   =====
      while (i < input.length() - 1) {  #paired
   =====
         if (input[i] == 'e') {
   =====
         if (input[i] = 'e') {  #paired
   =====
            input[i] = '*';
         }
   =====
            '*' = input[i];  #paired
         }
   =====
         i++;
      }
   =====
      return input;
   }

.. parsonsprob:: mucp_7_9
   :numbered: left
   :adaptive:

   Your work for the planet of Noes impressed the nearby planets of Noas, Nois, Noos, and Nous.
   They want you to write different functions that censor out each planet's corresponding forbidden letter.
   However, your galaxy brain knows better than to write a different function for each planet.
   Using generalization, write the function ``censorLetter`` which takes a string input and a char to censor 
   as parameters and returns a censored string. For example, censorLetter("Bye world", 'o') returns the
   string "Bye w*rld".
   -----
   string censorLetter (string input, char letter) {
   =====
   string censorLetter (string input) {  #paired
   =====
      int i = 0;
   =====
      int i = 1;  #paired
   =====
      while (i < input.length()) {
   =====
         if (input[i] == letter) {
   =====
         if (input[i] == "letter") {  #paired
   =====
            input[i] = '*';
         }
   =====
            '*' = input[i];  #paired
         }
   =====
         i++;
      }
   =====
      return input;
   }

.. parsonsprob:: mucp_7_10
   :numbered: left
   :adaptive:

   Let's write a function called ``alphabetizer`` which takes
   three ``string``\s, ``first``, ``second``, and ``third``,
   and returns a ``string`` which alphabetizes
   the words and separates them with spaces. For example,
   ``alphabetizer ("just", "do", "it")`` returns the ``string``
   "do it just". Put the necessary blocks in the correct order.
   Use the ``compare`` function from the ``<string>`` library.
   -----
   string alphabetizer (string first, string second, string third) {
   =====
   void alphabetizer (string first, string second, string third) {  #paired
   =====
      if (first.compare(second) < 0) {
   =====
         if (third.compare(first) < 0) {
   =====
            return third + " " + first + " " + second;
         }
   =====
         else if (third.compare(second) < 0) {
   =====
            return first + " " + third + " " + second;
         }
   =====
         else {
   =====
            return first + " " + second + " " + third;
         }
      }
   =====
      else {
   =====
         if (third.compare(second) < 0) {
   =====
            return third + " " + second + " " + first;
         }
   =====
         else if (third.compare(first) < 0) {
   =====
            return second + " " + third + " " + first;
         }
   =====
         else {
   =====
            return second + " " + first + " " + third;
         }
      }
   }