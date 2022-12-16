# Code Refactor 

## Technology Used 

| Technology Used         | Resource URL           | 
| ------------- |:-------------:| 
| HTML    | [https://developer.mozilla.org/en-US/docs/Web/HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) | 
| CSS     | [https://developer.mozilla.org/en-US/docs/Web/CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)      |   
| Git | [https://git-scm.com/](https://git-scm.com/)     |    

## Description 

https://famelga.github.io/code-refactor-site/

The client Horiseon, is looking to update their website to be more accessible. 

A screen reader is a common accessability tool used when searching the web. Having clearly marked tags allows for screen readers to more accurately identify the information that is on the page for the person using the tool. For this reason, I have replaced each div tag in the html file with the corresponding semantic element, which give meaning to the tags. 

Another html feature that can impact accessibility is the use of alternative texts (alt texts). The addition of alt texts provide a description of images, pictures, icons, figures, etc. that may not properly load. The descriptions provide the website visitor with an understanding of what the missing image would be displaying. Additionally, visitors who are using screen readers would have that description read to them.

The style.css document did consist almost entirely of id and class selectors. For this reason, the tag changes from html did not have real impact on the formatting of css. However, the were many repetitive ids and classes. These repeating selectors were consolidated, which required class renaming in both html and css.

https://famelga.github.io/code-refactor-site/

https://www.canva.com/design/DAFU47SVYTw/ANH6Kjx7ZrNfmk6TIH1THA/watch?utm_content=DAFU47SVYTw&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

<img scr="Untitled design.gif">


## Code Refactor Example

Below is the original html code with repeating div tags for different content and no alt text.


```html
  <div class="benefits">
        <div class="benefit-lead">
            <h3>Lead Generation</h3>
            <img src="./assets/images/lead-generation.png" />
            <p>
                Inbound strategies for lead generation require less work for your business, bringing customers directly to your website.
            </p>
        </div>
        <div class="benefit-brand">
```

The div tags were converted to semantic element tags to provide greater accessibility. Image alt text was also added. Section class benefits were also changed to be uniform.

```html
    <!-- Changed opening and closing div tags to aside -->
    <aside class="benefits">
           <!-- Changed opening and closing div tags to section -->
           <!-- Changed class title to benefit -->
        <section class="benefit">
            <h3>Lead Generation</h3>
            <!-- Added image alt text -->
            <img src="./assets/images/lead-generation.png" alt="Widget wheel funneling into coins." />
            <p>
                Inbound strategies for lead generation require less work for your business, bringing customers directly to your website.
            </p>
        </section>
           <!-- Changed opening and closing div tags to section -->
           <!-- Changed class title to benefit -->
        <section class="benefit">

```

These changes require some additional modification to the CSS selector.  

```css
.benefits {
    margin-right: 20px;
    padding: 20px;
    clear: both;
    float: right;
    width: 20%;
    height: 100%;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #2589bd;
}

.benefit-lead {
    margin-bottom: 32px;
    color: #ffffff;
}

.benefit-brand {
    margin-bottom: 32px;
    color: #ffffff;
}

.benefit-cost {
    margin-bottom: 32px;
    color: #ffffff;
}

.benefit-lead h3 {
    margin-bottom: 10px;
    text-align: center;
}

.benefit-brand h3 {
    margin-bottom: 10px;
    text-align: center;
}

.benefit-cost h3 {
    margin-bottom: 10px;
    text-align: center;
}
```

No longer targeting the element on the page with the class of 'header' but instead the css selector targeting the 'header' element 

```css
.benefits {
    margin-right: 20px;
    padding: 20px;
    clear: both;
    float: right;
    width: 20%;
    height: 100%;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #2589bd;
}

/* Consolidated three sections to use the same class */
.benefit {
    margin-bottom: 32px;
    color: #ffffff;
}

/* Consolidated three sections to use the same class */
.benefit h3 {
    margin-bottom: 10px;
    text-align: center;
}
```

## Usage 

Provide instructions and examples for use. Include screenshots as needed. 

To add a screenshot, create an `assets/images` folder in your repository and upload your screenshot to it. Then, using the relative filepath, add it to your README using the following syntax:

```md
![alt text](assets/images/screenshot.png)
```


## Learning Points 


This is a good place to Explain what you Learned by creating this application.
This is a great way to remind about all of the Complex Skills you now have.
If the user is less experienced than you:
They will be impressed by what you can do!

If the user is more experienced than you:
They will be impressed by what you can do!

Remember, it is easy to forget exactly how Valuable and Impressive your skills are, as well as How Much You’ve Learned!
So quantify that here!


## Author Info

### Fayven Amelga 


* [Portfolio](https://youtu.be/bHX54GCrDB4)
* [LinkedIn](https://youtu.be/bHX54GCrDB4)
* [Github](https://youtu.be/bHX54GCrDB4)



## Credits

List your collaborators, if any, with links to their GitHub profiles.

If you used any third-party assets that require attribution, list the creators with links to their primary web presence in this section.

If you followed tutorials, include links to those here as well.


## License

MIT License

Copyright (c) 2022 Fayven Amelga

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Badges

![MIT Badge](https://img.shields.io/badge/license-MIT-blue)

---

© 2022 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved.