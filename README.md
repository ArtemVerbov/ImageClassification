# Knowledge Distillation For Image Classification 

```
The following repository contains knowledge distillation code example for image classification task

All experiments are tracked with clearml: https://clear.ml/docs/latest/docs/

Environment created with poetry: https://python-poetry.org/docs/

To install dependeces: poetry install
To run training: 
1. Student model: poetry run python3.11 -m src.train lightning_module=student_model
2. Teacher model: poetry run python3.11 -m src.train lightning_module=teacher_model
3. Knowledge distillation: poetry run python3.11 -m src.train   
```

1. Setup ClearML: clearml-init

2. Migrate dataset to ClearML: make migrate_dataset

3. To download teacher model weights: make download_weights

## Models Accuracy:

| Model            | Test Set Accuracy % |
|------------------|---------------------|
| Teacher          | 91                  |
| Student          | 86                  |
| Student with KD  | 88                  |

## Model Training Results:
Teacher: https://app.clear.ml/projects/27f17385bf22464fa816703a1659f67f/experiments/2867f03e68a64cddabef62b9779c8ebc/output/execution

Student: https://app.clear.ml/projects/27f17385bf22464fa816703a1659f67f/experiments/142f53eb005d47c69497e56fc85a64fe/output/execution

KD: https://app.clear.ml/projects/27f17385bf22464fa816703a1659f67f/experiments/9015bb59e7e940c5849557596cdf730a/output/execution

## Test Data Confusion Matrix

### Teacher
![alt text](https://github.com/ArtemVerbov/Knowledge-Distillation-X-Lightning/blob/main/media/teacher_result.jpeg?raw=true)

### Student
![alt text](https://github.com/ArtemVerbov/Knowledge-Distillation-X-Lightning/blob/main/media/student_result.jpeg?raw=true)

### Knowledge Distillation
![alt text](https://github.com/ArtemVerbov/Knowledge-Distillation-X-Lightning/blob/main/media/KD_result.jpeg?raw=true)
