# UFOs

## Overview

Our goal here is to utilize HTML and JavaScript to create a dynamic webpage which allows visitors to filter various UFO sightings by date, location and UFO shape.

### HTML

Our [index.html](https://github.com/bristlab/UFOs/blob/main/index.html) document takes advantage of [Bootstrap](https://getbootstrap.com/) to quickly and easily create a layout for our site using `<DIV>` containers and basic CSS. Bootstrap does most of the heavy lifting for styling, whereas our `style.css` file handles the banner image. We import the Bootstrap stylesheet from a CDN using the following code:

`<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css"
integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous" />`

### data.js

 We've been provided with a [data.js](https://github.com/bristlab/UFOs/blob/main/static/js/data.js) file which contains descriptions of around one hundred UFO sightings from the first two weeks of 2010. We source this .js file using the following code:

 `<script src="static/js/data.js"></script>`


### D3

We require [D3](https://d3js.org/) to interpret and filter data found in the `data.js` file, as well as adding an event listener that detects user input dynamically. As with Bootstrap, we also load D3 from a CDN as follows:

`<script src="https://cdnjs.cloudflare.com/ajax/libs/d3/4.12.0/d3.js"></script>`

### app.js

The JavaScript functions we've written in [app.js](https://github.com/bristlab/UFOs/blob/main/static/js/app.js) handle the actual construction of the HTML table containing the `data.js` data, as well as determing which filters the user has modified. 


## Results

Our website has been deployed at [bristlab.github.io/UFOs](https://bristlab.github.io/UFOs/) so that users can check out the end result. For example, try entering `CA` into the 'state' input field and press enter. The table should then display all UFO sightings in California. As a bonus, we made sure that the form accepts both uppercase and lowercase characters by appending `.toLowerCase()` to our input strings.

![truth_is_out_there](https://github.com/bristlab/UFOs/blob/main/truth_is_out_there.png?raw=true)


## Summary

Unfortunately the dataset only contains around 100 entries spanning two weeks in the year 2010, and that isn't nearly enough data to draw any conclusions. While we have built a solid proof of concept here, if we want to confirm whether an alien invasion is imminent, we're going to need a lot more data.
