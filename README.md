# board-game-bots

A repo for building bots to beat games.

Roadmap
 * [ ] `Game` base class to track game state
 - [ ] Battleship
   - [ ] Implement game
     - [ ] Variants for returning "sunk" or not
     - [ ] Variants for whether or not ships can be adjacent
   - [ ] Implement strategies
     - [ ] Binary search
       - [ ] Update search pattern based on if white or black gets more coverage
     - [ ] Trinary search
     - [ ] Bayesian
     - [-] Neural net
 - [ ] Minesweeper
   - [ ] Implement game
         Don't worry about auto-revealing tiles
   - [ ] Implement strategy
     - [ ] Shadow board that keeps track of
       - \# of unlocated adjacent bombs 
       - \# of unlocated adjacent safe spaces
       - \# of unknown adjacent spaces
         - when this equals one of the other two, fill in all remaining spaces
       - Data types for bomb, safe, unknown, but also "maybe bomb" and "maybe safe"
     - [ ] Start coding in known safe patterns
       - <pre>O O O O
         1 2 2 1
         S S S S
        </pre> becomes <pre>O X X O
         1 2 2 1
         S S S S
        </pre>
       - <pre>O O O
         1 2 1
         S S S
        </pre> becomes <pre>X O X
         1 2 1
         S S S
        </pre>
       - Use central number as a hash key to limit searches
       - handle symmetries properly--rotational and reflective
     - [-] Neural net