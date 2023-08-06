### 마이크로서비스로서의 ML 모델 서비스 - Streamlight, Fast API 및 Docker

```
이 repo는 승객들이 타이타닉 재난에서 살아남았을지를 예측하기 위한 작은 웹앱에 대한 코드를 포함한다. 

애플리케이션은 프론트엔드와 백엔드로 구성되며 
API를 통해 마이크로서비스로서 ML 모델을 서비스하는 방법을 시연하는 데 사용된다. 

프론트엔드는 
Streamlit로 구축되어 사용자로부터 승객 정보를 획득하는 데 사용된다. 

백엔드는 
FastAPI 프레임워크로 구축되며 데이터를 전처리하고 
모델이 사용하는 형식으로 변환하는 데 사용되는 /process/의 2개의 엔드포인트로 구성된다. 
/predict/ API로부터의 응답으로서 생존 확률(%)을 얻기 위해 사용된다.
```

### 응용 프로그램 실행 방법 1
- 두 부분 모두 도커로 컨테이너화되고 도커-콤포지를 통해 결합된다. 
- 앱을 실행하려면 레포(또는 도커-콤포지.yml 복사)를 복제하고 터미널에서 도커-콤포지를 실행하면 된다.

### 응용 프로그램 실행 방법 2
- api :cd api;uvicorn api:api --reload
- webapp : cd app;streamlit run app.py

----
# FORK FROM : https://github.com/tlary/fastapi_titanic

### Serving ML Models as Microservices - Streamlit, FastAPI, and Docker

This repo contains code for a small webapp to predict if passengers would have survived the Titanic disaster. The application consists of a frontend and a backend part and is used to demonstrate how to serve ML models as microservices through an API. The frontend is built with Streamlit and used to acquire passenger information from the user. The backend is built with the FastAPI framework and consists of 2 endpoints: `/preprocess/` used to preprocess the data and transform it into the format used by the model; `/predict/` to get the survival probability in percent as a response from the API. 

### How to run the Application

Both parts are containerized with Docker and combined via Docker-Compose. To run the app, simply clone the repo (or copy the docker-compose.yml) and run `docker-compose up` from the terminal. 





