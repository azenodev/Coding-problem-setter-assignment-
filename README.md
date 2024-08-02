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
