# Job Listing FastAPI Application

Live Demo [Link 🔗](https://fastapi-joblisting-api.onrender.com/docs)

Welcome to the Job Listing FastAPI Application! This repository contains a simple API built with FastAPI that allows users to manage job listings. The API supports adding, retrieving, updating, and deleting job entries.

## Features

- Add Job: Create a new job listing.
- Retrieve Jobs: Get a list of all job listings.
- Retrieve Job by ID: Get a specific job listing by its ID.
- Update Job: Update an existing job listing by its ID.
- Delete Job: Delete a job listing by its ID.

## Installation

### Prerequisites

Python 3.7+
FastAPI
Uvicorn

### Steps

1. Clone the repository:

```
Copy code
git clone https://github.com/your-username/job-listing-fastapi.git
cd job-listing-fastapi
```

2. Create and activate a virtual environment:

```
Copy code
python -m venv venv
source venv/bin/activate # On Windows use `venv\Scripts\activate`
```

3. Install the dependencies:

```
Copy code
pip install -r requirements.txt
```

4. Start the application:

```
uvicorn main:app --reload
```

## Usage

Once the application is running, you can interact with the API using an HTTP client like curl, Postman, or directly through the browser at http://127.0.0.1:8000.

## API Endpoints

### Add Job

- Endpoint: /add-job
- Method: POST
- Request Body:

```
{
"title": "Job Title",
"description": "Job Description",
"company": "Company Name",
"location": "Job Location"
}
```

- Response:

```
{
"id": 1,
"title": "Job Title",
"description": "Job Description",
"company": "Company Name",
"location": "Job Location"
}
```

### Retrieve Jobs

- Endpoint: /jobs
- Method: GET
- Response:

```
[
{
"id": 1,
"title": "Job Title",
"description": "Job Description",
"company": "Company Name",
"location": "Job Location"
},
...
]
```

### Retrieve Job by ID

- Endpoint: /jobs/{id}
- Method: GET
- Response:

```
{
"id": 1,
"title": "Job Title",
"description": "Job Description",
"company": "Company Name",
"location": "Job Location"
}

```

### Update Job

- Endpoint: /jobs/{id}
- Method: PUT
- Request Body:

```
{
"title": "Updated Job Title",
"description": "Updated Job Description",
"company": "Updated Company Name",
"location": "Updated Job Location"
}
```

- Response:

```
{
"id": 1,
"title": "Updated Job Title",
"description": "Updated Job Description",
"company": "Updated Company Name",
"location": "Updated Job Location"
}
```

### Delete Job

- Endpoint: /jobs/{id}
- Method: DELETE
- Response:

```
{
"message": "Job deleted successfully"
}
```

## Contributing

Contributions are welcome! Please fork this repository and submit a pull request for any changes you propose.

1. Fork the repository
2. Create a new branch (git checkout -b feature-branch)
3. Commit your changes (git commit -am 'Add new feature')
4. Push to the branch (git push origin feature-branch)
5. Create a new Pull Request
   License
   This project is licensed under the MIT License.
