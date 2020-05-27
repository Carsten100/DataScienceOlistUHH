# Brazilian E-Commerce Public Dataset by Olist
![lul](https://i0.wp.com/alitech.com.ng/wp-content/uploads/2019/12/Screenshot_20191209-104115.png?fit=720%2C639&ssl=1)]

Link zum Datenset:
https://www.kaggle.com/olistbr/brazilian-ecommerce

### Cosumter Lifetime Value ermitteln
Customer Lifetime Value ermitteln
*	Verkaufte Produkte
*	Aktivität des Kunden
*	Bestellungen des Kunden 
*	Wie oft hat der Kunde etwas gekauft
*	In welcher Zeiteinheit hat der Kunde die Produkte gekauft?
*	Umsatz
*	RFM-Matrix (Recency, Frequency) 


Unlike most parser-building frameworks, you use Sprache directly from your program code, and don't need to set up any build-time code generation tasks. Sprache itself is a single tiny assembly.

A simple parser might parse a sequence of characters:

```csharp
// Parse any number of capital 'A's in a row
var parseA = Parse.Char('A').AtLeastOnce();
```

Sprache provides a number of built-in functions that can make bigger parsers from smaller ones, often callable via Linq query comprehensions:

```csharp
Parser<string> identifier =
    from leading in Parse.WhiteSpace.Many()
    from first in Parse.Letter.Once()
    from rest in Parse.LetterOrDigit.Many()
    from trailing in Parse.WhiteSpace.Many()
    select new string(first.Concat(rest).ToArray());

var id = identifier.Parse(" abc123  ");

Assert.AreEqual("abc123", id);
```

### Examples and Tutorials

The best place to start is [this introductory article](http://nblumhardt.com/2010/01/building-an-external-dsl-in-c/).

**Examples** included with the source demonstrate:

* [Parsing XML directly to a Document object](https://github.com/sprache/Sprache/blob/master/samples/XmlExample/Program.cs)
* [Parsing numeric expressions to `System.Linq.Expression` objects](https://github.com/sprache/Sprache/blob/master/samples/LinqyCalculator/ExpressionParser.cs)
* [Parsing comma-separated values (CSV) into lists of strings](https://github.com/sprache/Sprache/blob/master/test/Sprache.Tests/Scenarios/CsvTests.cs)

**Tutorials** explaining Sprache:

 * A great [CodeProject article by Alexey Yakovlev ](http://www.codeproject.com/Articles/795056/Sprache-Calc-building-yet-another-expression-evalu) (and [in Russian](http://habrahabr.ru/post/228037/))
 * Mike Hadlow's example of [parsing connection strings](http://mikehadlow.blogspot.com.au/2012/09/parsing-connection-string-with-sprache.html)

**Real-world** parsers built with Sprache:

 * The [template parser](https://github.com/OctopusDeploy/Octostache/blob/master/source/Octostache/Templates/TemplateParser.cs) in [Octostache](https://github.com/OctopusDeploy/Octostache), the variable substitution language of [Octopus Deploy](https://octopus.com)
 * The [XAML binding expression parser](https://github.com/OmniGUI/OmniXAML/blob/master/OmniXaml/InlineParsers/Extensions/MarkupExtensionParser.cs) in [OmniXaml](https://github.com/OmniGUI/OmniXAML), the cross-platform XAML implementation
 * The query parser in [Seq](https://getseq.net), a structured log server for .NET
 * The [connection string parser](https://github.com/EasyNetQ/EasyNetQ/blob/master/Source/EasyNetQ/ConnectionString/ConnectionStringGrammar.cs) in [EasyNetQ](http://easynetq.com/), a .NET API for RabbitMQ
 * The [markup parsers](https://github.com/AvaloniaUI/Avalonia/blob/master/src/Markup/Avalonia.Markup.Xaml/Parsers/SelectorGrammar.cs) in [AvaloniaUI](https://github.com/AvaloniaUI/Avalonia), the multi-platform desktop .NET UI framework
 * [ApexSharp parser](https://github.com/apexsharp/apexparser/blob/master/ApexParser/Parser/ApexGrammar.cs), a two-way [Apex to C# transpiler](https://github.com/apexsharp/apexparser) (Salesforce programming language)
 * Sprache appears in the [credits for JetBrains ReSharper](https://confluence.jetbrains.com/display/ReSharper/Third-Party+Software+Shipped+With+ReSharper#Third-PartySoftwareShippedWithReSharper-Sprache)

### Background

Parser combinators are covered extensively on the web. The original paper describing the monadic implementation by [Graham Hutton and Eric Meijer](http://www.cs.nott.ac.uk/~gmh/monparsing.pdf) is very readable. Sprache was originally written by [Nicholas Blumhardt](http://nblumhardt.com) and grew out of some exercises in [Hutton's Haskell book](http://www.amazon.com/Programming-Haskell-Graham-Hutton/dp/0521692695).

The implementation of Sprache draws on ideas from:

* [Luke Hoban's Blog](http://blogs.msdn.com/b/lukeh/archive/2007/08/19/monadic-parser-combinators-using-c-3-0.aspx)
* [Brian McNamara's Blog](http://lorgonblog.wordpress.com/2007/12/02/c-3-0-lambda-and-the-first-post-of-a-series-about-monadic-parser-combinators/)
