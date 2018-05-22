![Ironhack Logo](https://i.imgur.com/1QgrNNw.png)

# Ironhack Coding Challenge | Data Engineering

Welcome to Ironhack code challenge! We hope you find it interesting and helps you becoming Ironhack Data Engineering. We don't provide any kind of starter code, so feel free to configure your environment to achieve the proposed goals.

During the execution of this test, you will create a crypt-comparisson, where you will create an small website to show a chart with the information of a selected cryptcurrency.

Once you have completed the code challenge, send us your Github repository link with the solution to product@ironhack.com.

This challenge is composed by four different parts and is made to test different skills that a Data Engineer should have. You will use an external API, Python, PostgreSQL, HTML and Chart JS. You don't have to do all of them. The more you do, the better knowledge we will have. We don't like boring iterations, so we have named each part of the challenge differently. We hope you like Harry Potter ;)

## 1 - Hufflepuff

First of all, we want to fetch the historical data of the following cryptocurrencies:

- Bitcoin (BTC)
- Ethereum (ETH)
- Ripple (XRP)
- Litecoin (LTC)
- Stellar (XLM)

You have to fetch all the information since 1st of January of 2016, and you have to use the [CoinAPI.io](https://www.coinapi.io/) API. Read [the documentation](https://docs.coinapi.io/) to find out which API method you will need to fetch the historical data of each cryptocurrency. Note the following things about the API:

- **API Key**. This API requires a key to allow you launch queries, so you'll have to create an API Key before proceed.
- **Free Account**.  If you check out the [API Pricing](https://www.coinapi.io/pricing), you'll see that the free accounts have a limitation of 100 daily requests. In the next iteration of the exercise we will solve this limitation, but keep in mind that you have this daily limit while fetching the information.

---

**To do**

- Create a script with Python that, given a cryptocurrency symbol (i.e. BTC), it returns the historical data fetched from the API.

## 2 - Ravenclaw

The second step of the project will allow us exceed the API daily limit. We are going to store the information in a PostgreSQL database. To do that, you have to review the API response structure, and create the correct database structure to store this information.

Our recommendation here is to create two different tables:

- The first one will store all the cryptocurrencies.
- The second one will store all the historical data.

The tables will have a *one to many relation*, that will join the cryptocurrency with his historical data.

---

**To do**

- Using the script you created on **Hufflepuff iteration**, insert the information inside a PostgreSQL database.
- Create a database structure with two tables.
- These tables will have a *one to many* relation.
- Feel free to use any database adapter to communicate Python and PostgreSQL.

## 3 - Slytherin

At this point, you already have a script that is fetching information from an API, and stores this information inside our own PostgreSQL database. Now it's time to show this information in a chart. To do that, you are going to use [chart.js](https://www.chartjs.org/).

In this iteration, you have to create a one-page website that has to fetch the information from the database, and show this information in a chart. The website has to have the following elements:

- Dropdown with all the cryptocurrencies you have in the database.
- Chart with the historical data of the current cryptocurrency selected in the dropdown.

The behaviour is super simple: every time you select a cryptocurrency in the dropdown, the chart has to show the related information in the database.

**To do**

- Create a one-page website with the following items:
  - Dropdown with all the currencies
  - Chart that shows the current cryptocurrency historical data
- Every time you change the value in the dropdown, the chart has to show the selected cryptocurrency data.

## 4 - Gryffindor

Sent information about the selected currency to a Google Analytics account.
