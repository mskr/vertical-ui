# vertical-ui
Using web apps can feel better

Vertical Design with Snapped Swiping and size-responsivity using only flexbox and max-width.

Use of semantic HTML which it builds a Vertical UI design from. Like this:

```
<aside>
<aside>
...
<aside>
<Main>
```

But it doesn't stack columns on mobile like many CSS frameworks. Instead it uses native Snap Scrolling, or a non-animated (radio button tabs) version for older browsers.

### Pointer Events

On document blur: display sleeping symbol and disable all pointer events. 

Mobile and Desktop.

Replace Hover and Touch events.

Look out for Samsung Internet compatibility, because it is widely used in other countries.

Reactive filtering:

1) Define "free areas"

1a) Trigger swipe only on free areas.

2) Smoothed through requestAnimationFrame

3) Ultimately enable native-like finger-synced animations for maximally natural UIs.

4) Allow only one listener per touch gesture, when the effect is big.

4a) Allow under conditions: When every handler individually has very small effect, or non user-facing effect multiple listeners are ok. 

5) Prevent touch gesture trigger together with one of these effects:

5a) Link activation

5b) Text selection

5c) Long press/ Context menu

5d) Native Scrolling

6) Long Press: Users typically longpress when they are stuck and don't know what their options are.

### Modals

Can be closed via X or Scrolling.

Use for images in large view.

Do not use noscroll JS and similar!

### Fitt's Law Optimization

Pointer travel distance as low as possible, target element size as large as possible (element area does not need to coincide with visible boxes or text size)

### Typography

A text is best readable when it has a line length of 60-70 characters.

The human eye can fixate around 4-5 characters at once.

### Honor user attention

Measure attention and engagement

When out of focus: everything greyscale

Prevent accidental typing without the input reaching the app.

### Scrolling Tools

Scrolling is the main interaction, but that doesn't mean it is only controlled via scrollbar or swiping. Navigation buttons and links are additional navigation tools.
  
### CSS Techniques
  
Flexbox and max-width: https://codepen.io/mskr/pen/gOpYRYM

CSS Grid: https://www.euismod.dev/

Scroll-behavior: https://developer.mozilla.org/en-US/docs/Web/CSS/scroll-behavior

Appbar and Navdrawer on transparent overlay with autohide and swiping:
Can be entirely controlled by native scrolling and snap-scrolling (No JS!). Only thing missing is passing events through overlay to page content. Possible in CSS with pointer-events: none, depending on swipe being a pointer event or not.

Snap-scroll: https://codepen.io/mskr/pen/qBEaoKv?editors=1100

Auto-hide header: https://codepen.io/mskr/pen/yLygXgO?editors=1000

Parallax: https://codepen.io/mskr/pen/NWPRoeK

Space-efficient navigation: https://codepen.io/mskr/pen/ExagEZL
