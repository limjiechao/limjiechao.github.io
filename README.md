# [jiechaolim.com](https://jiechaolim.com)

Project Portfolio

## Features
- Displays correctly and beautifully on *all* screen sizes
- Renders the most optimal layout on for *every* screen sizes
- *No* CSS framework
- *No* JavaScript
- CSS grid and media queries for *responsive* layouts
  - 4-column × 1-row grid for >`1184px` width,
  - 2-column × 2-row grid for <`1184px` width
  - 1-column × 4-row grid for <`608px` width
- CSS flexbox
  - Responsive placement of quote marks enclosing the headline quotation
  - Quote marks will never touch the quotation or be awkwardly positioned
- CSS gradient
  - Portfolio backdrop,
  - Badges for language, framework, database used
  - Fallback backdrop

## CSS Flexbox

### Headline Quotation

<p align="center"><img src="./documentation/quotation.png"/></p>

```css
#quote-container {
  display: flex;
  flex-direction: column;
  padding: 20px;
  background-color: rgba(236, 233, 230, 0.64);
  background-blend-mode: overlay;
  border-radius: 30px;
  box-shadow: 3px 3px 3px #333333;
  font-family: Hoefler Text, Garamond, Palatino, Times, serif;
}

#quote-block {
  display: flex;
  flex-direction: column;
}

#quote-line {
  display: flex;
  flex-direction: row;
  align-items: bottom;
}

#open-quote {
  display: inline-block;
  padding-top: 6px;
  padding-left: 8px;
  color: black;
  margin-right: 6px;
  font-size: 60px;
  line-height: 1.0;
  vertical-align: bottom;
}

.nbsp {
  letter-spacing: 0.15rem;
}

#close-quote {
  display: inline-block;
  padding-right: 8px;
  text-align: right;
  color: black;
  font-style: normal;
  font-size: 60px;
  line-height: 0;
}

#quote {
  display: inline-block;
  max-width: 400px;
  vertical-align: middle;
  margin: 10px 10px 4px 10px;
  padding: 2px;
  color: black;
  line-height: 1.3;
  text-align: justify-all;
  font-size: 30px;
  font-style: italic;
  letter-spacing: 0.02em;
}
```

## CSS Grid

### 4-column × 1-row

<p align="center"><img src="./documentation/4-by-1.png"/></p>

```css
.portfolio {
  background: #8e9eab;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to top, rgba(236, 233, 230, 0.75), rgba(255, 255, 255, 0.9));  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to top, rgba(236, 233, 230, 0.75), rgba(255, 255, 255, 0.9)); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  color: black;
  padding: 1rem 2rem 2rem 2rem;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(5, auto);
  grid-row-gap: 0.8rem;
  grid-column-gap: 2rem;
  grid-template-areas:
    "title-1      title-2      title-3      title-4"
    "picture-1    picture-2    picture-3    picture-4"
    "links-1      links-2      links-3      links-4"
    "writeup-1    writeup-2    writeup-3    writeup-4"
    "techstack-1  techstack-2  techstack-3  techstack-4"
    "photo-credit photo-credit photo-credit photo-credit";
}
```

### 2-column × 2-row

<p align="center"><img src="./documentation/2-by-2.png"/></p>

```css
@media screen and (max-width: 1184px) {
  .top-half {
    background-image: url("../images/shooting-star-b.jpg");
  }

  .portfolio {
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(10, auto);
    grid-row-gap: 0.8rem;
    grid-column-gap: 2rem;
    grid-template-areas:
      "title-1      title-2"
      "picture-1    picture-2"
      "links-1      links-2"
      "writeup-1    writeup-2"
      "techstack-1  techstack-2"
      "title-3      title-4"
      "picture-3    picture-4"
      "links-3      links-4"
      "writeup-3    writeup-4"
      "techstack-3  techstack-4"
      "photo-credit photo-credit";
  }
}
```

### 1-column × 4-row

<p align="center"><img src="./documentation/1-by-4.png"/></p>

```css
@media screen and (max-width: 608px) {
  .portfolio {
    grid-template-columns: repeat(1, 1fr);
    grid-template-rows: repeat(20, auto);
    grid-row-gap: 0.7rem;
    grid-column-gap: 2rem;
    grid-template-areas:
      "title-1"
      "picture-1"
      "links-1"
      "writeup-1"
      "techstack-1"
      "title-2"
      "picture-2"
      "links-2"
      "writeup-2"
      "techstack-2"
      "title-3"
      "picture-3"
      "links-3"
      "writeup-3"
      "techstack-3"
      "title-4"
      "picture-4"
      "links-4"
      "writeup-4"
      "techstack-4"
      "photo-credit";
  }
}
```
