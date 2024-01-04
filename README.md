### Hi there 👋
![Header](https://github.com/AikokulUlan-qa/AikokulUlan-qa/blob/main/assets/video.gif)
![giphy (2)](https://github.com/AikokulUlan-qa/AikokulUlan-qa/assets/154068607/350bf63a-88f3-45c5-9d5a-7dd83e8fb286)


### About me :sunglasses:
- QA engineer from Moscow.
- Experience in testing since 2023
- I’m currently learning QA Automation





💻 Technology stack
______________________________________________________________________________________________________________
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)
![HTML](https://img.shields.io/badge/html-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![Jira](https://img.shields.io/badge/jira-%230A0FFF.svg?style=for-the-badge&logo=jira&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-%23000000.svg?style=for-the-badge&logo=notion&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white)
![GraphQL](https://img.shields.io/badge/-GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white)
![Swagger](https://img.shields.io/badge/-Swagger-%23Clojure?style=for-the-badge&logo=swagger&logoColor=white)





⚓ Contact me :)
_________________________________________________________________________________________________________________
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)
![Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)
![Facebook](https://img.shields.io/badge/Facebook%20-015BE5?style=for-the-badge&logo=facebook&logoColor=white)


<picture>
  <source media="(prefers-color-scheme: dark)" srcset="github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="github-snake.svg" />
  <img alt="github-snake" src="github-snake.svg" />
</picture>
# @snk/solver

Contains the algorithm to compute the best route given a grid and a starting position for the snake.

## Implementation

- for each color in the grid

- 1\ **clear residual color** phase

  - find all the cells of a previous color that are "tunnel-able" ( ie: the snake can find a path from the outside of the grid to the cell, and can go back to the outside without colliding ). The snake is allowed to pass thought current and previous color. Higher colors are walls

  - sort the "tunnel-able" cell, there is penalty for passing through current color, as previous color should be eliminated as soon as possible.

  - for cells with the same score, take the closest one ( determined with a quick mathematic distance, which is not accurate but fast at least )

  - navigate to the cell, and through the tunnel.

  - re-compute the list of tunnel-able cells ( as eating cells might have freed better tunnel ) as well as the score

  - iterate

- 2\ **clear clean color** phase

  - find all the cells of the current color that are "tunnel-able"

  - no need to consider scoring here. In order to improve efficiency, get the closest cell by doing a tree search ( instead of a simple mathematic distance like in the previous phase )

  - navigate to the cell, and through the tunnel.

  - iterate

- go back to the starting point

<!--
**AikokulUlan-qa/AikokulUlan-qa** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
