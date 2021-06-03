# CIT281 Lab-7
![roman-synkevych-vXInUOv1n84-unsplash](https://user-images.githubusercontent.com/84296093/120626098-3062b800-c417-11eb-8c75-cdfe902cdb6b.jpg)

Purpose of this lab:
- Create an GitHub organization for the CIT minor
- Practice with error handling using JavaScript

### Lab Code: 
``` 
class CustomerError extends Error {
 // initialize the class 
    constructor(args){
        super(args);
        this.message = 'Customer error';
    }

    throwGenericErrror(){
        throw new Error("Generic error");
    }
    throwCustomError(){
        throw new CustomerError().message;
    }
}

// initialize a CustomError obj
const myError = new CustomerError();

//try - catch - finally block  generic error 
console.log("Force generic error");
try{
    console.log("Generic error try block");
    myError.throwGenericErrror();
} catch {
    console.log("Generic error catch block");
    console.log(myError.throwGenericErrror());
} finally {
    console.log("Generic error finally block");
}

// using custom error 
console.log("Force custom error");
try{
    console.log("Customer error try block");
} catch {
    console.log("Custom error catch block");
    console.log(myError.throwCustomError());
} finally {
    console.log("custom error finally block");
}
```

### What I learned: 
- Learned how to create a GitHub repository 
- Learned how to clone GitHub repository to local system
- Practiced with Try...catch...finally..throw errors


[SOurcecode](https://ruichen11.github.io/Ruichen11.CIT-Minor/)
