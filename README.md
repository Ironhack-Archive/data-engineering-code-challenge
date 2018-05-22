![Ironhack Logo](https://i.imgur.com/1QgrNNw.png)

# Ironhack Coding Challenge | Data Engineering

Welcome to Ironhack code challenge!

We hope you find this challenge interesting, but most important, it leads the way for you to become a Data Engineer at Ironhack. We won't provide any kind of starter code, so feel free to configure your own environment to achieve the proposed goals.

During the execution of this test, you will develop a crypt-comparison tool: a small website that will display a chart with information from a selected cryptocurrency.

The challenge is composed of four different blocks and it was intended to test the skills we think a Data Engineer should have. You will use an external API, Python, PostgreSQL, HTML and ChartJS.

Keep in mind that you are not required to complete the entire challenge in order to succeed, but of course, the more you achieve, the better.

As you will see, we don't like boring iterations, so we have named each block of the challenge differently — and we hope you like Harry Potter as much as we do 🧙

Upon challenge completion, please send us the GitHub repository link with the solution at product@ironhack.com.


## 1. Hufflepuff

First of all, we want to fetch the historical data of the following cryptocurrencies:

- Bitcoin (BTC)
- Ethereum (ETH)
- Ripple (XRP)
- Litecoin (LTC)
- Stellar (XLM)

You have to fetch all the information since January 1st of 2016, and you have to use the [CoinAPI.io](https://www.coinapi.io/) API. Read [the documentation](https://docs.coinapi.io/) to find out which API methods you will need to fetch the historical data of each cryptocurrency.

Note the following things about the API:

- **API Key**: this API requires a key to allow you to launch queries, so you'll have to create an API key to proceed.
- **Free Account**: if you check out the [API Pricing](https://www.coinapi.io/pricing), you'll see that the free accounts have a limitation of 100 daily requests. In the next iteration of the exercise we will solve this limitation, but keep in mind that you have this daily limit while fetching the information.

---

**To do**

- Create a script in Python that given a cryptocurrency symbol (i.e. BTC), it returns the historical data fetched from the API.

## 2. Ravenclaw

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

## 3. Slytherin

At this point, you already have a script that is fetching information from an API, and stores this information inside our own PostgreSQL database. Now it's time to show this information in a chart. To do that, you are going to use [chart.js](https://www.chartjs.org/).

In this iteration, you have to create a one-page website that has to fetch the information from the database, and show this information in a chart. The website has to have the following elements:

- Dropdown with all the cryptocurrencies you have in the database.
- Chart with the historical data of the current cryptocurrency selected in the dropdown.

The behaviour is super simple: every time you select a cryptocurrency in the dropdown, the chart has to show the related information in the database.

**To do**

- Create a one-page website with the following items:
  - Dropdown with all the currencies.
  - Chart that shows the current cryptocurrency historical data.
- Every time you change the value in the dropdown, the chart has to show the selected cryptocurrency data.

## 4 - Gryffindor

Last, but not least, we are going to integrate [Google Analytics](https://www.google.com/analytics/) into our application. First of all, you have to create and configure an Analytics account in the project. The goal of this iteration is to sent some information to the account.

When the user selects a cryptocurrency in the dropdown, you have to send an event to Google Analytics to track that this currency has been selected, so we can have stats about which currency is the most visited. You will need to implement an [Event Tracking](https://developers.google.com/analytics/devguides/collection/analyticsjs/events) that will be triggered when you select an element in the dropdown.

**To Do**

- Create a Google Analytics account.
- Trigger an event when the dropdown changes its value.
- Be able to see the tracked information in Google Analytics.

Good luck, and happy coding! :)
