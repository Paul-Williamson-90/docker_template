# Docker With FastAPI Template

- Quick starting point for creating a Docker container with FastAPI app

# How to run?
- From the root dir:
    - Ensure Docker Desktop is running
    - Run in the CLI:
        - docker build -t docker_image_name_here .
        - docker run -p 8000:8000 docker_image_name_here

# How to test
```python
import requests

response = requests.get("http://localhost:8000/")
if response.status_code == 200:
    print(response.text)

data = {
    "q": 3
}
response = requests.get("http://localhost:8000/items/1234", params=data)
if response.status_code == 200:
    print(response.text)
```