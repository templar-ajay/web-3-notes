# web-3-notes
useful notes to revise web03


## install dfx version 0.9.3
```bash
DFX_VERSION=0.9.3 sh -ci "$(curl -fsSL https://sdk.dfinity.org/install.sh)"
```

## create new project
```bash
# project-name = hello
dfx new hello
```
then
```bash
npm install
```
then
```bash
dfx start
```
*split terminal*
```bash
dfx deploy
```
then 
```bash
npm start
```

## Motoko language 

- comments are same as js //
- let keyword is used to declare constant in motoko
- var keyword is used to declare variable in motoko
- := is used to reassign the value to a mutable variable.
```motoko
// import the debug module to access console functionality 
import Debug "mo:base/Debug";

// declare class with name DBank
actor DBank{
  // variables declared with var are mutable
  var currentBalance  = 300;
  currentBalance :=100;

  // variables declared with let are immutable
  let id = "0001"; // let means the value is constant in motoko.
  // id := 932 // cannot reassign an immutable variable.
  
  Debug.print("Jai Shree Ram");
  // to print a variable use debug_show() in Debug.print
  Debug.print(debug_show(currentBalance));
  Debug.print(debug_show("your id is ",id));
}
```


