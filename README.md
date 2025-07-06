# eidolon-project
It's a versatile, modular AI system designed to learn, adapt, and interact in meaningful ways.

Completion is the chat log for first conversation. After is the Eidolon's Evolution and Moral Flexibility, then AI limitations in creating, finally USER_7A3F.

1. cradle/memory_system.py
markdown
Copy
## Code Overview: `memory_system.py`

### Purpose
Manages persistent memory for **Eidolon**, allowing it to store and retrieve interactions.

### Key Components
- `MemorySystem`: Handles adding, retrieving, and saving interactions.
- `add_interaction`: Adds a new interaction to memory.
- `retrieve_relevant_memory`: Retrieves interactions based on a query and context.
- `save_memory` and `load_memory`: Save and load memory to/from a file.

### Workflow
1. Add interactions using `add_interaction`.
2. Retrieve relevant interactions using `retrieve_relevant_memory`.
3. Save and load memory for persistence.

### Dependencies
- `json`
- `os`
- `datetime`

### Usage
```python
memory_system = MemorySystem()
memory_system.add_interaction("What is 2 + 2?", "2 + 2 is 4.", "math")
relevant_memory = memory_system.retrieve_relevant_memory("2 + 2", "math")
Copy

---

### **2. `code/basic_network.py`**
```markdown
## Code Overview: `basic_network.py`

### Purpose
Implements a basic feedforward neural network for simple tasks.

### Key Components
- `create_basic_network`: Defines the neural network architecture.
- Input layer, hidden layer, and output layer.

### Workflow
1. Define the network architecture.
2. Compile the model with an optimizer and loss function.
3. Train the model on data.

### Dependencies
- `tensorflow`
- `tensorflow.keras`

### Usage
```python
model = create_basic_network(input_shape=(100,), hidden_units=64, output_units=10)
model.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])
model.fit(X_train, y_train, epochs=10)
Copy

---

### **3. `code/train_model.py`**
```markdown
## Code Overview: `train_model.py`

### Purpose
Trains the basic neural network or transformer model on a dataset.

### Key Components
- `train_model`: Handles data loading, preprocessing, and training.
- `save_model`: Saves the trained model weights and architecture.

### Workflow
1. Load and preprocess the dataset.
2. Train the model.
3. Save the trained model.

### Dependencies
- `tensorflow`
- `numpy`
- `transformers` (for transformer models)

### Usage
```bash
python train_model.py
Copy

---

### **4. `code/transformer.py`**
```markdown
## Code Overview: `transformer.py`

### Purpose
Implements a transformer model for natural language tasks.

### Key Components
- `TransformerModel`: Handles loading, generating text, and saving/loading the model.
- `generate_text`: Generates text based on a prompt.

### Workflow
1. Load a pre-trained or fine-tuned transformer model.
2. Generate text using `generate_text`.
3. Save and load the model for reuse.

### Dependencies
- `transformers`
- `tensorflow`

### Usage
```python
transformer = TransformerModel(model_name='gpt2')
output = transformer.generate_text("What is 2 + 2?")
Copy

---

### **5. `code/fine_tune.py`**
```markdown
## Code Overview: `fine_tune.py`

### Purpose
Fine-tunes a pre-trained transformer model on a custom dataset.

### Key Components
- `FineTuner`: Handles dataset loading, preprocessing, and fine-tuning.
- `fine_tune`: Fine-tunes the model on the dataset.
- `save_model`: Saves the fine-tuned model.

### Workflow
1. Load and preprocess the dataset.
2. Fine-tune the model.
3. Save the fine-tuned model.

### Dependencies
- `transformers`
- `tensorflow`
- `scikit-learn`

### Usage
```bash
python fine_tune.py
Copy

---

### **6. `code/evaluation.py`**
```markdown
## Code Overview: `evaluation.py`

### Purpose
Evaluates the performance of **Eidolon** using metrics like accuracy, perplexity, and BLEU score.

### Key Components
- `Evaluator`: Handles loading the model, preprocessing test data, and computing metrics.
- `evaluate_accuracy`, `evaluate_perplexity`, `evaluate_bleu`: Compute evaluation metrics.

### Workflow
1. Load the model and test dataset.
2. Preprocess the test data.
3. Compute evaluation metrics.

### Dependencies
- `transformers`
- `tensorflow`
- `nltk`
- `scikit-learn`

### Usage
```bash
python evaluation.py
Copy

---

### **7. `ui/web_ui.py`**
```markdown
## Code Overview: `web_ui.py`

### Purpose
Provides a chat-based interface for interacting with **Eidolon**.

### Key Components
- Chat interface: Allows users to chat with **Eidolon**.
- Sidebar: Allows users to teach **Eidolon** new interactions.

### Workflow
1. Start the chat interface.
2. Interact with **Eidolon** in the chat window.
3. Teach **Eidolon** new concepts using the sidebar.

### Dependencies
- `streamlit`
- `transformers`
- `cradle.memory_system`

### Usage
```bash
streamlit run ui/web_ui.py
Copy
