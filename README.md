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
- If you want to stop the app `Dashboard => Your App Name => Resources => Pencil icon=> Flip the switch => Confirm`.

Wait about 10 mintues for heroku to deploy the model.

# Deployment
- Go to your heroku account: https://www.heroku.com/
- Go to apps: https://dashboard.heroku.com/apps and create new app (underscore is not supported)
- Choose deployment method `GitHub` and connect it
- DO NOT click `Enable Automatic Deploys`, each github change consume 30 min dyno hours, rather manually click build.
- Click `Deploy Branch`, wait until it completes, if something fails, push github changes and click deploy branch again.
- Click `View` button at the bottom, deployed website will open. e.g. https://pycaret-insurance-bhishan.herokuapp.com/

# Usage
```python

import requests
url = 'https://pycaret-insurance-bhishan.herokuapp.com/predict_api'
pred = requests.post(url,json={'age':55, 'sex':'male', 'bmi':59, 'children':1, 'smoker':'male', 'region':'northwest'})
print(pred.json())
```
