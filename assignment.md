# 01 HTML CSS Git: Code Refactor

One of the most common tasks for front-end and junior developers is to take existing code and refactor it to either meet a certain set of standards or implement a new technology. Web accessibility is an increasingly important consideration for businesses, ensuring that people with disabilities or socio-economic restrictions have access to their website, and helping them avoid litigation.

Your task is to refactor an existing webpage to make it accessible. An important rule to follow when working with someone else's code is the Scout Rule:

> Always leave the code you are editing a little cleaner than you found it.

To impress clients, you should always go the extra mile and improve their codebase for long term sustainability. Ensure that all links are functioning correctly and clean up the CSS to make it more efficient, consolidating CSS selectors and properties, organizing them to follow the semantic structure of the HTML elements, and including comments before each element or section of the page.

## User Story

```
AS A marketing agency
I WANT a codebase that follows accessibility standards
SO THAT our own site is optimized for search engines
```

## Acceptance Criteria

```
GIVEN a webpage meets accessibility standards
~~WHEN I view the source code~~
~~THEN I find semantic HTML elements~~
~~WHEN I view the structure of the HTML elements~~
~~THEN I find that the elements follow a logical structure independent of styling and positioning~~
~~WHEN I view the image elements~~
~~THEN I find accessible alt attributes~~
~~WHEN I view the heading attributes~~
~~THEN they fall in sequential order~~
~~WHEN I view the title element~~
~~THEN I find a concise, descriptive title~~
```

## Review

You are required to submit the following for review:

* The URL of the deployed application.

* The URL of the GitHub repository. Give the repository a unique name and include a README describing the project.

## Starting HTML

```
<!DOCTYPE html>
<html lang="en-us">

<head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" href="./assets/css/style.css">
    <title>website</title>
</head>

<body>
    <div class="header">
        <h1>Hori<span class="seo">seo</span>n</h1>
        <div>
            <ul>
                <li>
                    <a href="#search-engine-optimization">Search Engine Optimization</a>
                </li>
                <li>
                    <a href="#online-reputation-management">Online Reputation Management</a>
                </li>
                <li>
                    <a href="#social-media-marketing">Social Media Marketing</a>
                </li>
            </ul>
        </div>
    </div>
    <div class="hero"></div>
    <div class="content">
        <div class="search-engine-optimization">
            <img src="./assets/images/search-engine-optimization.jpg" class="float-left" />
            <h2>Search Engine Optimization</h2>
            <p>
                The dominance of mobile internet use means that users are searching for the right business as they travel, shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility and find the right customers for your business.
            </p>
        </div>
        <div id="online-reputation-management" class="online-reputation-management">
            <img src="./assets/images/online-reputation-management.jpg" class="float-right" />
            <h2>Online Reputation Management</h2>
            <p>
                The web is full of opinions, and some of these can be negative. Social media allows anyone with an internet connection to say whatever they want about your business. Online Reputation Management gives you the control over what potential customers see when they search for your business.
            </p>
        </div>
        <div id="social-media-marketing" class="social-media-marketing">
            <img src="./assets/images/social-media-marketing.jpg" class="float-left" />
            <h2>Social Media Marketing</h2>
            <p>
                Social media continues to have a sizable influence on buying habits. Social media marketing helps you determine which platforms are suited to your brand, using analytics to find the right markets and increase your lead generation.
            </p>
        </div>
    </div>
    <div class="benefits">
        <div class="benefit-lead">
            <h3>Lead Generation</h3>
            <img src="./assets/images/lead-generation.png" />
            <p>
                Inbound strategies for lead generation require less work for your business, bringing customers directly to your website.
            </p>
        </div>
        <div class="benefit-brand">
            <h3>Brand Awareness</h3>
            <img src="./assets/images/brand-awareness.png" />
            <p>
                Users find your business through paid and organic searches, increasing the search ranking and visibility for your business.
            </p>
        </div>
        <div class="benefit-cost">
            <h3>Cost Management</h3>
            <img src="./assets/images/cost-management.png"></img>
            <p>
                As the search ranking for your business increases, your advertising costs decrease, and you no longer need to advertise your page.
            </p>
        </div>
    </div>
    <div class="footer">
        <h2>Made with ❤️️ by Horiseon</h2>
        <p>
            &copy; 2019 Horiseon Social Solution Services, Inc.
        </p>
    </div>
</body>

</html>
```

## Starting CSS
```
* {
    box-sizing: border-box;
    padding: 0;
    margin: 0;
}

body {
    background-color: #d9dcd6;
}

.header {
    padding: 20px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    background-color: #2a607c;
    color: #ffffff;
}

.header h1 {
    display: inline-block;
    font-size: 48px;
}

.header h1 .seo {
    color: #d9dcd6;
}

.header div {
    padding-top: 15px;
    margin-right: 20px;
    float: right;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    font-size: 20px;
}

.header div ul {
    list-style-type: none;
}

.header div ul li {
    display: inline-block;
    margin-left: 25px;
}

a {
    color: #ffffff;
    text-decoration: none;
}

p {
    font-size: 16px;
}

.hero {
    height: 800px;
    width: 100%;
    margin-bottom: 25px;
    background-image: url("../images/digital-marketing-meeting.jpg");
    background-size: cover;
    background-position: center;
}

.float-left {
    float: left;
    margin-right: 25px;
}

.float-right {
    float: right;
    margin-left: 25px;
}

.content {
    width: 75%;
    display: inline-block;
    margin-left: 20px;
}

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

.benefit-lead img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}

.benefit-brand img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}

.benefit-cost img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}

.search-engine-optimization {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
}

.online-reputation-management {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
}

.social-media-marketing {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
}

.search-engine-optimization img {
    max-height: 200px;
}

.online-reputation-management img {
    max-height: 200px;
}

.social-media-marketing img {
    max-height: 200px;
}

.search-engine-optimization h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

.online-reputation-management h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

.social-media-marketing h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

.footer {
    padding: 30px;
    clear: both;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    text-align: center;
}

.footer h2 {
    font-size: 20px;
}
```

- - -
© 2019 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
