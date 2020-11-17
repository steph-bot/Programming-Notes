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
