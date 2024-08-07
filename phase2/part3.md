# Phase 2.3: JS Fundamentals

JavaScript/TypeScript syntax is similar to C/C++ syntax, but it's type system is much looser. A lot of your C/C++ knowledge will carry over. Learn X in Y has a very concise [overview of TypeScript](https://learnxinyminutes.com/docs/typescript/). 

What's the difference between JS and TS? 
- TypeScript is a superset of JavaScript: All valid JS code is valid TS code (but not the other way around). TS just adds a type system on top of JS which allows type safety and type checking. It's a quality-of-life upgrade to JS which allows us to catch errors earlier and faster.

Implement each of the following functions in the Phase 2.3 page

### Function 1: playable() - Check if an Uno card is playable
A Card is playable under standard Uno rules if it has the same color, value, or symbol as the top card of the discard pile or if it is a Wild Card.
    
    // Test Case
    const card = {
      color: "yellow",
      value: "7"
    }
    const topOfDiscardPile = {
      color: "red",
      value: "3"
    }
    console.log(playable(card, topOfDiscardPile)); // should print `false` to the console
    

### Function 2: playableCards() - Filter out all nonplayable cards
Takes an array of Card objects and the current discard card as an input. Return an array of only the playable cards from the input hand.

(Hint: Check out the JS `filter` function!)

    // Test Case:
    const hand = [{
      color: "yellow",
      value: "7"
    }, {
      color: "red",
      value: "8",
    }, {
      color: "blue",
      value: "Draw Two"
    }, {
      color: "wild",
      value: "Wild Draw Four"
    }]
    const topOfDiscardPile = {
      color: "red",
      value: "3"
    }
    console.log(playableCards(hand, topOfDiscardPile));
    /* Should Print Out
    [{
      color: "red",
      value: "8",
    }, {
      color: "wild",
      value: "Wild Draw Four"
    }]
    */

### Function 3: playCard(card, discardPile)
Attempt to play a card if it is playable If the card is playable, return a copy of the discard pile with the played card on top. Otherwise throw a runtime error of your choice.

    // Test Case
    const card = {
      color: "yellow",
      value: "7"
    }
    const discardPile = [{
      color: "blue",
      value: "7"
    }, {
      color: "green",
      value: "5"
    }]

    console.log(playCard(card, discardPile))
    /* Should Print Out
    [{
      color: "yellow",
      value: "7"
    }, {
      color: "blue",
      value: "7"
    }, {
      color: "green",
      value: "5"
    }]
    */
