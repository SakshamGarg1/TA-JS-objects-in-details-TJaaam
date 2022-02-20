# 🎖 Object Creation Patterns

Create a object using the following patterns given below.

## Create in all 4 formats

- [ ] Using function to create object
- [ ] Using Object.create (prototypal pattern)
- [ ] Using Pseudoclassical Way
- [ ] Using Class

## Requirements


Create User (class/function) with the following properties.

- [ ] properties (data):
  - [ ] name
  - [ ] id
  - [ ] noOfProjects
- [ ] methods:
  - [ ] getProjects -> return number of project
  - [ ] changeName -> accepts one parameter (newName)returns old user name
  - [ ] incrementProject -> returns updated number of projects
  - [ ] decrementProject -> returns updated number of projects

Write 2 tests for all the different ways of creating object. Test all the methods on these objects.



function createUser(name,id,noOfProjects){
    let user ={};
    user.name=name;
    user.id=id ;    
    user.noOfProjects=noOfProjects;
     
    user.getProjects = function(){
        return user.noOfProjects;
    };

    user.changeName = function(newName){
         let prvName=user.name;
         user.name= newName;
         return prvName;
    };
    
    user.incrementProject = function(){
        user.noOfProjects += 1;
        return noOfProjects

    };
    
    user.decrementProject = function(){
        user.noOfProjects -= 1;
        return noOfProjects;

    };
  return user;
 

}
let Saksham = createUser("saksham",123,23);
let Ram = createUser("Ram",23,123);


//prototypal Method

let userMenthod={


    getProjects : function(){
        return this.noOfProjects;
    },

    changeName : function(newName){
         let prvName=this.name;
         this.name= newName;
         return prvName;
    },
    
    incrementProject : function(){
        this.noOfProjects += 1;
        return noOfProjects

    },
    
    decrementProject : function(){
        this.noOfProjects -= 1;
        return noOfProjects;

    },
};
    function createUser(name,id,noOfProjects){
    let user =Object.create(userMenthod)
    user.name=name;
    user.id=id ;    
    user.noOfProjects=noOfProjects;
  return user;
    };

let Saksham = createUser("saksham",123,23);
let Ram = createUser("Ram",23,123);

console.group("Saksham");


//psudo classical Method


