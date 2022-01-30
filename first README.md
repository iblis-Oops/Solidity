# Solidity
pragma solidity ^0.6.0;

contract first{
    // This will initialize the variable with 0;
    uint256 public fav;
    function store(uint256 _x) public{
        fav = _x;
    }
    
    struct People{
        uint256 fav;
        string name;
    }

    People public person = People({fav : 23 , name:"Sourabh Mishra"});

    People[] public people;// This is initialization of a dynamic array: In this People array is defined of dynamic size with public view..

    

    /* View function is a function which does not do any transaction as it is only read only function does not changes state*/

    function retrieve() public view returns(uint256){
        return fav;
    }

    /*Same pure function is a read only funtion which only reads the chain but not change the state of blockchain..*/
    // function retrieve(uint256 fav) public pure{
    //     fav+fav;
    // }

    
