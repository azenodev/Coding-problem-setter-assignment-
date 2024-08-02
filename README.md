using System;

class Program
{
    static void Main()
    {
        // Input string
        string inputStr = "Ade MOP Boy Girl xyZ IUX";
        
        // Convert the input string to uppercase
        string upperStr = inputStr.ToUpper();
        
        // Initialize an empty string to store the modified characters
        string modifiedStr = string.Empty;
        
        // Iterate through each character in the uppercase string
        foreach (char c in upperStr)
        {
            if (char.IsLetter(c))
            {
                // Add 2 to the ASCII value of the character
                char modifiedChar = (char)(((c - 'A' + 2) % 26) + 'A');
                modifiedStr += modifiedChar;
            }
            else
            {
                // Keep non-alphabetic characters unchanged
                modifiedStr += c;
            }
        }
        
        // Print the input and modified strings
        Console.WriteLine("Input: " + inputStr);
        Console.WriteLine("Output: " + modifiedStr);
    }
}




using System;

class Program
{
    static void Main()
    {
        // Input name
        Console.Write("Enter a name: ");
        string inputName = Console.ReadLine();
        
        // Initialize an empty string to store the modified name
        string modifiedName = string.Empty;
        
        // Iterate through each character in the input name
        foreach (char c in inputName)
        {
            if (char.IsUpper(c))
            {
                // Convert uppercase to lowercase
                modifiedName += char.ToLower(c);
            }
            else if (char.IsLower(c))
            {
                // Convert lowercase to uppercase
                modifiedName += char.ToUpper(c);
            }
            else
            {
                // Keep non-alphabetic characters unchanged
                modifiedName += c;
            }
        }
        
        // Print the original and modified names
        Console.WriteLine("The name: " + inputName);
        Console.WriteLine("New name: " + modifiedName);
    }
}



using System;

class ReplaceVowels
{
    public void Replace(string word)
    {
        // Convert the word to lowercase
        string wordInLower = word.ToLower();

        // Array to hold the new characters
        char[] newWordArray = new char[wordInLower.Length];

        // Iterate through each character in the word
        for (int i = 0; i < wordInLower.Length; i++)
        {
            char currentChar = wordInLower[i];

            // Check if the character is a vowel
            if ("aeiou".IndexOf(currentChar) >= 0)
            {
                // Replace vowel with the next character
                newWordArray[i] = (char)(currentChar + 1);
            }
            else
            {
                // Keep the consonants unchanged
                newWordArray[i] = currentChar;
            }
        }

        // Convert the char array back to a string
        string newWord = new string(newWordArray);

        // Print the result
        Console.WriteLine($"Given word :- {word}");
        Console.WriteLine($"New word :- {newWord}");
    }
}

class Program
{
    static void Main(string[] args)
    {
        // Create an instance of ReplaceVowels
        ReplaceVowels replaceVowels = new ReplaceVowels();
        
        // Input word
        string inputWord = "Computer";
        
        // Call the Replace method with the input word
        replaceVowels.Replace(inputWord);
    }
}
