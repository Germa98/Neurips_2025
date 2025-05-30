This repository contains the code, results, and trained models obtained with our experiments.

- The content is organized **first by task type**, with two top-level folders:
  - `classification_tasks/`
  - `segmentation_tasks/`
- Within each of these, the content is organized **by dataset**. Each dataset folder corresponds to a specific dataset used in our experiments.
- Inside each dataset folder, **subfolders for network architectures** are created **only if multiple architectures have been used**.
- If multiple experiments have been conducted with the same dataset and network, each experiment is placed in a **separate subfolder named with an `idx` identifier**.

Each experiment folder includes:
  - A `results.json` file summarizing the outcomes of the experiment.
  - The **trained models** obtained using:
    - Our methodology
    - The FedProx approach

## Folder Structure Example

```plaintext
classification_tasks/
  code.py
  <dataset>/
    <dataset_network>/                 # (optional, only if multiple networks have been used)
      dataset_network_0/              # (optional, only if multiple experiments have been performed)
        results.json
        model_ours.pt
        model_fedprox.pt
      dataset_network_1/
        results.json
        model_ours.pt
        model_fedprox.pt

- `results.json`: Contains the evaluation metrics and configuration used for the experiment.
- `model_ours.pt`: Trained model using our custom approach.
- `model_fedprox.pt`: Trained model using the FedProx method.
