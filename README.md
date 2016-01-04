# Unix ASCII games

This is a source of [https://bronevichok.ru/games.html](https://bronevichok.ru/games.html).
Feel free to submit pull requests to add new games and improve information about
those already in the database.

## How to contribute

Check `games.yaml` out. All information is inside, and you should more or less
understand what's going on by reading it. Sorting is alphabetical.

Use this template:

```
- name: hangman
  clones:
    - name: hangman
      url: 
      repo: https://github.com/ligurio/ascii-games
      info: 
      added: 2015-02-01
      media:
        - url: http://somefreegame.com/img1.jpg
          image: http://somefreegame.com/img1_thumbnail.jpg
        - url: http://somefreegame.com/img2.jpg
          image: http://somefreegame.com/img2_thumbnail.jpg
        - raw: <iframe width="320" height="240" src="//www.youtube.com/embed/abcdefg1234?rel=0" frameborder="0" allowfullscreen></iframe>
```

- `name`/`names`: Name of the original game
  - If the game goes under multiple names, or if the clone is inspired by multiple related games, use `names`
  - A Wikipedia link is created for the name; if the article link is different, use the syntax `[Name, Name of Wikipedia article]`
- `clones`/`reimplementations`: List the clones/reimplementations under this heading. Multiple clones can be listed.
  - `name`: Name of the clone
  - `url`: URL of clone main page
  - `repo`: (optional) if the clone has an online code repository (e.g. GitHub), link here
  - `info`: free text, but try to use terms already used in the list. HTML is supported
  - `added`: (optional) date when this clone was first added. Newly added clones are highlighted
  - `media`: (optional) list of screenshots or videos for the clone
    - `image`: URL of an image to display, preferrably a thumbnail
    - `url`: (optional) link to a bigger image, when the user clicks the thumbnail
    - `raw`: to embed raw HTML, e.g. to embed a video, use this tag followed by raw HTML