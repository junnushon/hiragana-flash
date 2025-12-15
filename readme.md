# Hiragana and Katakana Flashcards / 히라가나 및 가타카나 플래시카드

![GitHub repo size](https://img.shields.io/github/repo-size/junnushon/hiragana-flash)
![GitHub issues](https://img.shields.io/github/issues/junnushon/hiragana-flash)
![GitHub forks](https://img.shields.io/github/forks/junnushon/hiragana-flash)
![GitHub stars](https://img.shields.io/github/stars/junnushon/hiragana-flash)
![GitHub license](https://img.shields.io/github/license/junnushon/hiragana-flash)

This is a simple web application that uses flashcard functionality to help you learn Hiragana and Katakana, two of the Japanese writing systems. The application displays a random Hiragana or Katakana character, and you can enter the pronunciation in Romaji (Romanized Japanese) or Korean. 

이 웹 애플리케이션은 플래시카드 기능을 사용하여 일본어의 두 가지 문자 체계인 히라가나와 가타카나를 배우는 데 도움을 줍니다. 애플리케이션은 무작위 히라가나 또는 가타카나 문자를 표시하며, 로마자(로마자로 된 일본어) 또는 한국어 발음을 입력할 수 있습니다.


## Live Site / 라이브 사이트

You can access the live site [here](https://junnushon.github.io/hiragana-flash/)

## Updates
- 2024-07-09 : Add characters / 문자셋 추가
  - Voiced consonants: 濁音 (だくおん, dakuon) / 탁음
  - Semi-voiced consonants: 半濁音 (はんだくおん, handakuon) / 반탁음
  - Contracted sounds: 拗音 (ようおん, youon) / 요음
  
## Features / 특징

- Displays a random Hiragana or Katakana character using flashcard functionality.
- Allows you to enter the pronunciation in Romaji or Korean.
- Provides feedback on whether your answer is correct or incorrect.
- Allows you to switch between Hiragana and Katakana.
- Adjusts the probability of character exposure based on usage.

---

- 플래시카드 기능을 사용하여 무작위 히라가나 또는 가타카나 문자를 표시합니다.
- 로마자 또는 한국어로 발음을 입력할 수 있습니다.
- 답변이 맞았는지 틀렸는지에 대한 피드백을 제공합니다.
- 히라가나와 가타카나 사이를 전환할 수 있습니다.
- 사용 빈도에 따라 문자 노출 확률을 조정합니다.

## How to Use / 사용방법

1. Visit the [here](https://junnushon.github.io/hiragana-flash/)
2. Select the script you want to learn (Hiragana or Katakana) from the dropdown menu.
3. A random character will be displayed.
4. Enter the pronunciation in the text box and click "Check Answer".
5. You will receive feedback on whether your answer is correct or incorrect.
6. Click "Next" to move on to the next character.

---

1. [여기](https://junnushon.github.io/hiragana-flash/)에 방문합니다.
2. 드롭다운 메뉴에서 배우고 싶은 문자(히라가나 또는 가타카나)를 선택합니다.
3. 무작위 문자가 표시됩니다.
4. 텍스트 상자에 발음을 입력하고 "정답 확인" 버튼을 클릭합니다.
5. 답변이 맞았는지 틀렸는지에 대한 피드백을 받습니다.
6. "다음" 버튼을 클릭하여 다음 문자로 이동합니다.

## Probability Algorithm / 확률 알고리즘

The application uses a probability algorithm to adjust the exposure frequency of each character:

1. **Initial Equal Probability**: Initially, all characters have an equal chance of being displayed.
2. **Tracking Exposure and Errors**: Each character tracks the number of times it has been shown (`showCount`) and the number of incorrect attempts (`wrongCount`).
3. **Recent Characters**: To prevent the same character from appearing too frequently, the last 10 characters shown are stored, and these characters are excluded from the selection pool until 10 other characters have been displayed.
4. **Least Shown Characters**: When selecting the next character to display, the application prioritizes characters that have been shown the least.
5. **Error-Weighted Probability**: After all characters have been shown at least once, the selection algorithm gives higher exposure probability to characters with higher `wrongCount` values, ensuring that difficult characters are reviewed more frequently.

This algorithm helps maintain a balanced and effective learning experience by ensuring all characters are practiced equally while focusing more on characters that the user finds challenging.

이 애플리케이션은 각 문자의 노출 빈도를 조정하기 위해 확률 알고리즘을 사용합니다:

1. **초기 동일 확률**: 처음에는 모든 문자가 동일한 확률로 표시됩니다.
2. **노출 및 오류 추적**: 각 문자는 표시된 횟수(showCount)와 잘못된 시도 횟수(wrongCount)를 추적합니다.
3. **최근 문자**: 동일한 문자가 너무 자주 나타나는 것을 방지하기 위해 마지막으로 표시된 10개의 문자를 저장하고, 이 문자는 10개의 다른 문자가 표시될 때까지 선택 풀에서 제외됩니다.
4. **가장 적게 표시된 문자**: 다음에 표시할 문자를 선택할 때, 애플리케이션은 가장 적게 표시된 문자를 우선적으로 선택합니다.
5. **오류 가중 확률**: 모든 문자가 최소한 한 번씩 표시된 후에는 선택 알고리즘이 wrongCount 값이 높은 문자에 더 높은 노출 확률을 부여하여 어려운 문자가 더 자주 복습되도록 합니다.

이 알고리즘은 모든 문자가 균등하게 연습되도록 하면서 사용자가 어려워하는 문자에 더 집중할 수 있게 하여 균형 잡힌 효과적인 학습 경험을 제공합니다.

## License

This project is open source and available under the [MIT License](LICENSE).
