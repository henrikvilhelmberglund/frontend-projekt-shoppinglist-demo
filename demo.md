---
theme: "night"
transition: "slide"
highlightTheme: "monokai"
logoImg: "assets/e.webp"
slideNumber: false
title: "Demo Frontend-projekt Shoppinglist"
---

### Moduler och Github

---

## Moduler

--

:::

index.html

```js
<script src="main.js" type="module" defer></script>
```

:::

::: { .fragment }

module-animations.js

```js
export function showUpdateModal(text) {
  let modal = document.createElement("div");
  let main = document.querySelector("main");
  modal.innerText = text;
  modal.className = "update-modal";
  main.prepend(modal);
  setTimeout(() => {
    main.removeChild(modal);
  }, 1400);
}
```

:::

::: { .fragment }

stateEditMode.js (längst upp)

```js
import { showUpdateModal } from "./module-animations.js";
```

:::

::: { .fragment }

stateEditMode.js (rad 314)

````js
saveToAPIBtn.addEventListener("click", async () => {
    if (itemListArray.length > 0) {
      selectedList = await saveList();
      listItemsUl.innerHTML = "";
      showUpdateModal("Your list was saved!");
      ```

:::

---

### Liveshare

parprogrammering!

---

## Github

--

### Github-repo (inställningar)

<!-- .slide: data-background="/assets/github_repo.png"  data-background-opacity=0.1 -->

Vi låste repot så att vi bara kunde committa med pull requests { .fragment }

--

### Vårt "flow"

1. Göra ny feature branch { .fragment }
2. Committa ändringar { .fragment }
3. git pull origin main { .fragment }
4. Lägga upp pull request { .fragment }
5. Merga in pull request i main { .fragment }

--

### Mergekonflikter

var är min kod?

![alt text](/assets/mergeconflict.gif "Title")

--

### Conventional commits

![alt text](/assets/conventional_commits.png "Title") {.fragment }

--

Commit and tag version

`npx commit-and-tag-version`

--

![alt text](/assets/changelog.png "Title")

--

![alt text](/assets/release.png "Title")

---

## Extensions

Vi gillade **Git Graph** och **GitHub Pull Requests and Issues**!

--

### Git Graph

--

![alt text](/assets/git_graph.png "Title")

--

### GitHub Pull Requests and Issues

--

![alt text](/assets/github_pull_requests_and_issues.png "Title")

---

## Lite stats

- 526 commits {.fragment}
- 145 pull requests {.fragment}
- 8 issues {.fragment}

