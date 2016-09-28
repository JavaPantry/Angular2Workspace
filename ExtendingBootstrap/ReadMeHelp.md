# Bootstrap elements explained


### Navigation bar Toggle button
 
This three `<span class="icon-bar"></span>` spans are only to draw __the sandwich__ within button

    <button type="button" class="navbar-toggle" datatoggle="collapse" data-target=".navbar-ex1-collapse">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
    </button>

Let's take a look at the bootstrap.css

    .navbar-toggle .icon-bar {
      display: block;
      width: 22px;
      height: 2px;
      background-color: #cccccc;
      border-radius: 1px;
    }

It is a block structure, So, it is aligned as line by line. The background-color is set to be gray80. 

---

