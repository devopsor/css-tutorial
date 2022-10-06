### CCS_Tutorial


#### Introduction to CSS

CSS stands for Cascading Style Sheets. CSS is a standard style sheet language used to describe the presentation (i.e. layout and formatting) of web pages.

Before CSS, almost all presentation attributes of an HTML document were contained within HTML tags (especially within HTML tags). All font colors, background styles, element alignments, borders and sizes must be clearly described in HTML.

The consequence of this is that the development of a large website becomes a long and expensive process as style information is repeatedly added to each page of the website, and it also increases the cost of maintenance.

To solve this problem, CSS was introduced in 1996 by the World Wide Web Consortium (W3C), which also maintains its standard. CSS is designed to separate presentation and content. Web designers can now move a web page's formatting information into a separate style sheet, greatly simplifying HTML markup and improving maintainability.

CSS3 is the latest version of the CSS specification. CSS3 adds some new styling features and improvements to enhance web presentations.

#### What CSS can do

CSS can do so much more.

- You can easily apply the same style rule to multiple elements.
- You can use a single style sheet to control the display of multiple pages of your website.
- You can display the same page differently on different devices.
- You can style the dynamic state of an element (like hover, focus, etc.), which otherwise wouldn't be possible.
- You can change the position of an element on a web page without changing the markup.
- You can change the display of existing HTML elements.
- You can transform elements such as scale, rotation, skew, etc. in 2D or 3D space.
- You can create animations and transitions without using any JavaScript.
- You can create print-friendly versions of web pages.

The advantages of CSS are many more, and there are many other interesting things you can do with CSS. In the next chapters, you will learn about all of these in detail.


#### Advantages of using CSS

The biggest advantage of CSS is that it separates style and layout from the content of the document. There are more advantages here, why choose to use CSS?

- CSS saves a lot of time - CSS provides a lot of flexibility in setting style properties of elements. You can write CSS once. The same code can then be applied to groups of HTML elements or reused across multiple HTML pages.

- Ease of Maintenance — CSS provides an easy way to update the formatting of documents and maintain consistency across multiple documents. Because the content of an entire web page can be easily controlled using one or more style sheets.

- Pages load faster - CSS allows multiple pages to share formatting information, reducing the complexity and duplication of document structure content. It significantly reduces file transfer size, resulting in faster page loading.

- Advanced Styling of HTML - CSS has a wider range of presentation capabilities than HTML and provides better control over the layout of web pages. Therefore, you can make your web page look better than HTML represents elements and attributes.

- Multiple Device Compatibility - CSS also allows web pages to be optimized for multiple types of devices or media. Using CSS, the same HTML document can be rendered with different viewing styles for different rendering devices (e.g. desktop, mobile, etc.).

#### What this tutorial covers

This CSS tutorial series covers all the basics of CSS, including the concept of selectors, how to set colors and backgrounds, how to format fonts and text, styling UI elements like hyperlinks, lists, tables, and CSS boxes model, etc.

Once you're familiar with the basics, you'll move on to the next level, which will cover setting the size and alignment of elements, using image sprites to place elements on a web page, and the concepts of relative and associative. Absolute units, visual formatting models, display and visibility, layers, pseudo-classes and elements, media-related style sheets, and more.

Finally, you'll explore some of the advanced features introduced in CSS3, such as gradient colors, shadow effects, 2D and 3D transforms, alpha transparency, and ways to create transitions and animation effects, flex layouts, filter effects, media concept queries, and more.

#### Include CSS in HTML documents

CSS can be attached as a separate document or embedded in the HTML document itself. There are three ways to include CSS in an HTML document:

- Inline styles - use ***style*** attributes in HTML opening tags.
- Inline styles - use  ***\<style\>*** elements in the \<head\> of the document.
- External Style Sheets - use  ***\<link\>*** elements, pointing to external CSS files.

#### Inline CSS

An inline CSS is used to apply a unique style to a single HTML element.   
An inline CSS uses the style attribute of an HTML element.   
The following example sets the text color of the \<h1\> element to blue, and the text color of the \<p\> element to red:

```html
<h1 style="color:red; font-size:30px;"> This is a heading </h1>
<p style="color:green; font-size:22px;"> This is a paragraph. </p>
<div style="color: blue; font-size: 14px;"> This is some text content. </div>
```

#### Embedded style sheets

Embedded or internal style sheets only affect the document in which they are embedded.
Embedded style sheets use element definitions \<head\>in sections of an HTML document . \<style\>You can \<style\>define any number of elements in an HTML document, but they must appear between \<head\>and \</head\>tags. Let's see an example:

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        h1 {
            color: blue;
            text-align: center;
        }
        p {
            font-size: 18px;
            text-transform: uppercase;
        }
    </style>
</head>
<body>
    <h1>This is a heading</h1>
    <p>This is a paragraph.</p>
</body>
</html>
```

#### External style sheet

External style sheets are ideal when styles are applied to many pages of a website.

External style sheets keep all style rules in a separate document that you can link from any HTML file on your website. External style sheets are the most flexible because with external style sheets, you can change the look of your entire website by changing just one file.

You can attach external style sheets in two ways - linking and importing .

- Linking external style sheets

    Before linking, we need to create a stylesheet first. Let's open your favorite code editor and create a new file. Now type the following CSS code into that file and save it as "style.css".

```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <title> My HTML Document </title>
        <link rel="stylesheet" href="css/style.css">
    </head>

    <body>
        <h1> This is a heading </h1>
        <p> This is a paragraph of text. </p>
    </body>

    </html>
```

- Import external style sheets

    This @importrule is another way to load external style sheets. This @importstatement instructs the browser to load an external style sheet and use its styles.   
    You can use it in two ways. The easiest is within the header of the document. Note that other CSS rules may still be included in the \<style\> element. Here is an example:
    
    ```css
    @import  url( "css/layout.css" );
    @import  url( "css/color.css" ); 
    body  {
        color : blue;
        font-size :  14px ;
    }
    ```
