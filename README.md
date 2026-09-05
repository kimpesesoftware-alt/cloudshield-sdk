import requests

response = requests.post(
    '[https://cloudshield-licensing-backend.onrender.com/check-access](https://cloudshield-licensing-backend.onrender.com/check-access)',
    json={'githubUser': 'YOUR_GITHUB_USERNAME'}
)

data = response.json()
print(data)
