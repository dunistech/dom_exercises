Explanations to Text High-light
const replacedText = paragraph.innerText
  .replace(/\?/g, '🤔')
  .replace(/\!/g, '😲');
paragraph.innerText = replacedText;

1. What Does This Code Do?

This code:
- Takes the text inside a paragraph (HTML element).
- Finds all the question marks (`?`) in the text and replaces them with the emoji 🤔 (thinking face).
- Then, it finds all the exclamation marks (`!`) in the text and replaces them with the emoji 😲 (astonished face).
- Finally, it updates the paragraph's text with the modified version.

1. Breaking It Down

 a. `paragraph.innerText`
- `paragraph` refers to a DOM element (like `<p>`).
- `.innerText` gets the text inside the paragraph (not the HTML tags, just the text content).

For example:

<p id="myPara">Hello! How are you?</p>

If `paragraph` is this `<p>` tag, then:

paragraph.innerText // Output: "Hello! How are you?"

 b. `.replace(/\?/g, '🤔')`
- `.replace()`: Replaces specific parts of a string with something else.
- `/\?/g`: This is a regular expression (regex) that looks for all question marks (`?`) in the text.
  - `/`...`/`: The pattern is enclosed between slashes.
  - `\?`: Escapes the `?` symbol because it has a special meaning in regex. This ensures we search for the literal `?`.
  - `g`: A flag that means "global," so it replaces all occurrences of `?` in the text, not just the first one.
- `'🤔'`: The replacement for the question marks.

Example:
"How are you?".replace(/\?/g, '🤔');
// Output: "How are you🤔"

 c. `.replace(/\!/g, '😲')`
- This works the same way but targets all exclamation marks (`!`) and replaces them with 😲 (astonished face).

Example:
"Wow! So cool!".replace(/\!/g, '😲');
// Output: "Wow😲 So cool😲"

 d. `paragraph.innerText = replacedText`
- After replacing the question marks and exclamation marks in the text, we store the modified text in `replacedText`.
- Finally, we update the paragraph's text with the new version using `paragraph.innerText`.


1. Example in Action

<p id="myPara">Wow! What is this? It's amazing!</p>

const paragraph = document.getElementById("myPara");

const replacedText = paragraph.innerText
  .replace(/\?/g, '🤔') // Replace question marks with 🤔
  .replace(/\!/g, '😲'); // Replace exclamation marks with 😲

paragraph.innerText = replacedText;

<p id="myPara">Wow😲 What is this🤔 It's amazing😲</p>

1. Why Is This Useful?
- You can dynamically update and enhance text on a webpage based on patterns (e.g., replacing symbols, censoring words, or adding emojis).
- It's a great example of string manipulation combined with DOM manipulation. 

Tips for Newbies
- Practice Regex: Regular expressions might look intimidating, but they're just patterns used to search and replace text. Start with simple examples!
- Experiment: Try replacing other characters like `.` or `#`. Play with the code to see what happens.