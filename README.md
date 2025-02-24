Link to the Video:https://youtu.be/x_SpS7HNBbI

**Problem Statement:**  
The project aims to predict student outcomes such as dropout, graduation, and performance based on a variety of factors, including application details, parental education, financial status, and economic indicators. The challenge lies in processing and analyzing this complex dataset to identify patterns that influence student success. Accurate predictions can help in targeted interventions to support students in need, thus improving educational outcomes.

**Dataset Used:**  
I used a dataset from Kargal that includes features like marital status, application mode, course, parental qualifications, financial standing, and various economic indicators like unemployment rate and GDP. These attributes are used to predict whether a student will drop out, graduate, or be classified as a graduate based on various socio-economic factors and educational backgrounds.# Machine Learning Model Training and Results

## Training Instances

### Instance 1: Default Neural Network (No optimizer/regularizer defined)
| **Training Instance** | **Optimizer** | **Regularizer** | **Epochs** | **Early Stopping** | **Layers** | **Learning Rate** | **Accuracy** | **F1-Score** | **Precision** | **Recall** |
|-----------------------|---------------|-----------------|------------|--------------------|------------|-------------------|--------------|--------------|----------------|------------|
| Instance 1            | Default (SGD) | None            | 50         | No                 | 2          | Default           | 0.8904       | 0.6997       | 0.6570         | 0.7483     |

### Instance 2: Neural Network with Adam Optimizer, L2 Regularization
| **Training Instance** | **Optimizer** | **Regularizer** | **Epochs** | **Early Stopping** | **Layers** | **Learning Rate** | **Accuracy** | **F1-Score** | **Precision** | **Recall** |
|-----------------------|---------------|-----------------|------------|--------------------|------------|-------------------|--------------|--------------|----------------|------------|
| Instance 2            | Adam          | L2              | 50         | No                 | 2          | 0.001             | 0.8836       | 0.6645       | 0.6538         | 0.6755     |

### Instance 3: Neural Network with RMSprop Optimizer, Dropout Regularization
| **Training Instance** | **Optimizer** | **Regularizer** | **Epochs** | **Early Stopping** | **Layers** | **Learning Rate** | **Accuracy** | **F1-Score** | **Precision** | **Recall** |
|-----------------------|---------------|-----------------|------------|--------------------|------------|-------------------|--------------|--------------|----------------|------------|
| Instance 3            | RMSprop       | None            | 50         | No                 | 2          | 0.001             | 0.8667       | 0.6289       | 0.5988         | 0.6623     |

### Instance 4: Neural Network with Adam Optimizer, L2 Regularization, Early Stopping
| **Training Instance** | **Optimizer** | **Regularizer** | **Epochs** | **Early Stopping** | **Layers** | **Learning Rate** | **Accuracy** | **F1-Score** | **Precision** | **Recall** |
|-----------------------|---------------|-----------------|------------|--------------------|------------|-------------------|--------------|--------------|----------------|------------|
| Instance 4            | Adam          | L2              | 50         | Yes                | 2          | 0.001             | 0.8497       | 0.5908       | 0.5517         | 0.6358     |

### Instance 5 (Optional): Neural Network with Adam Optimizer, L2 Regularization, Dropout, Early Stopping
| **Training Instance** | **Optimizer** | **Regularizer** | **Epochs** | **Early Stopping** | **Layers** | **Learning Rate** | **Accuracy** | **F1-Score** | **Precision** | **Recall** |
|-----------------------|---------------|-----------------|------------|--------------------|------------|-------------------|--------------|--------------|----------------|------------|
| Instance 5            | Adam          | L2              | 50         | Yes                | 3          | 0.001             | 0.8746       | 0.6454       | 0.6235         | 0.6689     |

---

## Summary of Results
### Best Model
- The best-performing model was **Instance 1 (Default Neural Network)** with an **accuracy of 0.8904**, which outperformed other configurations in terms of **Accuracy** and **F1-Score**.

### Comparison Between Neural Networks and ML Algorithms
- **Neural Networks** (especially the default model) achieved higher accuracy compared to **Traditional ML Algorithms** (Logistic Regression, SVM, Decision Tree).
- **Logistic Regression** and **SVM** performed relatively well with accuracy around 0.88, but the **Neural Network** showed stronger performance for the dataset, particularly in **Recall** and **Precision**.

---

## Model Comparison:
| **Model**                  | **Accuracy** | **Precision** | **Recall** | **F1-Score** |
|----------------------------|--------------|---------------|------------|--------------|
| **Simple NN**              | 0.8904       | 0.6570        | 0.7483     | 0.6997       |
| **NN with L2 Regularization** | 0.8836    | 0.6538        | 0.6755     | 0.6645       |
| **NN with Dropout**        | 0.8667       | 0.5988        | 0.6623     | 0.6289       |
| **NN with Early Stopping** | 0.8497       | 0.5517        | 0.6358     | 0.5908       |
| **NN with L2 + Dropout + Early Stopping** | 0.8746 | 0.6235  | 0.6689     | 0.6454       |
| **Logistic Regression**    | 0.8802       | 0.6380        | 0.6887     | 0.6624       |
| **SVM**                    | 0.8791       | 0.6170        | 0.7682     | 0.6844       |
| **Decision Tree**          | 0.8633       | 0.5615        | 0.9073     | 0.6937       |


