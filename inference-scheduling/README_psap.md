# Changes made

- Added [ms_values.yaml] as an individual values file, this will override any value from [ms-inference-scheduling/values.yaml]

- Added a new helm chart to download a model from huggingface into a PVC.  This currently uses Helm Hooks, which can lead to timeouts given a large model or slow connection.
	- A PR will be made in the modelservices helm chart to define initContainers

- Model can be selected using `MODEL` enviornment variable and specifying HuggingFace ID. (Default is `MODEL=Qwen/Qwen3-0.6B`)

- This does _NOT_ set up the model PVC, currently this is required to be done manually.
