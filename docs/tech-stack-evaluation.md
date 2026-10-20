# Tech Stack Evaluation

## Project
Fuzzy Logic-Based Insulin Decision Support for Diabetes Management Using Meal Image Analysis

## Requirements that drive the decision
List 3 to 5 requirements from your own docs/requirements.md. Include at
least 2 non-functional requirements.
- [FR1]: The system shall allow users to upload a meal image in JPG, JPEG, or PNG format.
- [FR2]: The system shall identify food items from a predefined set of supported food categories in the uploaded image.
- [FR3]: The system shall display the estimated carbohydrate content of each recognized food item using a nutrition database.
- [FR4]: The system shall calculate and display the estimated total carbohydrate content of the recognized meal.
- [FR5]: The system shall process the available mealinformation using fuzzy logic rules and display the resulting decision-support category.

- [NFR1]: The system shall display the analysis result within 5 seconds for at least 95% of valid images submissions under the defined test environment.
- [NFR2]: The system shall allow first-time users to upload a meal image and view the result within 3 minutes without assistance.
- [NFR3]: The system shall reject unsupported image formats and files exceeding the specified upload size limit, displaying an appropriate error message.

## Options
- Option A: Python Flask + TensorFlow/Keras + scikit-fuzzy + SQLite
- Option B: Python Django + PyTorch + scikit-fuzzy + PostgreSQL
- Option C: Python StreamLit + TensorFlow/Keras + scikit-fuzzy + SQLite

## Decision matrix
Weight: how important the criterion is for YOUR project (1 = low, 5 = high).
Score: how well each option does (1 = poor, 5 = excellent).
Weighted score = weight x score. Add them up for each option.

| Criterion                          | Weight | A score | B score | C score |
|------------------------------------|--------|---------|---------|---------|
| Fits my requirements               |   5    |    5    |    5    |    4    |
| Skills I already have              |   4    |    4    |    2    |    4    |
| Time to build before my deadline   |   5    |    4    |    3    |    5    |
| Free hosting and tools             |   4    |    4    |    3    |    4    |
| Performance and security needs     |   3    |    4    |    5    |    3    |
| Room to grow later                 |   3    |    4    |    5    |    3    |
| **Total (weighted)**               |        |    83   |    76   |    77   |

## Decision record
- **Context:** My FYP is a web-based insulin decision-support system using meal image analysis and fuzzy logic. The system needs to recognise selected food items, estimate carbohydrate content, and provide fuzzy-logic-based decision support. I have limited development time, student-level programming skills, and a limited budget.
- **Decision:** Python Flask + TensorFlow/Keras + scikit-fuzzy + SQLite
- **Reasons:** 
1. Python supports the integration of meal image recognition, carbohydrate estimation, and fuzzy logic in one application, meeting my functional requirements.
2. Flask and SQLite are relatively lightweight, making the system easier to develop and test within my project deadline.
3. The required Python libraries are available for use without a paid license, supporting my cost requirements.
- **Consequences:** It will be easier to connect the image recognition, nutrition database, and fuzzy logic modules using Python. However, I will need to integrate and test each module carefully, and deploying the image recognition model may require additional configuration.
- **Risks and next review:** Image recognition may misidentify food items, causing inaccurate carbohydrate estimates and potentially misleading decision-support results. I will test the system using selected food images ans review its functionality and accuracy during development. If the model or hosting requirements are too difficult to manage, I will reconsider the implementation approach with my supervisor. The system will be an academic prototype, not a substitute for professional medical advice.
