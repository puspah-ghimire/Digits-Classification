# **Handwritten digit classification using TensorFlow v1.13.1**
We use TensorFlow to build a neural network to recognize handwritten
digits. The MNIST dataset has been called the hello world
of deep learning. It consists of 55,000 data points of handwritten digits (0 to
9).
In this section, we see how we can use our neural network to recognize
these handwritten digits, get the hang of TensorFlow and
TensorBoard.

---
# **MNIST digit classification using TensorFlow 2.0.0**

We see how we can perform MNIST handwritten digits
classification, using TensorFlow 2.0.0. It requires only a few lines of code
compared to TensorFlow 1.x. TensorFlow 2.0 uses
Keras which is a high-level library, meaning that it does
not perform any low-level operations on its own, such as convolution. The Keras API is
available in tf.keras, and TensorFlow 2.0 uses it as the primary API.

---

# **TensorFlow Virtual Environments (`tf1_env` & `tf2_env`)**

These are step-by-step instructions for setting up and managing two separate Conda environments for TensorFlow:
- **`tf1_env`** for TensorFlow 1.13.1
- **`tf2_env`** for TensorFlow 2.0.0

## **1. Prerequisites**
Before proceeding, ensure that you have Anaconda installed on your system. If Anaconda is not installed, download and install it from:

[Anaconda Official Website](https://www.anaconda.com/products/distribution)

To verify Anaconda installation, run:
```sh
conda --version
```
You should see an output like:
```
conda 24.11.3  # (or any other installed version)
```

---

## **2. Creating the Virtual Environments**
It is recommended to create separate environments for different TensorFlow versions to avoid dependency conflicts.

### **Create TensorFlow 1.x Environment (`tf1_env`)**
```sh
conda create --name tf1_env python=3.7
```
TensorFlow 1.x works with Python 3.7, so we specify it explicitly.

### **Create TensorFlow 2.x Environment (`tf2_env`)**
```sh
conda create --name tf2_env python=3.8
```
TensorFlow 2.x supports Python 3.7 or newer.

---

## **3. Activate the Environment**
Before installing TensorFlow, activate the respective environment.

### **Activate `tf1_env`**
```sh
conda activate tf1_env
```

### **Activate `tf2_env`**
```sh
conda activate tf2_env
```

---

## **4. Install TensorFlow**
Once the environment is activated, install the appropriate TensorFlow version.

### **Install TensorFlow 1.x in `tf1_env`**
```sh
pip install tensorflow==1.13.1
```

### **Install TensorFlow 2.x in `tf2_env`**
```sh
pip install tensorflow==2.0.0
```

To verify the installation:
```sh
python -c "import tensorflow as tf; print(tf.__version__)"
```

---

## **5. Install Jupyter & IPython Kernel**
To use these environments in Jupyter Notebook, install Jupyter and IPython kernel inside each environment.

### **Install Jupyter & IPython Kernel in `tf1_env`**
```sh
pip install jupyter ipykernel
python -m ipykernel install --user --name=tf1_env --display-name "Python (tf1_env)"
```

### **Install Jupyter & IPython Kernel in `tf2_env`**
```sh
pip install jupyter ipykernel
python -m ipykernel install --user --name=tf2_env --display-name "Python (tf2_env)"
```

---


## **6. Running Jupyter Lab**
To launch Jupyter Lab, use:
```sh
jupyter lab
```
Select **"Kernel" → "Change Kernel"**, and/or choose either `Python (tf1_env)` or `Python (tf2_env)` based on your requirements.

---

## **7. Troubleshooting**

### **Issue: Protobuf Version Mismatch**
- If you encounter:
  ```
  TypeError: Descriptors cannot not be created directly.
  ```
  Run:
  ```sh
  pip install protobuf==3.20.*
  ```

---

