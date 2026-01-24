# Experiment Specification
## Impact of Activation Functions on Stability and Generalization

### 1. Research Objective
The objective of this study is to experimentally evaluate how the choice of activation
function affects:
- training stability
- gradient propagation
- generalization performance
- robustness to noise
- performance on time series data

The study focuses on controlled experiments where the activation function is the
only varying component.

---

### 2. Research Hypotheses
#### H1: ReLU leads to faster convergence but exhibits higher training instability under noisy conditions.
#### H2: Tanh results in more stable training dynamics, at the cost of slower convergence.
#### H3: Activation saturation negatively affects generalization performance, particularly in the presence of noise.
#### H4: The impact of activation choice is more pronounced in time series settings than in i.i.d. data.

---

### 3. Datasets

#### 3.1 i.i.d. Dataset
- Synthetic two-moons dataset
- Binary classification
- Non-linearly separable
- Baseline and noisy versions (Gaussian noise + outliers)

#### 3.2 Time Series Dataset
- Simulated financial log-returns
- Zero-mean Gaussian distribution
- Controlled noise levels
- Supervised learning setup (next-step prediction)

---

### 4. Model Architecture
- Multilayer Perceptron (MLP)
- Fixed architecture across experiments
- Number of layers: fixed
- Number of hidden units: fixed
- Optimizer: Adam
- Learning rate: fixed
- Batch size: fixed
- Number of epochs: fixed
- Multiple random seeds per experiment

The only varying component is the activation function.

---

### 5. Activation Functions
- ReLU
- Tanh
- Sigmoid

---

### 6. Evaluation Metrics

#### 6.1 Training Dynamics
- Training loss vs epochs
- Convergence speed
- Gradient norm per layer

#### 6.2 Generalization
- Test accuracy (classification)
- Test MSE (time series)

#### 6.3 Stability
- Variance across random seeds
- Sensitivity to noise

---

### 7. Experimental Constraints
- No hyperparameter tuning per activation
- Identical initialization schemes
- Identical training protocol

---

### 8. Expected Outcomes
This study aims to identify systematic behaviors rather than absolute performance
winners, with particular focus on stability and robustness patterns.


