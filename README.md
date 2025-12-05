# Dmoney — API Test Suite

Short Postman/Newman test suite for the Dmoney API (user transactions: send, deposit, cashout, payments).

## Table of contents
- Project
- Technology
- Prerequisites
- Installation
- Running tests
- Reports
- API documentation
- Notes

## Project
This repository contains a Postman collection and a small Node script to run the collection via Newman and generate an HTML report.

## Technology
- Node.js
- Postman
- Newman
- newman-reporter-htmlextra

## Prerequisites
- Node.js (v14+ recommended) and `npm` installed.
- A `SECRET_KEY` environment variable is required by the tests. Create a `.env` file in the project root with:

```
SECRET_KEY=your_secret_value_here
```

Replace `your_secret_value_here` with the appropriate key for the API under test.

## Installation
1. Install dependencies:

```
npm install
```

## Running tests
- Run the test script (this executes `report.js` which runs Newman and produces the HTML report):

```

```

- Alternatively, run Newman directly (adjust collection/environment filenames as needed):

```
npx newman run <collection.json> -e <environment.json> -r htmlextra --reporter-htmlextra-export Reports/report.html
```

## Reports
- After `npm test`, open the generated HTML report at `Reports/report.html`.
- There is also a `report.html` at the repo root (if produced by your setup).

## API documentation
Postman documentation: https://documenter.getpostman.com/view/37122492/2sB3dMxWQL

## Notes / Caution
- Ensure `SECRET_KEY` is set before running tests (tests depend on this value).
- If you need help locating the collection or environment files, check the Postman workspace or ask the test author.

## License
This repository does not specify a license. Add one if you intend to share the project publicly.



