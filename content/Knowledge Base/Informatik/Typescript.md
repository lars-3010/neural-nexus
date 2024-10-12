> - Programming Language that is based on [[Javascript]]
> - allows developers to specify the types of data that they use in their code, such as numbers, strings, arrays, objects, functions
> - improves readability and maintainability of the code and can help to prevent bugs
> - supports classes, modules, decorators, async/await, etc.
> - any [[Javascript]] Code is Typescript Code, but Typescript Coe needs to be compiled into Javascript
___
[TypeScript: Documentation - TypeScript for JavaScript Programmers (typescriptlang.org)](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html)
___

## What is TypeScript?

- syntactic superset of JavaScript, adds **static typing**
- TypeScript adds syntax on top of JavaScript -> allowing developers to add **types**
- "Syntactic Superset" means that it shares the same base syntax as JavaScript, but adds something to it
---
## Why should I use TypeScript?

- JavaScript is a loosely typed language. It can be difficult to understand what types of data are being passed around in JavaScript.
- In JavaScript, function parameters and variables don't have any information! So developers need to look at documentation, or guess based on the implementation.
- TypeScript allows specifying the types of data being passed around within the code, and has the ability to report errors when the types don't match.
- For example, TypeScript will report an error when passing a string into a function that expects a number. JavaScript will not.
- TypeScript uses compile time type checking. Which means it checks if the specified types match **before** running the code, not **while** running the code.

## Configuring the compiler

By default the TypeScript compiler will print a help message when run in an empty project.

The compiler can be configured using a `tsconfig.json` file.

You can have TypeScript create `tsconfig.json` with the recommended settings with:

``npx tsc --init``

Which should give you an output similar to:

Created a new tsconfig.json with:  
TS  
```
  target: es2016  
  module: commonjs  
  strict: true  
  esModuleInterop: true  
  skipLibCheck: true  
  forceConsistentCasingInFileNames: true  `
```
  
You can learn more at https://aka.ms/tsconfig.json

Here is an example of more things you could add to the `tsconfig.json` file:

```ts
{  
  "include": ["src"],  
  "compilerOptions": {  
    "outDir": "./build"  
  }  
}
```
You can open the file in an editor to add those options. This will configure the TypeScript compiler to transpile TypeScript files located in the `src/` directory of your project, into JavaScript files in the `build/` directory.