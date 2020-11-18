# React

React

## Basics

- One way data flow: from parent to child.
- Virtual DOM: Handles DOM manipulation for you.
```
npm install -g create-react-app // install react app creation tool
create-react-app robofriends // create a new react project called "robofriends"
cd robofriends && yarn start // open app in browser
```

## Destructuring props
We can destructure our props to make our code cleaner. Before:
```
const Card = (props) => { // Props
  const { name, email, id } = props; // Props
  return (
    <div className='bg-light-green dib br3 pa3 ma2 grow bw2 shadow-5'>
      <img alt='robots' src={`https://robohash.org/${id}?200x200`} />
      <div>
        <h2>{name}</h2>
        <p>{email}</p>
      </div>
    </div>
  )
}
```
After:
```
const Card = ({ name, email, id }) => { // Props
  return (
    <div className='bg-light-green dib br3 pa3 ma2 grow bw2 shadow-5'>
      <img alt='robots' src={`https://robohash.org/${id}?200x200`} />
      <div>
        <h2>{name}</h2>
        <p>{email}</p>
      </div>
    </div>
  )
}
```

## React.Fragment and Semantic HTML
One thing you will notice with React is that because we always have to return just one element from a component, we end up wrapping a lot of our components in ```<div></div>```

BUT WHAT ABOUT SEMANTIC HTML!??!!

You are right! React realized this was an issue, and with the newer version of React 16.2, they introduced something called Fragment to fix this issue: https://blog.logrocket.com/rendering-sibling-elements-react-fragments/

## Parent / Child Components
- One way data flow: from parent to child.
- One-way data flow: We always have a parent, such as an app component, with children, that have their own children, etc. We can have one big app component that has different children so that we make each component small and reusable.

Right now, we have a Card component, which we are rendering over and over:
```
// index.js

ReactDOM.render(
  <React.StrictMode>
    {/* // Create greeting prop */}
    <div>
      <Card id={robots[0].id} name={robots[0].name} email={robots[0].email} />
      <Card id={robots[1].id} name={robots[1].name} email={robots[1].email} />
      <Card id={robots[2].id} name={robots[2].name} email={robots[2].email} />
    </div>
  </React.StrictMode>,
  document.getElementById('root')
);
```
Let's create a CardList component, that will be a parent of Card, so that we can just render 1 CardList instead of many individual Card components.

```
// components/CardList.js

const CardList = ({ robots }) => {
  const cardArray = robots.map((user, i) => {
    return <Card id={robots[i].id} name={robots[i].name} email={robots[i].email} />
  })
  return (
    <div>
      { cardArray }
    </div>
  );
}
```

## Key Prop

Note: Each child in an array or iterator should have a unique key prop. This error shows up in the browser console. This is just something you have to remember for loops. Basically, React needs to be able to identify each element easily without changing the entire DOM, which is why it asks for a unique key prop.

The key prop should have something that doesn't change. For example, index (i) could change if array items get moved, so it is not the best option for a key prop. It's better to use something unique, like the ID.

```
// components/CardList.js

const CardList = ({ robots }) => {
  const cardArray = robots.map((user, i) => {
    return (
      <Card 
        key={robots[i].id} // Key Prop Unique Identifier
        id={robots[i].id} 
        name={robots[i].name} 
        email={robots[i].email}
      />
    );
  })
  return (
    <div>
      { cardArray }
    </div>
  );
}
```


