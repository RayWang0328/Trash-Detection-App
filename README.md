
# Colby Trash Deletion App

Marine debris presents substantial ecological challenge to the ecosystem of Maine's islands where volunteer groups annually undertake cleanup initiatives on islands. These cleanup efforts hindered by unpredictable challenges in trash volume and placement. In this web app, we created a pipeline that leverages aerial drones and machine learning to automatically detect, classify, and map marine trash. 

## Local Instillation 🛠️ 

### 0. CPU or GPU
It is advisable to run this program on your local machine only if you have a GPU that is CUDA compatible. The reason for this is because the models used in this app are pretty heavy, computationally. 

If you do have a CUDA compatible GPU, mnake sure its activated by running this after installing everything below:
```javascript
>>> python
>>> import torch
>>> torch.cuda.is_available()
```

If CUDA is properly set up, the above should print `True`

### 1. Clone Repository onto a folder local machine:
```javascript
git clone https://github.com/RayWang0328/Colby-Trash-App.git
```
### 2. Change Directory into folder and activate virtual environment

**For Windows Users:**

```javascript
cd Colby-Trash-App
py -3 -m venv .venv
.venv\Scripts\activate
```

**For Mac Users:**

```javascript
cd Colby-Trash-App
python3 -m venv env
. .venv/bin/activate
```

### 3. Install Required Libraries 
```javascript
pip install -r requirements.txt
```
```javascript
python -m pip install scipy
```
### 4. Install GroundingDINO libraries
```javascript
cd GroundingDINO/
```
Install dependencies:
```javascript
pip install -e .
cd ..
```
### 5. Download GroundingDINO weights
```javascript
mkdir weights
cd weights
wget -q https://github.com/IDEA-Research/GroundingDINO/releases/download/v0.1.0-alpha/groundingdino_swint_ogc.pth
cd ..
```
### 6. Run Application: 
```javascript
python app.py
```

Go to http://localhost:8000/ to see web app working
    
## Deployment

Alternatively, the app can be deployed as a web app on a website. This will cost money, but it can be accessed anywhere. 

Docker Image: 🐋
```javascript
  rayw03/trash-app
```
