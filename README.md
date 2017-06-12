Prettier for pre-commit
========================

Prettier package for pre-commit>=0.12.0.

For pre-commit: see https://github.com/pre-commit/pre-commit

For Prettier: see https://github.com/prettier/prettier


### Using Prettier with pre-commit

Add this to your `.pre-commit-config.yaml`:
```yaml

    -   repo: https://github.com/awebdeveloper/pre-commit-prettier
        sha: ''  # Use the sha or tag you want to point at
        hooks:
        -   id: prettier
            args: ['--write', '--single-quote'] 
            # list of args like '--single-quote', '--jsx-bracket-same-line', '--print-width 120', '--no-bracket-spacing'. 
            # If you specify an args array, it must include '--write'.
            additional_dependencies: ['prettier@1.1.0']
 ```          
  ### FAQ's
  
  **1.** Why does pre-commit say failed everytime prettier changes the file.
  
  **A.** This is how pre-commit works. You need to just add the files again and commit. This is done so that you can verify the changes. 
   
   
  **2.** Prettier has lot more args that you dont support.
  
  **A.** Just add them as args in the above snippet. See comment in the snippet above for example. 
  


   
