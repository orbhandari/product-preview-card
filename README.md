# product-preview-card
Practice project taken from Frontend Mentor.

Kevin Powell did a "walkthrough" as well, which I watched after.
Here's some notes for myself:

1. 
He used a custom CSS reset https://www.joshwcomeau.com/css/custom-css-reset/ .
This helps make images responsive, remove margins, make buttons/textarea inherit fonts by default, etc.

2. He makes the colors and fonts as custom CSS variables on :root element.

3. He adds classes liberally.

4. He started mobile first.

5. Start with generic styling first, e.g. 
    Note: he puts global font-styling in the body
body {
    font-family: var(...);
    font-weight: var(...);
}

6. He recommends to use rem for font sizes.

7. His go-to .flex-group utility class:

.flex-group {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap; //which comes up when things get very narrow
}

8. He puts a locally scoped CSS variable in his "product" class, i.e.

.product {
    --content-padding: 1.5rem;
}

.product__content {
    padding: var(--content-padding);
}

9. letter-spacing is fine to use px

10. <s></s> tag won't be read to a screen reader!
so add a span that is read when its screen reader
<span>Original price: </span>

https://www.scottohara.me/blog/2017/04/14/inclusively-hidden.html

11. he added data-icon in button as attribute
then target specifically with CSS:

.button[data-icon="shopping-cart"]::before {
    content: '';

    //he matches height and width with svg
    width: ..;
    height: ..;
}


