# Intro to JavaScript
01. Which keywords are used to declare a variable in JavaScript?

    > | let mainly then const if you dont want it to be changed lastly var but its outdataed |

02. What is the definition of a function?

    > | is a block of code ran when called that peramiters can be passed tho |

03. What are the `SOLID` principles?

    > | single responsibility 
    open-closed
    Liskov substitution
    interface segregation
    dependency inversion |

04. Given this array: How could you remove the `pineapple`?

    ```js
    let fruit = ['apple', 'banana', 'pineapple', 'orange', 'strawberry']
    ```

    > | delete fruit[2] |

05. Given these two objects: How could you add each to the others friends arrays?

    ```js
    let you = {
        name: "You",
        hair: true,
        friends: []
    }
    let them = {
        name: "Them",
        hair: false,
        friends: []
    }
    ```

    > | you.friends += them
    them.friends += you |

06. Give an example of a JavaScript `Conditional`:

    > | an if statement |

07. What is the main difference between `parameters` and `arguments`?

    > | parameters are the conditions that are reqiured for the function the arguments are the values that the that are pass to a function to fill those conditions |

08. Instead of writing everything to the console, what is a better way to debug your code?

    > | by use the debug tool with visual code and the ones provided by you |

09. What is the difference between a `primitive` value and a `reference` value?

    > | primitive values are held while the reference value points to a place in memory|

10. Demonstrate a loop that prints the numbers between -100 and 100?

    > | let x = -100
    while(x<=100){
        consol.log(x)
        x++
    } |
