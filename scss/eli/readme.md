# Eli is the Olympusat scss style library
## Why is it named Eli, you ask? Because I couldn't think of a name and eli is short and sweet. ;)
Follows the BEM and OOCSS methodologies

## Import all of it into your scss project 
```
@import './eli/eli';
```

## Import selective parts of the library
```
@import "./eli/color";
@import "./eli/type";
@import "./eli/buttons";
@import "./eli/forms";
@import "./eli/modal";
```

## Usage

#### Gotchas
1. When importing the form file individually, you must import the utils and buttons file first, as they're dependencies.
2. When importing any file indiviually, it's best to import utils first

```
@import "./eli/utils";
@import "./eli/buttons";
@import "./eli/forms";
```
```
@import "./eli/utils";
@import "./eli/buttons";
```

#### Examples
##### Run the index.html file to see a live example
```
 <!-- Common Components  -->
    <h1 class="eli--underline">H1 Eli scss library</h1>
    <h2 class="eli-h2--secondary">H2 Because Eli is short and sweeet</h2> 
    <br/>
    <br/>
    <h3>H3 Paragraph styles</h3>
    <h4 class="eli-h4--secondary">H4 This first paragraph is a lead paragraph</h4>
    <div class="eli">
        <p class="eli-lead">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec consectetur tincidunt ultrices. Pellentesque vel vehicula justo. In eget tellus eget nunc suscipit dignissim mollis non neque. Sed ut lacus ligula. Aenean feugiat erat ut ultrices fringilla. Vestibulum sed tellus feugiat, gravida lacus luctus, rhoncus nisi. Integer elementum quam lectus, placerat varius enim fringilla a. Aliquam ut ullamcorper enim. Mauris ultrices efficitur tellus, nec fringilla orci vehicula vel. Aliquam aliquam ante eget finibus euismod. Curabitur tempus lobortis eros a egestas. Vivamus odio velit, eleifend nec massa vel, sollicitudin pretium nunc. Sed pharetra nisi vel tellus facilisis pellentesque.</p>
        <p class="">Nam mollis molestie porttitor. <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" title="Click me!"/>Sed vulputate gravida enim</a>, non semper massa tincidunt at. Nunc consectetur porta consequat. In pretium mollis facilisis. Aliquam eros leo, hendrerit nec nunc sed, rutrum suscipit nunc. Maecenas ornare enim sed ultricies convallis. Donec volutpat ante eget nisl faucibus aliquam. Mauris lacinia, purus in volutpat bibendum, lorem nisi auctor urna, quis hendrerit tortor est nec orci. In et odio dui.</p>
    </div>
    
    <br/>
    <br/>
    <h2>H2 Forms</h2>
    <h3>H3 Form with squared edges</h3>
    <form class="eli-form">
        <label>Email
            <input type="text" placeholder="I'm an input"/>
        </label>
        <label>Message
            <textarea> Lorem Ipsum</textarea>
        </label>
        <input type="submit" value="Submit"/>
    </form>

    <br/>
    <h3>H3 Form with rounded edges</h3>
    <form class="eli-form eli-form--rounded">
        <label>Email
            <input type="text" placeholder="I'm an input"/>
        </label>
        <label>Message
            <textarea> Lorem Ipsum</textarea>
        </label>
        <input type="submit" value="Submit"/>
    </form>

    <br/>
    <br/>
    <h2>H2 Buttons</h2>
    <button class="eli-button">Click Me!</button> 
    <button class="eli-button--rounded">Click Me!</button> 
    <button class="eli-button--circle">Click Me!</button> 

    <br/>
    <br/>
    <h2>H2 Other H tags</h2>
    <h4>H4 Does anyone use h4s much?</h4>
    <h5>H5 Does anyone use h5s?</h5>
    <h6>H4 Does anyone use h6s?</h6>

    <br/>
    <br/>
    <h2>H2 pre &amp; code elements</h2>
    <pre>
        <code>
            import Promise from 'bluebird';
            import _ from 'underscore';
            import axios from 'axios';
            import memoize from 'fast-memoize';
        </code>
    </pre>

    <br/>
    <br/>
    <h2>H2 CSS Only Modal</h2>
    <div class="eli">
        <a href="#modal-one" class="eli-button--rounded">Click Me!</a>

        <!-- Modal -->
        <div class="eli-modal" id="modal-one" aria-hidden="true">
            <div class="eli-modal-dialog">
                <div class="eli-modal-header">
                <h2>CSS only modal</h2>
                <a href="#" class="eli-button--circle" aria-hidden="true">×</a>
                </div>
                <div class="eli-modal-body">
                <p>One modal example here! :D</p>
                </div>
                <div class="eli-modal-footer">
                <a href="#" class="eli-button--rounded">Some Action!</a>
                </div>
            </div>
        </div>
        <!-- /Modal -->
    </div>
```

## Overrides
To override particular styles, copy the _overrides.example.scss into your parent scss folder and rename it, importing it after the eli files in the cascade or wrap the import to bump specificity. [DON'T modify the examples files and don't modify any files inside the eli directory, it's bad practice and will make spaghetti out of any future updates.]
