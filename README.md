## Your task

The year is 1600 and the Holy Roman Emperor and the King of Bohemia is Rudolf II. Rudolf II loves [science](https://en.wikipedia.org/wiki/Rudolf_II,_Holy_Roman_Emperor#Occult_sciences) and is a big believer in:
- the power of the blockchain in reducing tax evasion
- integer numbers
- the number Pi

You are tasked with creating a proof of concept contract that handles the division of collected taxes between the Holy Roman Empire and the kingdoms that comprise it. 

Since Rudolph is a big believer in integers, the indivisible currency unit is 1 *felt*.

The empire is always entitled to **at least** one $\pi$-th of **total all-time** collected taxes.

Rudolph doesn't want to leave any space for shenanigans by the empire's constituent kingdoms and will cut your head off if the contract doesn't always ascribe to the empire *at least* as many *felts* as it is entitled to according to the formula above like this:

- a kingdom collects 10 *felts* in taxes. Since $10/{\pi} \approx 3.183$, he expects to receive precisely 4 *felts*.
- a kingdom collects 314159 *felts*. Since $314159/{\pi} \approx 99999.9$, he is entitled to 10000 *felts*.
- a kingdom collects 1 *felt* in taxes. He wants it all or else you shall be executed.

---

The proof of concept doesn't at the moment take into account the fact that there are multiple kingdoms, thus it is only responsible for divison of taxes collected in one kingdom.

There should be three methods. 
1. or the tax collectors to permanently record how much taxes they collected on a given day
2. another one is for the king of the kingdom to collect its share of collected taxes. 
3. the final one is for the empire to collect the share of collected taxes that belongs to it

The collection methods return the amount of *felts* that the entity withdraws at the moment. It should note the withdrawal such that given two calls to this function, the second call always returns 0 as long as there hasn't been a call to method 1 with a nonzero amount deposited.

They can be called in any order.

If at any point, the last two calls to the contract are 2 and 3 (or 3 and 2), the total amount of collected taxes over the life of the contract should be equal to the total amount of withdrawn taxes over the life of the contract.

## Technical implementation details

You should write a smart contract in Cairo. You pull in any dependencies you wish. If you copy a substantial block of code from somewhere, please state its source in a comment.

You are free to internally represent numbers in any way you wish, but the inputs and outputs of the methods must be *felt*.

## Submission

TODO