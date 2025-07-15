# OPTIMIZATION-MODEL

COMPANY : CODTECH IT SOLUTIONS 
NAME : AMOL SHIVAJI KADAM 
INTERN ID : CT08DN391 
DOMAIN : DATA SCIENCE 
DURARION : 8 WEEKS 
MENTOR : NEELA SANTOSH

# Description

In this project, I developed a complete supply chain optimization model using Linear Programming (LP) to allocate the production and distribution of products efficiently. The model was implemented in Python using the PuLP library, which is a powerful open-source optimization tool. The project addresses a practical problem of minimizing the total shipping cost from multiple factories to different regional markets, while fulfilling demand and adhering to factory constraints.
# Objective
The primary objective of this work was to minimize the overall transportation cost of three different products shipped from two factories to three regional markets. This had to be achieved without violating the production capacity of each factory and while satisfying the demand of each region for every product.

# Step-by-Step Workflow
# Step 1: Importing Required Libraries
The first step involved importing the necessary Python libraries:
•	pulp: Used for defining and solving the linear programming problem.
•	pandas: Imported to support any potential tabular data processing and for easy integration in future stages.
## Step 2: Defining Problem Sets
Three key sets were defined:
•	Factories (F1 and F2)
•	Products (P1, P2, and P3)
•	Regions (R1, R2, and R3)
These sets provided the foundation for building the multidimensional decision variables and constraints.
# Step 3: Factory Capacities
Each factory was assigned a maximum available production time in hours:
•	Factory F1: 500 hours
•	Factory F2: 400 hours
This constraint ensured that no factory could produce beyond its operational capacity.
# Step 4: Production Time per Product
Different production times were defined for each product at each factory. For example:
•	F1 takes 2, 4, and 3 hours respectively for products P1, P2, and P3.
•	F2 takes 3, 2, and 3 hours respectively for the same products.
This step was crucial in determining how factory time would be allocated across different products.
# Step 5: Regional Demand
The demand for each product in every region was specified. For instance:
•	Region R1 needs 50 units of P1, 60 units of P2, and 40 units of P3.
•	Regions R2 and R3 have their own respective product demands.
These demands formed a lower-bound constraint for the optimization model to ensure that customer needs are met.
# Step 6: Shipping Costs
A three-dimensional dictionary was created to represent the cost per unit of shipping each product from each factory to each region. These values formed the basis of the objective function, which aimed to minimize the total transportation cost across all routes.
# Step 7: Defining Decision Variables
Decision variables were defined to represent the quantity of each product shipped from each factory to each region. These variables were:
•	Continuous
•	Non-negative
The variables were structured as x[f][r][p], meaning the quantity of product p sent from factory f to region r.
# Step 8: Problem Formulation
The LP model was formulated as a minimization problem. The objective function was the total shipping cost, calculated by summing the product of unit shipping cost and the corresponding quantity shipped for all factory-product-region combinations.
# Step 9: Adding Constraints
Three main types of constraints were added:
1.	Factory Time Constraint: Total hours used for production at each factory should not exceed the available hours.
2.	Demand Fulfillment Constraint: Each region must receive at least as many units of each product as demanded.
3.	Non-negativity Constraint: All decision variables must be zero or positive.
# Step 10: Solving the Model
The LP problem was solved using PuLP's default solver. Once solved, the results showed the optimal number of units to be shipped from each factory to each region for every product, as well as the minimized total shipping cost.
# Step 11: Interpretation of Results
The optimal shipping plan provided clear insight into how factories should distribute products to regions to minimize costs while meeting constraints. This solution can be directly used in logistics and supply chain decision-making processes.

# Conclusion
This project illustrates a practical application of linear programming in the field of supply chain optimization. It not only demonstrates the ability to mathematically model real-world logistics problems but also showcases how programming skills can be combined with optimization techniques to develop efficient, scalable solutions. The model is easily extendable to more factories, products, or regions and can also be adapted to different objective functions like profit maximization or time minimization.
Overall, the project reflects strong foundational knowledge in optimization, data structuring, and Python-based implementation using PuLP.

# Output


