# Word Puzzle API

This is a Django application that provides an API for solving word puzzles.

## Prerequisites

- Required Python version to run the project is 3.5 or higher

## Installation

1. Clone the repository:

   ```
   git clone https://github.com/alex1899/wordpuzzleapi.git
   cd wordpuzzleapi/
   ```

2. Install the requirements:

   ```
   pip install -r requirements.txt
   ```

3. Apply the migrations:
   ```
   python manage.py migrate
   ```

## Running the Application

You can run the application using the Django development server:

The API will be available at `http://localhost:8000/`.

First, go into wordpuzzle folder:

```
cd wordpuzzle/
```

Then run the server with:

```
python manage.py runserver --noreload
```

## Testing the Endpoint

You can test the endpoint using `curl`, any HTTP client like Postman or by visiting the url in the browser

Here's an example of how to test the endpoint using `curl`:

```
curl -X GET 'http://localhost:8000/api/wordpuzzle?startWord=hit&endWord=cog' -w '\n'
```

This should return a JSON response with the shortest sequence of words from 'hit' to 'cog'.

Example response: `{"sequence": ["hit", "cit", "cot", "cog"]}`

Modify the `startWord` and `endWord` to get a different sequence.

## Running the Tests

You can run the tests using Django's test runner:

```
python manage.py test
```

## Test Coverage

To measure test coverage, you can use `coverage.py`:

1. Run the tests with coverage:

   ```
   coverage run --source='api' manage.py test
   ```

2. Generate a coverage report:

   ```
   coverage report
   ```

3. Generate an HTML coverage report:
   ```
   coverage html
   ```

The HTML report will be available in the `htmlcov` directory.

Coverage report for the project:

<img width="650" alt="Screenshot 2024-02-05 at 06 46 01" src="https://github.com/Alex1899/wordpuzzleapi/assets/48056584/fa33ea43-949d-4294-ba92-3b82babd866a">
