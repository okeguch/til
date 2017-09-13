# react × router
## Overview
When I wanted to use router with react×redux I arranged it because I did not know what it was.
______

## Docs
- react-router
    - [github](https://github.com/ReactTraining/react-router)
    - [npm](https://www.npmjs.com/package/react-router)
- react-router-redux
    - [github](https://github.com/reactjs/react-router-redux)
    - [npm](https://www.npmjs.com/package/react-router-redux)
- redux-router
    - [github](https://github.com/acdlite/redux-router)
    - [npm](https://www.npmjs.com/package/redux-router)


### Why do we need to use react-router

When writing SPA with React, I think that the URL does not change even if the rendered component changes and the screen transitions. In other words, the status of the URL and the state of the application are not related. Associating these two with each other makes it possible to access a specific state in the application from the URL, or conversely, to reflect the state change in the application in the URL is called routing. Routing has the advantage that you can use the back button of the browser and you can access a specific page directly by typing in a specific URL.
React-router is the de facto library for routing with react.

### react-router notation
First we import React and react-router.
I will use browserHistory this time.

~~~javascript
import React, { Component } from 'react';
import { render } from 'react-dom';
import { IndexRoute, Link, Router, Route, browserHistory } from 'react-router';
~~~


Just write the <Link> tag in the part you want to link. After rendering, this part contains a tag.

~~~javascript
class App extends Component {
    render() {
        return (
            <div>
                <ul>
                    <li><Link to="/">TOP</Link></li>
                    <li><Link to="/link1">link1</Link></li>
                    <li><Link to="/link2">link2</Link></li>
                </ul>
                <div>
                    { this.props.children }
                </div>
            </div>
        );
    }
}
~~~
