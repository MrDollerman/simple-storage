# 🧠 SimpleStorage – Beginner Solidity Contract

This is a simple smart contract built as part of my learning journey with the **Cyfrin Updraft** program. It demonstrates the basics of Solidity such as storing and retrieving values, using structs, arrays, and mappings.

---

## 🚀 Features

- **Store a Number**
  - `store(uint256 _favoriteNumber)` – Save a number on-chain.
  - `retrieve()` – Read the stored number.

- **Add a Person**
  - Uses a `Person` struct with a name and favorite number.
  - Adds each person to an array.
  - Also maps a person's name to their favorite number for quick access.

- **Mapping**
  - `mapping(string => uint256) nameToFavoriteNumber` – Get a person’s favorite number using their name.

---

## 📦 Code Summary

```solidity
struct Person {
    uint256 favoriteNumber;
    string name;
}

Person[] public listOfPeople;

function addPerson(string memory _name, uint256 _favoriteNumber) public {
    listOfPeople.push(Person(_favoriteNumber, _name));
    nameToFavoriteNumber[_name] = _favoriteNumber;
}
---


# 🔐 Tech Used
Solidity ^0.8.18

Cyfrin Updraft learning resources
***

📚 Learning Goals
This contract helped me learn:

How to use state variables

How to define and use structs and arrays

How to work with mappings in Solidity

Function visibility and memory management

Accessing smart contract data from another contract (used in StorageFactory)

📌 Notes
This is a beginner-level smart contract and serves as a foundation for more advanced projects in Solidity and smart contract development.
