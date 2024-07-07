# Hiragana and Katakana Flashcards

This is a simple web application that uses flashcard functionality to help you learn Hiragana and Katakana, two of the Japanese writing systems. The application displays a random Hiragana or Katakana character, and you can enter the pronunciation in Romaji (Romanized Japanese) or Korean. 

## Live Site

You can access the live site here: [Hiragana and Katakana Flashcards](https://junnushon.github.io/hiragana-flash/)

## Features

- Displays a random Hiragana or Katakana character using flashcard functionality.
- Allows you to enter the pronunciation in Romaji or Korean.
- Provides feedback on whether your answer is correct or incorrect.
- Allows you to switch between Hiragana and Katakana.
- Adjusts the probability of character exposure based on usage.

## How to Use

1. Visit the [live site](https://junnushon.github.io/hiragana-flash/).
2. Select the script you want to learn (Hiragana or Katakana) from the dropdown menu.
3. A random character will be displayed.
4. Enter the pronunciation in the text box and click "Check Answer".
5. You will receive feedback on whether your answer is correct or incorrect.
6. Click "Next" to move on to the next character.

## Probability Algorithm

The application uses a probability algorithm to adjust the exposure frequency of each character:

1. **Initial Equal Probability**: Initially, all characters have an equal chance of being displayed.
2. **Tracking Exposure and Errors**: Each character tracks the number of times it has been shown (`showCount`) and the number of incorrect attempts (`wrongCount`).
3. **Recent Characters**: To prevent the same character from appearing too frequently, the last 10 characters shown are stored, and these characters are excluded from the selection pool until 10 other characters have been displayed.
4. **Least Shown Characters**: When selecting the next character to display, the application prioritizes characters that have been shown the least.
5. **Error-Weighted Probability**: After all characters have been shown at least once, the selection algorithm gives higher exposure probability to characters with higher `wrongCount` values, ensuring that difficult characters are reviewed more frequently.

This algorithm helps maintain a balanced and effective learning experience by ensuring all characters are practiced equally while focusing more on characters that the user finds challenging.

## License

This project is open source and available under the [MIT License](LICENSE).
