### Download a dataset from the Hugging Face Hub

> https://huggingface.co/docs/hub/en/models-downloading

- Using Git

  ```bash
  pip install --upgrade huggingface-hub
  huggingface-cli login
  git lfs install
  git clone https://huggingface.co/datasets/JourneyDB/JourneyDB
  ```

- Using Hugging Face Cli

  ```bash
  huggingface-cli login
  huggingface-cli download --repo-type dataset JourneyDB/JourneyDB
  ```

- Code

  ```
    pip install datasets
  ```

  ```python
  from datasets import load_dataset

  # Download JourneyDB dataset
  dataset = load_dataset("JourneyDB/JourneyDB")

  # To see the first few examples
  print(dataset['train'][:5])
  ```

- Faster downloads

  > https://huggingface.co/docs/huggingface_hub/v0.27.0/package_reference/environment_variables#hfhubenablehftransfer
