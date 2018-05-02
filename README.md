# Simple React App Using Hacker News API

This is a simple React App that shows the difference between class and functional components. It does not use a 3rd party state library, such as Redux or Mobx, but instead relies on native React setState to handle data flow.

It uses a number of React lifecycle methods including:
- constructor()
- render()
- componentDidMount()

## Hacker News API
Hacker News is a news aggregator about tech topics. I used their search API to fetch trending stories from the platform.
[Hacker News Search API](https://hn.algolia.com/api)

## Client and Server-Side Search
The app utilises both client and server-side search. An onSearchSubmit() method is defined in the App component which fetches results from the Hacker News API when executing a search. The result object is then stored in the internal state, with the search term as key and the result as the value. This means you're not always querying the Hacker News API for searches you've already made. Time saved!

## Axios (fetch)
I opted to use the Axios instead of native fetch due to lack of support in older browsers. Axios is a library that solves only one problem, but it solves it with a high quality: performing asynchronous requests to remote APIs.


## Testing
I used Jest to write snapshot tests. The tests work by taking an initial snapshot of the rendered component and run this snapshot against future snapshots.

When a future snapshot changes, it notifies that there is a change in the UI that you might not have expected. You can either accept the snapshot change, because you changed the component implementation on purpose, or deny the change and investigate for the error.

It complements unit tests very well, which I used Enzyme to do. Enzyme is a testing utility by Airbnb to assert, manipulate and traverse React components.


## Some Other Things used
- Conditional Rending
- PropTypes
- Pagination
