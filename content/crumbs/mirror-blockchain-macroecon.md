+++
title = "[Mirror] Blockchain Macroeconomics: Redesigning Financial Intermediaries"
date = "2018-09-04T00:00:00+00:00"
tags = []
+++

> **NOTE: This is just a mirror of my old writing from 2018 for record-keeping purposes. 1) My current self does not consider this writing to carry useful insights, 2) I may no longer agree / believe with some of the details here, and 3) this is just poorly written.** 

One of the most fundamental beliefs of blockchain based economies is the ability to have 100% control of one’s funds. This is quite the opposite of our current status, where the majority of the money supply is kept in banks and lent out to create profit. Because of this act of lending, many often regard banks as evil, or institutions that put people into debt. However, saying so without understanding our current financial system and the role of banks there wouldn’t make much sense. Understanding this complicated system could also help give insights to building future blockchain based economies. As such, in this two part series I would like to give an short explanation on what banks do, why removing banks are not that simple, and how the monetary system can be altered to preserve one’s rights to their assets without causing inefficiencies in the economy.

## What Banks Do
In traditional economies, banks serve multiple functions. They are responsible for:

- Acting as financial intermediaries between lenders and borrowers
- Creating new money
- Converting Short-Term Deposits into Long-Term Credit
- Investing idle money into productive sectors of the economy

### Connecting Lenders and Borrowers
First of all, banks act as financial intermediaries, connecting lenders with borrowers. When you deposit say for example a $100 bill in a bank, the bank is not required to store all of it. The bank can lend out most of it, storing only a fraction of it as a reserve. While you can still spend the $100 you’ve deposited via bank transfers, the money you spend will be in the form of credit, or more exactly, bank credit. Since there are thousands of depositors, you could also withdraw your deposit into hard cash, and the bank is able to cover it from reserves of other depositors. When a loan is paid back, a portion of the interest collected is shared with depositors, creating an financial incentive for more people to make deposits.

### Investing Idle Money into Productive Sectors
Quite a lot of people view this ability to lend out depositors’ money as one of the core reason why banks are evil. But in fact, this lending process is crucial for economic development. If you choose to keep your salary under the mattress, your salary can be considered as idle money, wasting its opportunity value. If you deposit your salary in a bank, it could be lent out to productive sectors and help fuel economic development. An entrepreneur willing to upgrade his/her factory could get funded by your deposit, increasing the factory’s efficiency and thus the productivity of the economy.

### Creation of New Money
When banks lend out deposits, both the deposit and the loan are spendable. If we assume a 10% reserve ratio for banks, a deposit of $1000 leads to a loan of $900, and the amount of money in the economy now increases by $900. The $900 that was lent out could eventually end up being deposited to a bank and $810 of it can be lent out. If this cycle continues, banks in theory can create up to $9000 from a initial deposit of $1000. Since money is created by loans, repayments destroy the created money, thus contracting the money supply. By this process, banks have the ability to control the amount of money in the economy.

People often think that banks will try to make as much loans, creating as much money as possible and indebting people. This however is not true (mostly), as ill-judged loans lead to defaults, or direct losses to banks. Too much defaults and the bank will end up with a low reserve ratio and a high chance of bankruptcy. The result is that banks will try to fund productive sectors which is the only way of creating new value. In theory, even money from loans made to non-productive sectors will eventually flow to productive ones, thus creating value indirectly (although I believe this does not work currently, thus the need for a better system design). If all goes well, the money supply will represent the capacity of future productive capacity of the economy (again, I do not believe this is the current case).

## Problems that could Arise when Banks are Removed
As seen above, banks play a critical role in the economy. Removing them without economic restructuring simply won’t do. Not considering this may lead to problems below.

### Uncertainty in Total Currency Supply
The currency supply of the economy can be divided into two, circulatory and non-circulatory. The argument here is that the amount of currency that is not actively used for trades within the economy should be minimized. Businesses that gain profit hoard currency to their contract addresses, thus putting them out of circulation.

Since all concepts discussed in this writing happen in a stablecoin based economy, we will assume that the contract only accepts stablecoins as the means of payment (currency of stable value is used to participate in the game). We will also assume that the duration is long enough to put long-term macroeconomic effects into consideration. As the contract operates and gains profit, currency that was in circulation is slowly deposited to the contract, thus becoming non-circulatory.

Given the assumption that long-term effects are considered, a decrease in circulating supply leads to an increase in currency value as the demand for transactions has not changed. To counteract this, new currency has to be printed and put into circulation in order to maintain the circulating supply the same as before. As a result, the total currency supply is increased. Problems arise as the business becomes less profitable and the currency previously hoarded is released into circulation. The circulating supply now increases and this decreases the currency value, requiring currency in circulation to be suctioned off and destroyed.

This makes it difficult to know the amount of currency currently being used in economic activities and gives uncertainties in future monetary policies.

### Excessive Waste of Value
This mechanism also removes a lot of value from the economy. Both the creation and destruction of currency tokens requires an incentive, and every bit of currency created consumes a bit of value as the incentive. However, currency tokens that get hoarded requires the same amount of currency to be printed and put into circulation, thus requiring double the amount for the process, and triple the amount if the hoarded amount goes back into circulation.

### Inefficient Capital Investments
There are mainly three possibilities for hoarded money in a bankless economy

1. Hoarded funds are not invested
2. Hoarded funds are invested by the owner

First, there is the method of assuring 100% control of one’s capital without a method of reinvesting hoarded funds. As hoarded currency decreases the circulating supply, currency is newly printed. The currency that was printed has to somehow enter economy. Putting the newly created currency in a specific part of the economy can be viewed an investment, the funds being retrieved when previously hoarded currency (the cause of newly printed currency) re-enters circulation.

Here, value is invested by a central source, the network. This is somewhat similar to full-reserve banking, since deposits cannot be lent out and the money supply is centrally controlled. Money centrally issued is invested from the central source without free market economic data contrary to fractional reserve banking. This process is inefficient because of reasons similar to why capital allocation in planned economies is inefficient. In order for investments to be made efficiently into the correct productive sectors, the investor needs to know the productivity of each technological sectors and the demand for capital of them. For example, VC investments in startups have a high ROI and a high failure rate. On the other hand, corporate bonds tend to be the opposite, assuring a low return but a safer investment.

In free-market based investments such as our current economy, this risk-reward balance will eventually reach equilibrium, where investments happen in the most efficient way. Projects with high ROIs relative to the risk (productive projects which lack investments) gets more funding until an equilibrium is reached. The increased amount of funds lowers returns and the allocation of capital reaches an optimal state.

By contrast, in a central investment program, the lack of a lending market will face difficulties in distributing funds because of the lack of economic variable that represents the demand for investment.

Next, we could allow individual companies to make separate investments, but this is also not free from inefficiencies. Companies can now go bankrupt not because they have poor quality products or failed to manage people, but because they have made bad investments. This significantly increases the chance of bankruptcy and distorts market efficiencies because now events outside of the company can have major effects inside the company.

Not only this but the efficiency of investments also goes down. A large bank can have lower reserve ratios than smaller banks because they can distribute their portfolios more widely and cover more losses. Likewise, smaller companies can only invest a smaller portion of their funds than larger corporations. Contrast to a economy where most of the investments are made by big banks, where they can make investments while maintaining a relatively low reserve ratio, risk management forces this bankless economy to invest less in total. Other difficulties that might arise is the loss of efficiency in investment market analysis due to economies of scale, and since returns on investments are now included in the companies profit, political conflicts within the company may disturb the company’s goals while wasting resources on internal fights.

> I would like to say that these are not arguments on why banks will naturally exist and total control of one’s assets is not possible. It is just an explanation on why current approaches of blockchain economy designs are not enough and why radically different approaches are essential to achieving a decentralized, bankless economy. 
> 
> The most important use case of money is being used as the medium of exchange, not a store of value. If store of value played an important role for old money, then new money should be designed to avoid this. However, this does not mean that money shouldn’t be stable in value. What I am suggesting is that there has to be an asset separate from the “medium of exchange” money that only fulfills the store of value need.