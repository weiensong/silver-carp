<h1 align="center">opsariichthys-bidens</h1>

<p align="center">
<img src="https://img.shields.io/badge/matlab-green" alt=""> <img src="https://img.shields.io/badge/license_-GPL3.0-green" alt=""> <img 
</p>

## Repository Introduction

Understand the game model of public goods, understand the evolution and propagation of cooperation, and use Monte Carlo simulation analysis to achieve mechanism modeling.

## Background Introduction

There are many restaurants of all sizes in the city, and each restaurant has a probability of being subjected to hygiene checks by relevant departments every day. If hygiene is not done on that day (i.e. betrayal), fines will be imposed. Use this mechanism to demonstrate cooperation and betrayal on four networks.

## Model ideas

When an individual is a collaborator and regardless of whether they undergo inspection or not, the collaborator has already done a good job of hygiene and will not be punished. At this point, the profit that the individual collaborator obtains from the whole is as follows:
$$
D(i) = \frac{{NC*r*c}}{{NCD}}
$$

When an individual is a betrayer and the probability of being tested meets the following criteria.
$$
inspectionP > 0.5
$$

The betrayer has not yet done a good job in hygiene, and at this point, the benefits of the betrayer are
$$
D(i) = D(i) - penaltyAmount
$$

Rewards are awarded when the group cooperation rate is less than 0.5. Finally, calculate the total income of the individual
$$
E\left( i \right) = totalpay - A\left( i \right)*NCD*c + A\left( i \right)*individualRewards
$$

Plus benefits from other groups
$$
individualRewards = individualRewards + reward\left( {Node\_neighbor\left( {i,j} \right)} \right)
$$
### Parameter Description
- c: Cooperation costs for collaborators
- r: Input-output ratio
- k: Rationality level
- penaltyAmount:Fine
- rewardAmount: Reward
- reward: group reward
- Cooperation_rate: Group combination work rate
- M1: Number of rows
- M2: Number of columns
- N: Number of game rounds
- A: Denotes a collaborator or betrayer
- D: Benefits of each individual in the group
- E: Total income per individual
- tongji: stores the proportion of collaborators at each moment
- NC: represents the number of co authors in group i


## Install

This project uses [Matlab](https://www.mathworks.com/products/matlab.html) [Git](https://git-scm.com/). Go check them out if you don't have them locally installed.

```shell
$ git clone 
```



## Related Efforts

- [MATLAB](https://www.mathworks.com/products/matlab.html)
- [Monte Carlo Analysis](https://www.investopedia.com/terms/m/montecarlosimulation.asp)



## Maintainers

[@weiensong](https://github.com/weiensong)



## Contributing


Feel free to dive in! [Open an issue]() or submit PRs.



### Contributors

This project exists thanks to all the people who contribute.



## License

[MIT]() © weiensong

