# TailwindCSS_Learn
This repository is a complitaion of my Tailwind CSS Learning Journey.
and this README file consists of my rough notes.

Tailwind CSS being the most used practices, This repo is/was created while I make/made switch to Tailwind CSS from Vanila CSS.

## Utility Class 
Tailwind CSS classes can be categorized into:
- Layout classes : Margin, padding, width, height
- Typography classes : font size, font weight, text alignment
- Background and Color classes
- Flexbox and grid classes
- Spacing classes

Using predefined utility classes might lead you to believe there are limited choices only, However it's not the case. In fact Tailwind is quite flexible in that context.
Just in Time (JIT) compiler allows you to create new CSS class on the go.
- **For Example:**
 A font size of 13px is not a predefined Utility Class but using syntaxes and JIT we can  
- font-[13px], square bracket

- [play.tailwindcss](https://play.tailwindcss.com) - A wonderful site that allows you to tally between the Tailwind CSS and the CSS you write.



### Example :
- __< h1 class="text-center text-lg text-blue-400" > Hello world  </ h1>__

 is equivalent to :

- .text-center {
  text-align: center;
}
.text-lg {
  font-size: 1.125rem;
  line-height: 1.75rem;
}
.text-blue-400 {
  --tw-text-opacity: 1;
  color: rgb(96 165 250 / var(--tw-text-opacity));
}

# Easy quick Notes 
- p : padding, px- padding x-axis (left), py- padding y-axis (top)
- m : margin, mx, my
- w : width, h : height
- text : for text related properties
- bg : background

### POSITION :
- In normal CSS -- **{ position : absoulte, relative, fixed, sticky }**
- In tailwind **< class="fixed" >**

### DISPLAY :
- flex, grid, block, inline, inline-block, none
- In tailwind : for parent < div class="flex justify-center space-x-6" > #child1, #child2 < /div>

### MEDIA QUERIES
Tailwind provides breakpoints
- sm 640px (min-width: 640px) _stying for screen width 640px or larger_ 
**Note: Focus on the use of max**
- max-sm 640px (min-width: 640px) _stying for screen width 640px or smaller_ 
- max-md 768px (min-width: 768px)
- max-lg 1024px (min-width: 1024px)
- max-xl 1280px (min-width: 1280px)
- max-2xl 1536px (min-width: 1536px)

### Modifiers
Indicate level or specific value,
- sm-small,
- lg-large,
- 2xL- 2 extra large

### Adding Properties 
- m-2, text-center

### Use of Pseudo Classes
Pseudo classes include hover,active, focus etc. So for ease just write down a pseudo Class followed by colon in TailwindCSS
- < button class= " hover:bg-green " > Click Here < / button >

### Styling for Dark mode
For styling in dark mode, a utility class can be defined after 
- < div class="**dark:_utilityClass_**" > Dark Styles < /div >
- Also you need to make changes in module.exports adding { darkMode="class",}

## Custom Styles
### I- Square Bracket meth0d

- **Color**
< p class= " text -2xl text-[#973F29] bg-[#456A]" >

- **Sizes**
< p class="text-[12px]" >

### II- Custom styles using Using Tailwind Config

**Inside Config**
 extend:{
   colors : {
      chestnut : '#973F2'
    }
 }

_in Code_
< p class=" text-chestnut bg-chestnut" >


### III- Can use components libraries like
- shadcn,
- tailwind UI,
- headless UI,

## Avoding Clutters :

< div class="card" > < /div>
_Here the card is not an ordinary className akin to Vanila CSS_

**inside @tailwind components**
@layer components {

  .card {
    @apply m-10 rounded-lg px-6 bg-blue shadow-xl
  }
}

_Better to apply this for only complicated larger componets rather than for all_



### Notes :
-using tailwind is not inline css
-You don't need to remember all utility classes.

