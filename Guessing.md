``` mermaid
flowchart TD

%% Nodes 
    A("start")
    B("Generate Random Number")
    C("Prompt User Input")
    D("Output: Please guess a number from a to b")
    E("Input: User Guess")
    F("Input Validation")
    G("Is User Guess a Number?")
    H("Y")
    I("N")
    X(Output:You did not enter a number )
    J("Is User Guess Within Range ")
    K("Y")
    L("N") 
    Z(""Your Number was out of the guessing range"")
    M("Is user Guess > Number")
    N("Y")
    S("Your number was too high")
    O("N")
    P("Is user Guess < Number")
    Q("Y")
    Y(""Your number was too low"")
    R("N")
    U("Your Guess was correct!") 
    V("End")
%% Edge Connections Between Nodes
    A --> B --> C --> D --> F
                C --> E --> F
                F --> G 
                G --> H --> J --> K --> M --> N --> S --> C
                                        M --> O --> P --> Q --> Y --> C
                                                    P --> R --> U --> V
                            J --> L --> Z --> C
                G --> I --> X --> C
```
Documentation:

The flowchart illustrates the control flow for a random guessing game. The program begins by generating a random number within the range of A to B. At step C, following step B, the program prompts the user to input a guess. This input is stored in a variable named userGuess, and at this stage, the corresponding output message is displayed to the user.
To ensure the program functions correctly, the next section models a sequence of input validation checks. These tests verify the user's input against various potential failure cases, represented by nodes G, J, M, and P. If the input passes all these validation checks, the program proceeds to the END node. At this point, we conclude that the user's input matches the randomly generated number, as all other fail conditions have been ruled out.
