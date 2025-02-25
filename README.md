# MTW-NPCI-Doom
Developing an innovative AI/ML solution to identify frauds on UPI scale of data

## Project Structure

```bash
upi-fraud-detection/
├── backend/
│   ├── app/
│   │   ├── api/
│   │   │   ├── api_v1/
│   │   │   │   ├── endpoints/
│   │   │   │   │   ├── __init__.py
│   │   │   │   │   ├── alerts.py
│   │   │   │   │   ├── auth.py
│   │   │   │   │   ├── transactions.py
│   │   │   │   ├── __init__.py
│   │   │   │   ├── api.py
│   │   │   ├── __init__.py
│   │   ├── core/
│   │   │   ├── __init__.py
│   │   │   ├── config.py
│   │   │   ├── security.py
│   │   ├── models/
│   │   │   ├── __init__.py
│   │   │   ├── alert.py
│   │   │   ├── transaction.py
│   │   │   ├── user.py
│   │   ├── schemas/
│   │   │   ├── __init__.py
│   │   │   ├── alert.py
│   │   │   ├── token.py
│   │   │   ├── transaction.py
│   │   │   ├── user.py
│   │   ├── services/
│   │   │   ├── __init__.py
│   │   │   ├── alert_service.py
│   │   │   ├── transaction_service.py
│   │   │   ├── user_service.py
│   │   ├── utils/
│   │   │   ├── __init__.py
│   │   │   ├── fraud_features.py
│   │   │   ├── notification.py
│   │   ├── __init__.py
│   │   ├── main.py
│   ├── tests/
│   │   ├── __init__.py
│   │   ├── conftest.py
│   │   ├── test_api.py
│   │   ├── test_services.py
│   ├── venv/
│   ├── .env
│   ├── .gitignore
│   ├── README.md
│   ├── requirements.txt
├── frontend/
│   ├── public/
│   │   ├── favicon.ico
│   │   ├── robots.txt
│   ├── src/
│   │   ├── components/
│   │   │   ├── common/
│   │   │   │   ├── Button.jsx
│   │   │   │   ├── Card.jsx
│   │   │   │   ├── Input.jsx
│   │   │   │   ├── Loading.jsx
│   │   │   ├── dashboard/
│   │   │   │   ├── AlertsTable.jsx
│   │   │   │   ├── FraudMetricsCard.jsx
│   │   │   │   ├── RecentTransactions.jsx
│   │   │   │   ├── TransactionChart.jsx
│   │   │   │   ├── TransactionForm.jsx
│   │   │   ├── layout/
│   │   │   │   ├── Footer.jsx
│   │   │   │   ├── Navbar.jsx
│   │   │   │   ├── Sidebar.jsx
│   │   ├── pages/
│   │   │   ├── auth/
│   │   │   │   ├── Login.jsx
│   │   │   │   ├── Register.jsx
│   │   │   ├── dashboard/
│   │   │   │   ├── Dashboard.jsx
│   │   │   │   ├── Alerts.jsx
│   │   │   │   ├── Transactions.jsx
│   │   │   ├── Home.jsx
│   │   │   ├── NotFound.jsx
│   │   ├── redux/
│   │   │   ├── features/
│   │   │   │   ├── alertSlice.js
│   │   │   │   ├── authSlice.js
│   │   │   │   ├── transactionSlice.js
│   │   │   ├── store.js
│   │   ├── utils/
│   │   │   ├── api.js
│   │   │   ├── auth.js
│   │   │   ├── constants.js
│   │   │   ├── helpers.js
│   │   ├── App.jsx
│   │   ├── index.css
│   │   ├── main.jsx
│   │   ├── routes.jsx
│   ├── .gitignore
│   ├── index.html
│   ├── package.json
│   ├── tailwind.config.js
│   ├── vite.config.js
├── kafka-streaming/
│   ├── config/
│   │   ├── kafka_config.py
│   ├── consumers/
│   │   ├── fraud_detection_consumer.py
│   │   ├── transaction_consumer.py
│   ├── producers/
│   │   ├── alert_producer.py
│   │   ├── transaction_producer.py
│   ├── requirements.txt
│   ├── run_consumers.py
│   ├── run_producers.py
├── ml-models/
│   ├── data/
│   │   ├── processed/
│   │   ├── raw/
│   │   │   ├── transactions.csv
│   ├── models/
│   │   ├── fraud_detection_model.pkl
│   │   ├── model_metrics.json
│   ├── notebooks/
│   │   ├── exploratory_analysis.ipynb
│   │   ├── model_training.ipynb
│   ├── src/
│   │   ├── features/
│   │   │   ├── build_features.py
│   │   ├── models/
│   │   │   ├── predict_model.py
│   │   │   ├── train_model.py
│   │   ├── utils/
│   │   │   ├── data_utils.py
│   │   │   ├── evaluation.py
│   ├── requirements.txt
│   ├── train.py
│   ├── predict.py
│   ├── retrain.py
├── database/
│   ├── migrations/
│   │   ├── postgres/
│   │   │   ├── 001_create_tables.sql
│   │   ├── mongodb/
│   │   │   ├── init_collections.js
│   ├── init_postgres.sh
│   ├── init_mongodb.sh
│   ├── README.md
├── k8s/
│   ├── backend-deployment.yaml
│   ├── frontend-deployment.yaml
│   ├── kafka-deployment.yaml
│   ├── ml-deployment.yaml
│   ├── mongodb-deployment.yaml
│   ├── postgres-deployment.yaml
│   ├── ingress.yaml
│   ├── service-mesh.yaml
├── docker/
│   ├── backend/
│   │   ├── Dockerfile
│   ├── frontend/
│   │   ├── Dockerfile
│   ├── kafka-streaming/
│   │   ├── Dockerfile
│   ├── ml-models/
│   │   ├── Dockerfile
├── docker-compose.yml
├── .gitignore
├── README.md
