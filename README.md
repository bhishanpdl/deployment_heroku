# Build and deploy your first machine learning web app
- https://www.kdnuggets.com/2020/05/build-deploy-machine-learning-web-app.html
Website: https://pycaret-insurance-bhishan.herokuapp.com/

Wait about 10 mintues for heroku to deploy the model.

# Usage
```python

import requests
url = 'https://pycaret-insurance-bhishan.herokuapp.com/predict_api'
pred = requests.post(url,json={'age':55, 'sex':'male', 'bmi':59, 'children':1, 'smoker':'male', 'region':'northwest'})
print(pred.json())
```
