# Quotes Repository

```markdown
# Quotes Repository

This repository contains a collection of 1500+ inspirational and thought-provoking quotes stored in a JSON file. You can access the quotes and their respective authors to display them in your web applications.

## JSON Structure

The JSON file stores each quote as an object with the following structure:

```json
[
  {
    "Author": "Thomas Edison",
    "Quote": "Genius is one percent inspiration and ninety-nine percent perspiration."
  },
  {
    "Author": "Yogi Berra",
    "Quote": "You can observe a lot just by watching."
  },
  {
    "Author": "Abraham Lincoln",
    "Quote": "A house divided against itself cannot stand."
  }
]
```

Each object contains:
- `Author`: The person who said the quote.
- `Quote`: The actual quote.

## Accessing Quotes

To fetch a random quote from the JSON file, you can use the following JavaScript code:

```javascript
// URL to the JSON file (replace with your actual file URL)
const quotesurl = 'https://raw.githubusercontent.com/Mayborg121/QuotesFileHostin/refs/heads/main/quotes.json';

// Fetch the JSON data
fetch(quotesurl)
    .then(response => response.json())
    .then(data => {
        // Handle the JSON data here
        const quotes = data[Math.floor(Math.random() * data.length)];
        setquote(quotes);
    })
    .catch(error => {
        console.error('Error fetching JSON:', error);
    });
```

This code:
1. Fetches the JSON data from the URL.
2. Randomly selects a quote.
3. Displays the selected quote by calling the `setquote()` function (you should define this function to display the quote on your webpage).

## Usage

To use this repository, simply fetch the `quotes.json` file and use the provided JavaScript code to display random quotes in your application.

Feel free to clone the repository and integrate it into your projects!

## License

This repository is open source and available under the [MIT License](LICENSE).

