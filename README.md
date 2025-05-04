# FuzzyPromoEngine

Discount Recommendation System Using Fuzzy Logic

This system recommends discount levels to e-commerce customers using a **Fuzzy Logic Algorithm** with **trapezoidal membership functions**. The recommendation is based on two main input factors: Purchase Frequency and Total Spending.


Membership Function Categories

### 1. Purchase Frequency
| Category | Trapezoidal Range |
|----------|-------------------|
| Low      | [0, 0, 2, 4]       |
| Medium   | [3, 4, 6, 7]       |
| High     | [6, 8, 10, 10]     |

### 2. Total Spending (in IDR)
| Category | Trapezoidal Range                  |
|----------|------------------------------------|
| Low      | [0, 0, 500000, 1000000]            |
| Medium   | [750000, 1250000, 1750000, 2250000]|
| High     | [2000000, 2500000, 3000000, 3000000]|

### 3. Discount Output (in %)
| Category | Trapezoidal Range |
|----------|-------------------|
| Small    | [0, 0, 5, 10]     |
| Medium   | [8, 12, 18, 22]   |
| Large    | [20, 25, 30, 30]  |

---

## Implementation Steps

1. Use the `scikit-fuzzy` library and utilize the `control` module from it.
2. Declare input and output variables using `ctrl.Antecedent` and `ctrl.Consequent`.
3. Define trapezoidal membership functions for:
   - Purchase Frequency
   - Total Spending
   - Discount
4. Create fuzzy rules using `ctrl.Rule`.
5. Build the fuzzy control system using `ctrl.ControlSystem`.
6. Visualize membership functions using the `.view()` method.

---

## How It Works

The system applies fuzzy inference rules to determine an appropriate discount based on customer behavior. Trapezoidal membership functions allow for flexible and gradual interpretation of frequency and spending levels, resulting in a more personalized discount strategy.
