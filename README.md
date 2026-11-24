# FairFareAI: An Intelligent Ride Service Recommendation and Fair Surge-Pricing Framework

https://github.com/user-attachments/assets/2e5f428d-db72-41cf-9d91-aeeea46b3476

## 1. Overview

FairFareAI is an intelligent, data-driven ride service recommendation framework designed to improve transparency in dynamic ride pricing while addressing the ethical implications of surge pricing under exceptional circumstances.

The framework addresses two fundamental challenges associated with contemporary ride-hailing platforms:

### 1.1 Ride Fare Transparency and Informed Decision-Making

Existing ride-hailing services often provide limited insight into the underlying components of a fare, including estimated cost per kilometre, dynamic pricing adjustments, and the influence of demand and traffic conditions on the final booking price. This lack of transparency can make it difficult for commuters to evaluate available transportation options and determine the most cost-effective time to travel.

FairFareAI aims to address this limitation by modelling ride fares, predicting potential surge-pricing conditions, and providing users with insights into estimated travel costs and timings. By presenting these predictions, the framework seeks to empower commuters to make more informed decisions regarding their transportation choices.

### 1.2 Ethical Surge Pricing During Emergencies

Dynamic pricing mechanisms are generally designed to balance supply and demand. However, their application during emergencies raises important ethical and societal concerns.

Consider situations involving medical emergencies, natural disasters, or large-scale evacuations. Under such circumstances, transportation may become a necessity rather than a matter of convenience. Imposing substantially increased fares on individuals seeking emergency transportation raises concerns about accessibility, fairness, and the ethical responsibility of service providers.

FairFareAI explores an approach to identifying such circumstances through predictive modelling and contextual classification. Based on predicted pricing conditions and the nature of the ride, the framework aims to determine whether surge pricing should be permitted or subject to restrictions or predefined caps.

The underlying objective is to explore a more equitable approach to dynamic ride pricing, in which commercial pricing mechanisms can be balanced against public welfare and emergency transportation requirements.

---

## 2. Research Challenges and Dataset Development

One of the primary challenges encountered during the development of FairFareAI was the absence of a publicly available dataset that adequately represented the geographical, operational, and pricing characteristics required for the proposed framework.

To address this limitation, a synthetic dataset was developed using information obtained from publicly accessible sources. The dataset was designed to approximate the characteristics of an urban ride-hailing environment, with Bengaluru, India, serving as the geographical reference.

The dataset development process incorporated information from the following sources:

- **Geographical and Administrative Data:** Publicly available government datasets, particularly those accessible through the Government of Karnataka's Open Data Portal ([Karnataka Open Data Portal](https://karnataka.data.gov.in/)), were used to represent Bengaluru's 225 municipal wards and their associated geographical locations.

- **Ride Pricing Information:** Uber's publicly accessible Bengaluru service information ([Uber – Bengaluru](https://www.uber.com/global/en/r/cities/bangalore-south-karnataka-in/)) was examined to understand the general structure and components involved in ride fare estimation.

Since the resulting dataset was synthetically generated, controlled randomness and variability were incorporated into the data generation process. This was intended to avoid an overly idealised dataset and introduce variations that more closely resemble the uncertainty associated with real-world transportation and dynamic pricing environments.

The resulting dataset provided the experimental foundation for training and evaluating the predictive models.

---

## 3. Model Evaluation and Experimental Results

Multiple machine learning regression models were evaluated to identify an appropriate approach for predicting ride pricing. Model performance was assessed using two principal evaluation metrics:

- **Mean Squared Error (MSE):** Measures the average squared difference between predicted and actual target values. A lower MSE indicates better predictive accuracy, with larger prediction errors receiving greater penalties.

- **Coefficient of Determination (R²):** Measures the proportion of variance in the target variable explained by the regression model. Values closer to 1 indicate a stronger fit between the model's predictions and the observed values.

The comparative evaluation demonstrated that the **Random Forest Regressor achieved the lowest MSE of 10.99** among the evaluated models, indicating the strongest performance in terms of the selected error metric.

The R² evaluation further provided insight into how effectively the individual models captured variations in the target variable. Together, these metrics enabled a comparative assessment of predictive accuracy and model explanatory performance.

The experimental results are illustrated in the following figures.

<table align="center">
  <tr>
    <td align="center" width="50%">
      <img
        src="https://github.com/user-attachments/assets/495053fe-286b-4bb5-98c1-81c2c65e379f"
        width="100%"
        alt="Comparative MSE evaluation of regression models"
      />
    </td>
    <td align="center" width="50%">
      <img
        src="https://github.com/user-attachments/assets/93c6ffd8-3312-45c1-afd4-7260c8501682"
        width="100%"
        alt="Comparative R-squared evaluation of regression models"
      />
    </td>
  </tr>
</table>

<p align="center">
  <em>Figures 2 and 3. Comparative evaluation of regression models using (left) Mean Squared Error (MSE) and (right) the Coefficient of Determination (R²).</em>
</p>

Based on the comparative evaluation, the Random Forest Regressor was identified as the best-performing model among those considered, based on its achieved MSE.

---

## 4. Research Contribution and Future Direction

FairFareAI explores the intersection of machine learning-based transportation analytics, consumer-oriented fare transparency, and ethical dynamic pricing.

Its primary contribution lies in investigating how predictive modelling can be extended beyond conventional fare estimation to support more socially responsible pricing decisions.

By combining ride fare prediction with contextual surge-pricing classification, the framework seeks to establish a foundation for transportation recommendation systems that account for both economic efficiency and equitable access to mobility.

Ultimately, FairFareAI aims to demonstrate how data-driven decision-making can contribute to more transparent, accessible, and ethically informed ride-hailing services, particularly in urban transportation environments.

---

## 5. Research Publication and Citation

The research associated with FairFareAI was published as a book chapter in Springer's *Lecture Notes in Networks and Systems* series.

**Publication Details**

- **Title:** Data-Driven Insights for Intelligent Ride Service Recommendations with FairFareAI on Indian Road
- **Authors:** M. Robinson, S. George, S. M. Raju, D. K. Sony, T. Kattampally, and A. Tripathi
- **Conference:** International Conference on Computational Intelligence (ICCI 2025)
- **Series:** Lecture Notes in Networks and Systems
- **Volume:** 2063
- **Publisher:** Springer, Cham
- **Publication Date:** 02 August 2026
- **DOI:** [10.1007/978-3-032-31523-6_18](https://doi.org/10.1007/978-3-032-31523-6_18)

### BibTeX Citation

```bibtex
@incollection{robinson2026fairfareai,
  title={Data-Driven Insights for Intelligent Ride Service Recommendations with FairFareAI on Indian Road},
  author={Robinson, M. and George, S. and Raju, S. M. and Sony, D. K. and Kattampally, T. and Tripathi, A.},
  booktitle={Proceedings of International Conference on Computational Intelligence},
  editor={Saraswat, M. and Tiwari, R. and Pavone, M. F. and Patel, S. J.},
  series={Lecture Notes in Networks and Systems},
  volume={2063},
  publisher={Springer, Cham},
  year={2026},
  doi={10.1007/978-3-032-31523-6_18}
}
```

**DOI:** https://doi.org/10.1007/978-3-032-31523-6_18
