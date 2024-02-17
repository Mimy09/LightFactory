
## Identifier Names
Learn more here: https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/identifier-names

 - <b>Interface</b> names start with a capital I.
 - <b>Attribute</b> types end with the word Attribute.
 - <b>Enum</b> types use a singular noun for nonflags, and a plural noun for flags.
 - <b>Identifiers</b> shouldn't contain two consecutive underscore (_) characters. <i>Those names are reserved for compiler-generated identifiers</i>.
 - Use meaningful and descriptive names for <b>variables</b>, <b>methods</b>, and <b>classes</b>.
 - Prefer clarity over brevity.
 - Use <b>PascalCase</b> for <b>class names</b> and <b>method names</b>.
 - Use <b>camelCase</b> for <b>method arguments</b>, <b>local variables</b>, and <b>private fields</b>.
 - Use <b>PascalCase</b> for <b>constant names</b>, <b>both fields</b> and <b>local constants</b>.
 - <b>Private instance</b> fields start with an <b>underscore</b> (_).
 - <b>Static fields</b> start with <b>s_</b>. <i>This convention isn't the default Visual Studio behavior, nor part of the Framework design guidelines, but is configurable in editorconfig.</i>
 - <b>Avoid using abbreviations</b> or acronyms in names, except for widely known and accepted abbreviations.
 - Use meaningful and descriptive namespaces that follow the reverse domain name notation.
 - Choose assembly names that represent the primary purpose of the assembly.
 - <b>Avoid using single-letter names</b>, except for simple loop counters. Also, syntax examples that describe the syntax of C# constructs often use the following single-letter names that match the convention used in the C# language specification. Syntax examples are an exception to the rule.
    - Use S for structs, C for classes.
    - Use M for methods.
    - Use v for variables, p for parameters.
    - Use r for ref parameters.

## Unity Coding Conventions
Learn more here: https://unity.com/how-to/naming-and-code-style-tips-c-scripting-unity

### Default Methods
 - Default methods like ```start``` and ```update``` should be ```protected``` to avoid unnecessary C# warnings
```C#
protected void Start()
{
    // Code...
}
```

## C# Coding Conventions
Learn more here: https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions

### String Data
- Use string interpolation to concatenate short strings, as shown in the following code.
```C#
string displayName = $"{nameList[n].LastName}, {nameList[n].FirstName}";
```
- To append strings in loops, especially when you're working with large amounts of text, use a System.Text.StringBuilder object.
```C#
var phrase = "lalalalalalalalalalalalalalalalalalalalalalalalalalalalalala";
var manyPhrases = new StringBuilder();
for (var i = 0; i < 10000; i++)
{
    manyPhrases.Append(phrase);
}
//Console.WriteLine("tra" + manyPhrases);
```

### Arrays
 - Use the concise syntax when you initialize arrays on the declaration line. In the following example, you can't use ```var``` instead of ```string[]```.
```C#
string[] vowels1 = { "a", "e", "i", "o", "u" };
```
 - If you use explicit instantiation, you can use ```var```.
```C#
var vowels2 = new string[] { "a", "e", "i", "o", "u" };
```

### Delegates

