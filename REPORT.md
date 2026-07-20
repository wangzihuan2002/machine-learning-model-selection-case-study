# Machine Learning Applications: Housing and Autonomous Transportation

## Decision Context

Machine learning projects should begin with the problem, data, and decision environment—not with a preferred algorithm. This report compares a traditional machine learning regression problem with a deep learning perception problem and explains why each requires a different technical approach.

## 1. Traditional Machine Learning: California House-Price Prediction

During a previous internship, I worked on a California house-price prediction project. The objective was to estimate market value from structured property and neighborhood information such as location, square footage, room counts, property age, and local market characteristics.

Traditional supervised machine learning is suitable because the available information can be represented as tabular features with a continuous target. Regression models, random forests, and gradient-boosted trees can learn relationships between property attributes and historical prices. These approaches also support practical baselines, efficient experimentation, and clearer explanations for real-estate professionals and clients.

Deep learning would not be the first choice for the structured-data baseline. It generally introduces greater requirements for training data, computing resources, hyperparameter tuning, and model governance. It can also make individual predictions harder to explain. The additional complexity is difficult to justify unless evaluation demonstrates a meaningful improvement.

The decision would change if the product incorporated photographs, satellite imagery, floor plans, or large volumes of listing descriptions. Those unstructured and multimodal inputs could justify deep representation learning, potentially combined with a traditional tabular model.

## 2. Deep Learning: Autonomous Taxis

Autonomous taxis provide a real-world deep learning application because a vehicle must interpret continuous, high-dimensional information about pedestrians, vehicles, signals, lanes, and obstacles. Waymo publicly describes a sensor suite that includes lidar, cameras, radar, and an AI compute platform. The resulting system must determine where the vehicle is, what surrounds it, what may happen next, and how it should respond.

Deep learning is suitable for perception and prediction because neural networks can learn visual and spatial representations directly from large datasets. They support tasks such as object detection, semantic segmentation, motion forecasting, and sensor fusion, all of which are difficult to solve through manually engineered rules alone.

Traditional machine learning is not sufficient for the complete perception problem. A conventional model may work well for a narrow, structured task such as travel-time prediction or fleet-demand forecasting, but it cannot by itself understand raw images and complex road scenes. The distinction is important: deep learning is necessary for central perception capabilities, while traditional methods may still add value elsewhere in the platform.

Deep learning also introduces significant risks. Predictions can be difficult to explain, training data may underrepresent unusual situations, and an error can affect human safety. A deployable autonomous-driving system therefore requires more than a trained network: it needs simulation, scenario-based testing, redundant sensors, independent safety controls, monitoring, and disciplined release management.

## Conclusion

The most advanced model is not automatically the most appropriate model. Traditional machine learning is a practical and explainable choice for structured house-price prediction. Deep learning is more appropriate for the complex sensory perception required by autonomous taxis. The final decision should reflect the data modality, business objective, acceptable error, explainability needs, available resources, and consequences of failure.

## References

1. scikit-learn developers. “California Housing dataset.” https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_california_housing.html
2. Waymo. “Frequently Asked Questions.” https://waymo.com/faq/
3. Waymo. “Autonomous Driving Technology.” https://waymo.com/about/
