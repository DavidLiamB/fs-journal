# CSharp and SQL Fundamentals
01. What is the purpose of a `namespace`?

  > | it like import tells that file what other file it will need code from |

02. What is the difference between a `class` and an `interface`?

  > | classes are full build out with a constructor and methods while a interface is not, there for you can create an instance of a class but not and interface|

03. What is the method that returns an instance of a class, yet it has no return type?

  > | constructor |

05. In the Car example what is the access modifier of the `Start()` method?

  ```c#
  abstract class Car
  {
    public string Start()
    {

      return "Vroooom";

    }
  }
  ```

  > | Public |

06. In the Car example what is `string` an indication of?

  > | Type |

07. In the Car example what is `abstract` preventing?

  > | its preventing very declared method for needing to do something  |

08. In a SQL table, what is the difference between information in a row and information in a column?

  > | info in a row is all the info about one thing or object while the info in a column is the same info for different object or property |

09. Demonstrate the necessary SQL for creating a table called `characters` with the values `name, age, description` as strings, and an `int` id.

  > | INSERT INTO characters (name, age, description) value("guy", "20", "big strong man") |

10. In SQL how can you query more than a single table? Provide an example.

  > | with join [ SELECT * FROM table1 JOIN table2] |
