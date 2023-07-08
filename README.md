# wii menu page
A custom page that mimics the wii menu UI

## Customizing this page

To create a popup that looks like this:

![8NCj0VdXYu](https://github.com/cornetespoir/wii-menu-page/assets/35387318/ea40666a-d3f1-453f-aa88-bd6006c26888)

You need to make sure that the icon/button that you click on is set up like this, inside of ` <ul class="navigation">`:

```HTML
  <a href="#container-1">
    <img src="https://64.media.tumblr.com/57cf461a1819e5f240894118d1d0c568/d662040e3a2b8722-26/s400x600/c04c16872971599bb3c749bfa29c7d561c736247.pnj" alt="empty CD wii menu placeholder" />
  </a>
```
It needs 
1. an anchor (a) tag to wrap the content
2. the anchor tag needs to have a href attribute that contains the ID of the popup
3. content inside of the anchor tag that can be clicked on (in this case, an image of an empty disk)

Then, outside of the close `</ul>` tag, the popup HTML is set up like this:

```HTML
 <div id="container-1" class="content full">
                <div class="container">
                    <header></header>
                    <div class="wii">
                        Wii menu content
                    </div>
                    <div class="bottom">
                        <a href="#" class="button">
                            <span class="corner"></span>
                            <!-- put the text content inside <span class="text"> -->
                            <span class="text">Back</span>
                        </a>
                        <a href="" class="button">
                            <span class="corner"></span>
                            <!-- put the text content inside <span class="text"> -->
                            <span class="text">???</span>
                        </a>
                </div>
           </div>
    </div>
```

The id `id="container-1"` matches the href of our anchor tag `href="#container-1"`

If you want to make a smaller popup like this:

![RuaJaUuN26](https://github.com/cornetespoir/wii-menu-page/assets/35387318/aa5721f1-3459-495a-91f0-62db8d437ca5)

The set up is the exact same, except when adding the HTML for the popup itself, remove the "full" class from this line:

`<div id="container-1" class="content full">`

Remember that each popup needs a unique ID in order to work, so if you are copying and pasting sections, remember to update the id and href attributes accordingly. 
