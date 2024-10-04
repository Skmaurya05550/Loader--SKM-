# Square Loader Animation

This repository contains a square loader animation with hover effects. The loader animates using pure CSS and shows the text "Skm" in the center. Hover over it to see the transition effect.

## GIF & Animation

Here's a preview of the CSS-based square loader animation with the text "Skm" in the center:

![Square Loader Animation](https://i.ibb.co/xD0KXP1/IMG-20241004-175635.jpg)

[Click here to see the live animation demo](https://github.com/Skmaurya05550/Loader--SKM-)

## How it Works

The animation is built purely with CSS. Here's the code for reference:

```html
<br />
<div id="SquareLoader"></div>
<br />

<style>
body {
    display: grid;
    place-items: center;
    background-color:black; /* Optional: to match the loader's background color */
}

#SquareLoader {
    width: 10rem;
    height: 10rem;
    display: grid;
    place-items: center;
    color: seagreen;
    --c: no-repeat linear-gradient(#5cf75c 0 0);
    background: var(--c), var(--c), var(--c), var(--c);
    background-size: 1.6rem 1.6rem;
    background-color:black;
    animation: l5 2s infinite cubic-bezier(0.3, 1, 0, 1);
}

@keyframes l5 {
    0% { background-position: 0 0, 100% 0, 100% 100%, 0 100% }
    33% { background-position: 0 0, 100% 0, 100% 100%, 0 100%; width: 4rem; height: 4rem }
    66% {
        background-position: 100% 0, 100% 100%, 0 100%, 0 0; width: 4rem; height: 4rem;
    }
    100% { background-position: 100% 0, 100% 100%, 0 100%, 0 0 }
}

#SquareLoader::after {
    content: "Skm";
    position: center ;
    width: 2.8rem;
    height: 2.8rem;
    border: 0.2rem solid seagreen;
    display: grid;
    place-items: center;
    color: seagreen;
    background: #3eed9e;
}

#SquareLoader:hover::after {
    background: seagreen;
    color: #5cf75c;
    border: 1rem solid #3eed9e;
}
</style>
