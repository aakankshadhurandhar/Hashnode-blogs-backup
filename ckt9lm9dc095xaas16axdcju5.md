## Multiple classes on the same element in  CSS

Recently in an interview, I was asked a question about multiple classes assigned to the same div in CSS. Let's see this in detail.

![hello](https://media.giphy.com/media/bcKmIWkUMCjVm/giphy.gif?cid=ecf05e47tl7d87s7pkhw1ghq4imngz6i4qcj3zmnzfjftqti&rid=giphy.gif&ct=g)



Many classes can be assigned to the div by the following method. Just separate in class names with spaces like this.


```
<div class="test1 test2 test3"> Hello  </div>
``` 

The div will then match style rules for three different selectors **.test1** **.test2** **.test3**

If the same property is declared in both the classes CSS  then conflict is resolved through specificity, then according to the order of CSS declarations. The order of classes does not matter.




```
<html>
  <head>
     <title>repl.it</title>
    <link href="style.css" rel="stylesheet" type="text/css" />
  </head>
  <body>
    <div class="class1 class2 class3">text 3</div>
    <script src="script.js"></script>
  </body>
</html>
``` 

style.css
```
.class3{
  background-color: yellow
}
.class1 {
    
    background-color: red
}

.class2 {
    background-color:#296BCB;
}

``` 
Output:


![Screenshot from 2021-09-07 08-52-38.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1630984973861/MnJRay1p4.png)

As we can see the CSS rule which is being declared at last is applied to the div.


Now, what if I have to make one CSS rule to higher specificity then we can use either **!important** or **div.** in the rule.


```
.class3{
  background-color: yellow !important
}
.class1 {
    
    background-color: red
}

.class2 {
    background-color:#296BCB;
}
``` 
output:

![Screenshot from 2021-09-07 09-05-17.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1630985730326/mPJYma4G8.png)


If the two rules don't conflict then both rules will be applied.


```
.class3{
  background-color: yellow !important
}
.class1 {
    color: brown
    
}

.class2 {
    background-color:#296BCB;
}

``` 
output:

![Screenshot from 2021-09-07 09-15-45.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1630986357145/6Hfi6iYva.png)

 [Repl link](https://replit.com/join/uodfovnnmg-aakankshadhuran) 

**References**

-  [MDN docs](https://developer.mozilla.org/en-US/docs/Learn/CSS/Howto/CSS_FAQ) 




That's all for this article. If you like this article do subscribe to the newsletter or follow me on  [Twitter](https://twitter.com/AakankshaDhura1) 

![thanks](https://media.giphy.com/media/KB8C86UMgLDThpt4WT/giphy.gif?cid=ecf05e472dg0itfuwnwrdfqbxtscqijvswdnddq21tv0p3y8&rid=giphy.gif&ct=g)









