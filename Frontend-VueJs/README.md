## Idea of the App 💻

On this assignment you'll be creating a small Web App that will list the most starred Github repositories created after 30 days from the date filter (see attached mock). this is meant to demonstrate your knowledge and coding skills.

You'll be fetching the sorted JSON data from the Github API (explanation down below).

## Features 🚀

- As a User I should be able to list the most starred Github repos that were created after 30 days from the date filter.
- As a User I should see the results as a list. One repository per row.
- As a User I should be able to see for each repo/row the following details :
  - Repository name
  - Repository description
  - Number of stars for the repo.
  - Number of issues for the repo.
  - Username and avatar of the owner.
- As a User I should be able to keep scrolling and new results should appear (infinite scroll).

## Things to keep in mind 🚨

- Features are less important than code quality. So please put more focus on code quality and less on speed and number of features implemented.
- Your code will be evaluated based on: code structure, programming best practices, legibility.
- The git commit history (and git commit messages) will be also evaluated.
- Do not forget to include few details about the project in the README (e.g explain choice of libraries, how to run it ...)

- Bonus points on styling 😉.

## Mock 🍪

![alt text](https://raw.githubusercontent.com/Imtiyaz-CHOUJAI/coding-challenge/master/Frontend-VueJs/mock.png)

## How to get the data from Github 🌍

To get the most starred Github repos created in the last 30 days (relative to 2019-11-22), you'll need to call the following endpoint :

`https://api.github.com/search/repositories?q=created:>2019-11-22&sort=stars&order=desc`

The JSON data from Github will be paginated (you'll receive around 100 repos per JSON page).

To get the 2nd page, you add `&page=2` to the end of your API request :

`https://api.github.com/search/repositories?q=created:>2019-11-22&sort=stars&order=desc&page=2`

To get the 3rd page, you add `&page=3` ... etc

You can read more about the Github API over [here](https://developer.github.com/v3/search/#search-repositories).
