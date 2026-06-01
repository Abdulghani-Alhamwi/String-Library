# 🧵 C++ String Utility Library

 A Library for clean and reusable string manipulation.

![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)

---

## 💡 What It Does

String Library gives you 22+ string utilities in a single `.h` file — no dependencies, no build step, just include and go.

Every method is available in two styles:

- **Static** — call directly without an object: `clsString::UpperAllString("hello")`
- **Instance** — create an object and call it directly: `myStr.UpperAllString()`

---

## 📦 Feature Overview

| Category | Methods |
|---|---|
| 🔠 Case Control : | `UpperAllString` · `LowerAllString` · `InvertAllLettersCase` · `UpperFirstLetterOfEachWord` · `LowerFirstLetterOfEachWord` |
| ✂️ Trim : | `TrimLeft` · `TrimRight` · `Trim` |
| 🔢 Count : | `CountWords` · `CountLetters` · `CountCapitalLetters` · `CountSmallLetters` · `CountSpecificLetter` · `CountVowels` |
| 🔀 Split & Join : | `Split` · `JoinString` |
| 🔍 Search & Replace : | `ReplaceWord` |
| 🔄 Transform : | `ReverseWordsInString` · `RemovePunctuations` |
| 📏 Inspect : | `Length` · `IsVowel` |

---

## 🚀 Getting Started :

### 1. Clone the repo

```bash
git clone https://github.com/your-username/string-library.git
```

### 2. Include the header

```cpp
#include "clsString.h"
```

### 3. Choose your style

```cpp
// Static — no object needed
string upper = clsString::UpperAllString("hello world");
// → "HELLO WORLD"

// Instance — object holds and updates the value
clsString s("  hello world  ");
s.Trim();
cout << s.Value; // → "hello world"
```

---

### 🔠 Case Control :

```cpp
clsString::UpperAllString("hello world");              // → "HELLO WORLD"
clsString::LowerAllString("HELLO WORLD");              // → "hello world"
clsString::InvertAllLettersCase("Hello World");        // → "hELLO wORLD"
clsString::UpperFirstLetterOfEachWord("hi there");     // → "Hi There"
clsString::LowerFirstLetterOfEachWord("Hi There");     // → "hi there"
```

---

### ✂️ Trimming :

```cpp
clsString::TrimLeft("   hello");    // → "hello"
clsString::TrimRight("hello   ");   // → "hello"
clsString::Trim("   hello   ");     // → "hello"
```

---

### 🔢 Counting :

```cpp
clsString::CountWords("hello world foo");             // → 3
clsString::CountVowels("hello");                      // → 2
clsString::CountCapitalLetters("Hello World");        // → 2
clsString::CountSmallLetters("Hello World");          // → 8
clsString::CountSpecificLetter("hello", 'l');         // → 2
clsString::CountSpecificLetter("Hello", 'h', false);  // → 1  (case-insensitive)

// Using the built-in enum
clsString::CountLetters("Hello", clsString::CapitalLetters); // → 1
clsString::CountLetters("Hello", clsString::SmallLetters);   // → 4
clsString::CountLetters("Hello", clsString::All);            // → 5
```

---

### 🔀 Split & Join :

```cpp
// Split by any delimiter
vector<string> parts = clsString::Split("one,two,three", ",");
// → ["one", "two", "three"]

// Join a vector back with a delimiter
string joined = clsString::JoinString(parts, " | ");
// → "one | two | three"

// Join a raw C++ array
string arr[] = {"a", "b", "c"};
string result = clsString::JoinString(arr, 3, "-");
// → "a-b-c"
```

---

### 🔍 Search & Replace :

```cpp
clsString::ReplaceWord("I love cats", "cats", "dogs");
// → "I love dogs"

clsString::ReplaceWord("Hello hello", "hello", "Hi", false); // case-insensitive
// → "Hi Hi"
```

---

### 🔄 Transform :

```cpp
clsString::ReverseWordsInString("hello world foo"); // → "foo world hello"
clsString::RemovePunctuations("Hello, World!");     // → "Hello World"
```

---

### 📏 Inspect :

```cpp
clsString::Length("hello");  // → 5
clsString::IsVowel('a');     // → true
clsString::IsVowel('b');     // → false
```

---

## 📁 Project Structure :

```
string-library/
└── clsString.h    ← everything lives here
```

---
