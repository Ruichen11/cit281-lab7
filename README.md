# cit281-Lab7
![Image](https://github.com/Ruichen11/cit281-lab7/blob/0f0c3b3144a5ba7452b890b3b89b918306f66c3e/roman-synkevych-vXInUOv1n84-unsplash.jpg)

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
