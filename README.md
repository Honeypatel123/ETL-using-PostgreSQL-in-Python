# Fashion MNIST Image Storage in PostgreSQL Database

## Description
This repository contains code for storing Fashion MNIST dataset images in a PostgreSQL database. The Fashion MNIST dataset is a collection of 28x28 grayscale images of fashion items, such as shirts, pants, shoes, etc. This dataset is commonly used for training and testing machine learning models.

## Files
1. `fashion_mnist_to_postgres.py`: This Python script demonstrates how to load the Fashion MNIST dataset using Keras, preprocess the data, and store it in a PostgreSQL database.
2. `fashion_mnist.db`: This is the PostgreSQL database file where the images and their corresponding labels are stored.

## Dependencies
- Python 3.x
- TensorFlow (for loading the Fashion MNIST dataset)
- psycopg2 (Python library for connecting to PostgreSQL database)
- pandas (Python library for data manipulation and analysis)

## Usage
1. Make sure you have Python installed on your system.
2. Install the required dependencies using pip:
```
pip install tensorflow psycopg2 pandas
```
3. Ensure you have PostgreSQL installed and running on your system.
4. Update the database connection details (dbname, user, password, host, port) in the Python script (`fashion_mnist_to_postgres.py`) according to your PostgreSQL setup.
5. Run the Python script to execute the code:
```
python fashion_mnist_to_postgres.py
```

## Note
- This code assumes that you have already set up a PostgreSQL database named `fashion_mnist.db` with appropriate permissions.
- The Fashion MNIST dataset will be split into training and testing sets. Images and their corresponding labels will be stored in the `images` table within the database.
- The images are stored as binary data (`BYTEA` type) in the database.
- After executing the script, you can verify the data stored in the database by running a SELECT query on the `images` table.

