# CC25k Dataset

The CC25k dataset consists of labeled citation contexts obtained through crowdsourcing. Each context is labeled by three independent workers. This README describes the structure and columns of the dataset.

## Dataset Description

The CC25k dataset is unique in its focus on **reproducibility-related sentiments** within scientific literature. This introduces a novel approach to studying computational reproducibility by leveraging citation contexts, which are textual fragments in scientific papers that reference prior work. This dataset comprises 25,829 labeled citation contexts, each annotated with one of three sentiment labels: positive, negative, or neutral. These labels reflect the cited work's perceived reusability or reproducibility. Unlike traditional sentiment or citation datasets, CC25k uniquely focuses on reproducibility-related signals. 
The dataset contains labeled contexts along with metadata about the workers, their labeling process, and the final aggregated labels. The columns in the dataset are detailed in the table below:  


| **Column Name**             | **Description**                                                                 |
|-----------------------------|-------------------------------------------------------------------------------|
| `input_index`               | Unique identifier for each input context.                                     |
| `input_context`             | Text or data snippet that workers are asked to label.                        |
| `input_file_key`            | Identifier or filename linking the context to a cited paper.                 |
| `input_first_author`        | Name or identifier of the first author of the cited paper.                   |
| `worker_id_w1`              | Unique ID of the first worker who labeled this context.                      |
| `work_time_in_seconds_w1`   | Time (in seconds) the first worker took to label the context.                |
| `worker_id_w2`              | Unique ID of the second worker who labeled this context.                     |
| `work_time_in_seconds_w2`   | Time (in seconds) the second worker took to label the context.               |
| `worker_id_w3`              | Unique ID of the third worker who labeled this context.                      |
| `work_time_in_seconds_w3`   | Time (in seconds) the third worker took to label the context.                |
| `label_w1`                  | Label assigned by the first worker.                                          |
| `label_w2`                  | Label assigned by the second worker.                                         |
| `label_w3`                  | Label assigned by the third worker.                                          |
| `batch`                     | Batch number for the posted Mechanical Turk job.                             |
| `majority_vote`             | Final label based on the majority vote among workers’ labels.                |
| `majority_agreement`        | Indicates how many of the three workers agreed on the final majority vote.   |


## GitHub Repository
The dataset and additional resources are available on GitHub:
https://github.com/lamps-lab/cc25k-citation-contexts-for-ai-reproducibility