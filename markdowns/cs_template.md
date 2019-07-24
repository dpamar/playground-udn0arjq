# C# template

Even if you're not familiar with C#, it should be understandable :)

```csharp
/** HEADERS **/
using System;
using System.Collections.Generic;
class MultiQuine
{
    static void Main(string[] args)
    {
        Dictionary<String, int[]> data = new Dictionary<String, int[]>();
        /** DATA **/
        data.Add("BF", new int[]{/** BF code goes here **/});
        data.Add("CS", new int[]{/** CS code goes here **/});
        data.Add("JS", new int[]{/** JS code goes here **/});
        /** CODE **/
        String language = "CS";
        if (args.Length > 0) language = args[0];
        switch (language)
        {
            case "BF":
                foreach (int i in new int[] {/** BF headers block goes here **/}) Console.Write((char)i);
                foreach (String l in new String[] { "BF", "CS", "JS" })
                {
                    foreach (char c in l) Console.Write(new string('+', (int)c) + ">");
                    Console.Write(">");
                    foreach (int i in data[l]) Console.Write(new string('+', i) + ">");
                    Console.Write(">");
                }
                break;
            case "CS":
                foreach (int i in new int[] {/** CS headers block goes here **/}) Console.Write((char)i);
                foreach (String l in new String[] { "BF", "CS", "JS" })
                    Console.WriteLine("        data.Add(\"" + l + "\", new int[]{" + String.Join(",", data[l]) + "});");
                break;
            case "JS":
                foreach (int i in new int[] {/** JS headers block goes here **/}) Console.Write((char)i);
                foreach (String l in new String[] { "BF", "CS", "JS" })
                    Console.WriteLine(" data['" + l + "']=[" + String.Join(",", data[l]) + "];");
                break;
        }
        foreach (int i in data[language]) Console.Write((char)i);
    }
}
```

_Note_: We already define here that
* JS syntax to add data values will be data[language] = [array of integers]
* and in BF, the language name as an array, encoded using "+" to have the final char, then ">"; followed by 0, array, separator, then all integers (all non null), followed by an array separator as well

We will make sure these syntaxes will be used.

