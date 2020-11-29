---
layout: post
title: 1. Snoop into Selenium
author: Nagaraj BR

image: '/images/posts/1-1.jpg'
---

Hello guys*,* are you finding how to create a testing script to test your website*.* If yes, you landed a perfect page. When it comes to testing selenium plays the Lead role as well. Here we are going to explore the basic methods in selenium with a suitable Definition and a snippet of code opt one for each method. Before that have some brush-up sessions with Java and OOPS concepts.

This blog is recommended for one who is ready to know testing ideas with different types of tools and the importance of software testing to increase the quality of the product. I think this should be a better choice to learn different phase in software testing.

**What is What?** is the basic question for everyone when you kick off on any topic. Well! Before bouncing into 'Selenium' and its 'Methods', there should be a basic understanding of Selenium and its behavior. So here we go for a definition of selenium.

**Selenium :**

Selenium is a framework that is used to test your web application. It was developed by Jason Huggins in 2004. It also provides a interface which lets you write test scripts in programming languages like Ruby, Java, NodeJS, PHP, Perl, Python, and C#, among others. Selenium is a bunch of tool with different behaviour. Here the list of tools in selenium.

- Selenium Integrated Development Environment (IDE)
- Selenium Remote Control (RC)
- WebDriver
- Selenium Grid

**Why Selenium :**

Among more no.of paid testing suits this selenium is open-source with a stunning performance. I think this single reason is enough to go with this selenium tool for an organization to save in a big number. But still according to statistics around 25,000 organizations use selenium worldwide!

Even though there are many testing tools like HP Unified Functional Testing, Apache JMeter, HP Quality Centre, and Others. Selenium is still invited again and again only for its performance and easy handling techniques.

When you enter into selenium the 'Locator' methods are the heart of selenium. So by scrolling down we will figure out the Locator methods with prompt definition and snip of code to explore the methods appropriately.

**Packages in Selenium**

The package mechanism is to enclose the group of Classes and Sub Classes. These packages are used to avoid Conflicts. When you enter into selenium the package import way differ from one browser to another. List of ways to import the package as per browsers are 

**Chrome** **:**

```java
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
```

Firefox :

```java
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
```

Safari :

```java
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.safari.SafariDriver;
```

Opera :

```java
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.opera.OperaDriver;
```

**Locators**

**Definition** 

Locators are exactly a command which handles the UI elements to perform actions on the website. Identifying the appropriate Element is a challenging step to take. Henceforward the Selenium provided with a different type of method to approach.

**List of Selenium methods :**

- ID
- Name
- Link
- Class
- Xpath
- CSS Selector

**Element ID :**

It's a universal way to locate the element because the ID's are predominantly set as Unique elements on a web page by a developer. We can find the element's ID by using the inspect option in the Chrome browser.

**HTML Code :**

```html
*<input id="email" class="required" type="text">*
```
**Selenium Snip :**

```java
WebDriver driver=new ChromeDriver();
driver.findElement(By.id("email")).sendKeys("got_it");
```

By executing this "got_it" text will be filled in the "email" text box by given appropriate ID. Take note that ID must be unique.

**Element Name :**

Locating the "Name" element is similar to Id locator, where the slight changes in the attribute and its behavior. This element most likely used in the Loggin pages with suitable functionality. Mostly this attribute might be unique on the web page or may not.

**HTML Code :**

```html
*<input id="email" name="text" class="required" type="text">*
```

**Selenium Snip :**

```java
WebDriver driver=new ChromeDriver();
driver.findElement(By.name("text")).sendKeys("Hurry.!");
```

This snip selects the given name and types "Hurry" text which is passed as a value. On some web pages, the elements may have the same 'By.name' value in such cases elects some other Locator Element type which is preferable.

**Element Link :**

This will be the impeccable method to test your hyperlink provided on your web page. It deals only with anchor tags on a page

i.e: like "Forget Password?"

**HTML Code :**

```html
*<a href="http://www.facebook.com/recover/initiate/">Forgotten account?</a>*
```

**Selenium Snip :**

```java
WebDriver driver=new ChromeDriver();
driver.findElement(By.PartialLinkText("Forgotten account?")).click();
```

The above code will select a suitable hyperlink and perform the written functionality. There's nothing more stuff is present when you come to this Link element particularly.

**Element CSS Class Name :**

The ClassName element is to locate the attribute which is defined by the Class on-page. It helps when developers use uncommon styles for web pages mostly.

**HTML Code :**

```html
*<input type="email" class="inputtext login_form_input_box" name="email" id="email" data-testid="royal_email">*
```

**Selenium Snip :**

```java
WebDriver driver=new ChromeDriver();
driver.findElement(By.className(“inputtext login_form_input_box”)).sendKeys("Success");
```

When you run this bit of code it directly hits the first className with the relevant name given above and prints the 'success' message as assigned in the Email text field.

**Element Xpath :**

Xpath is one of the most important locators in Selenium. This locator mainly deals with XML Expressions. We are going to learn about Standard Xpath which can be obtained by the Chrome browser itself. Even we have User Defined Xpath which will be discussed in the upcoming hearings.

**To get Xpath from chrome :**

To open the Console in the Chrome by using inspect option and refer below given picture to select the XPath from the Chrome.

<img src="\images\pages\Xpath_selection.png">


**Selenium Snip :**

```java
WebDriver driver=new ChromeDriver();
driver.findElement(By.XPath(“/[@id='Login']”)).click();
```

The snip will perform the Click action on the given XPath locator as scripted. But the Default XPath may not be accurate in every corner while you writing the testing scripts.

**Element CSS Selector :**

CSS Selector is quite similar to the XPath locator, but both locators can be used where ever in the script it completely depends on their convenience. CSS Selector may be a bit faster when compared to XPath.

**To get CSS Selector from Chrome**

<img src="\images\pages\CSSSelector.png">

**Selenium Snip :**

```java
WebDriver driver=new ChromeDriver();
driver.findElement(By.cssSelector(“#pass”)).sendKeys("Abc@gmail.com")
```

This above snip will perform an action by sending the email-id as 'Abc@gmail.com' using the CSSSelector.