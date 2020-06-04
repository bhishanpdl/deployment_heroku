# Deploying apps to heroku using pycaret
- [heroku deployment using pycaret](https://www.kdnuggets.com/2020/05/build-deploy-machine-learning-web-app.html)
- [heroku free plan](https://www.heroku.com/free)
- [Heroku Dashboard](https://www.heroku.com/dx)

# Heroku
- deployed website: https://pycaret-insurance-bhishan.herokuapp.com/
- 550 free dyno hours for free plans and upto 5 apps
- extra 450 hours and upto 100 apps for credit card verified free plan.
- When request is sent app will be open for 30 minutes, and will be idle.
- If we enable Automatic Github Deployment, it will consume 30 mintues for each
  github push or changes.

Wait about 10 mintues for heroku to deploy the model.

# Usage
```python

import requests
url = 'https://pycaret-insurance-bhishan.herokuapp.com/predict_api'
pred = requests.post(url,json={'age':55, 'sex':'male', 'bmi':59, 'children':1, 'smoker':'male', 'region':'northwest'})
print(pred.json())
```
