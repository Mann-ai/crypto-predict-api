from flask import Flask, jsonify
import random

app = Flask(__name__)

@app.route('/predict', methods=['GET'])
def predict():
    prediction = random.choice(["UP", "DOWN"])  # Future me AI Model laga sakte ho
    return jsonify({"prediction": prediction})

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000)
