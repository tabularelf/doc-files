## Installing
1. Download Lexicons's .yymp from [releases!](https://github.com/tabularelf/lexicon/releases)
2. With your GameMaker Project, drag the .yymp (or at the top goto Tools -> Import Local Package)
3. Press "Add All" and press "Import".

## Updating to a new version
?> If you've made changes to `lexicon_settings`, consider backing it up (preferably with source control) before updating!

1. Delete `Lexicon`'s folder (with all scripts inside.)
2. Follow the steps through [Installing](#installing), but with the latest version.
3. Reimport your `lexicon_settings` (if changes were made)

## Using Lexicon
Once added to your project, Lexicon will automatically initialise its core functionality when you run the game.
Lexicon requires your language files to be in either JSON or CSV format. 

The format of these files are as follows:

<!-- tabs:start -->

#### **JSON A**

```json
{
	"language": "Languge Name",
	"locale": "locale",
	"text": {
		"text.entry": "TextA",
		"text.entry2": "TextB",
	}
}
```

#### **JSON B**

```json
{
	"language": "Languge Name",
	"locale": ["Locale A", "Locale B"],
	"text": {
		"text.entry": "TextA",
		"text.entry2": "TextB",
	}
}
```

#### **JSON C**

```json
{
	"language": "Languge Name",
	"locale": "locale",
	"text": {
		"entry": "textA",
		"entry2": "textB",
		"moreEntries": {
			"foo": "bar"
		}
	}
}
```

<!-- tabs:end -->

CSV:

| Language | Languge Name | Language Name 2 |
|------|------|------|
| Locale | Locale A | ["Locale B", "Locale C"] |
| text.entry| TextA | TextB |
| ------------------ | This cell is forcefully ignored as of [`LEXICON_ROW_SEPERATOR`](configuration.md) | |
| text.entry2| TextC | TextD |

Lexicon will assign all locales in an array to the same Language Name. 

Once you have your language files created, you can set it up as one of three ways.

<!-- tabs:start -->

### **The old way**

```gml
// To declare a language
// i.e. lexicon_index_declare("English", "en-US");
lexicon_index_declare("English", "en-US");
```

```gml
// To add JSON
// i.e. lexicon_index_add_json("en-US", "english.json")
// i.e. lexicon_index_add_json("English", "english.json")
lexicon_index_add_json("en-US", "english.json")
```

```gml
// To add CSV
// i.e. lexicon_index_add_csv("en-US", "locale.csv");
// i.e. lexicon_index_add_csv("English", "locale.csv");
lexicon_index_add_csv("en-US", "locale.csv");
```

### **The new way**

Note: These will add additional files if the language is already declared.

```gml
// i.e. lexicon_index_declare_from_json("english.json");
lexicon_index_declare_from_json("english.json");
```


```gml
// Which will declare multiple languages within the CSV.
// i.e. lexicon_index_declare_from_csv("locale.csv");
lexicon_index_declare_from_csv("locale.csv");
```

### **Definitions File**

(If you prefer to use the definitions file, see [here](definitions.md)

```gml
lexicon_index_definitions("definitions.json");
```

<!-- tabs:end -->

```gml
// Set Language
lexicon_language_set("English");
```


As for fetching text, you just need to do.
```gml
// For fetching text
// i.e. lexicon_text("game_intro_text");
var _text = lexicon_text("text.entry");
```