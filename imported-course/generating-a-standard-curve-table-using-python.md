# Generating a Standard Curve Table Using Python

In this article, we will walk through the process of creating a Python script that calculates and generates a standard curve table for serial dilutions. The script takes user inputs for the parameters involved in the dilution process and generates a table showing the necessary details, including stock solution volumes, diluent volumes, and concentrations.

### Inputs Required

The following inputs are needed to generate the standard curve table:

1. **Stock solution name**: The name of the stock solution being used, for example, glucose or a protein solution.
2. **Diluent name**: The name of the substance used to dilute the stock solution, typically water or buffer.
3. **Concentration of the stock solution** ($$\mu M$$): The concentration of the stock solution in micromolar units.
4. **Serial dilution initial concentration** ($$\mu M$$): The starting concentration of the serial dilution, typically lower than the stock solution concentration.
5. **Dilution factor**: The factor by which the solution is diluted in each step. For example, a dilution factor of 2 means each dilution step halves the concentration.
6. **Final volume of each dilution** ($$\mu L$$): The total volume of each diluted solution.
7. **Number of dilutions**: The total number of dilutions to be performed.
8. **Number of replicates (optional)**: The number of replicates for each dilution (default is 1).

### The Math Behind Serial Dilutions

To calculate the volume of the stock solution and the diluent, as well as the resulting concentration for each step of the serial dilution, we use the following formulas:

1. **Stock solution volume**: The volume of stock solution required to achieve the target concentration in each dilution is calculated as:

$$
[ V_{\text{stock}} = \frac{V_{\text{final}}}{\text{dilution factor}} ]
$$

Where:

* $$V_{\text{stock}}$$ is the volume of the stock solution.
* $$V_{\text{final}}$$ is the final volume of the dilution.
* Dilution factor is the factor by which the solution is diluted.

2. **Diluent volume**: The volume of the diluent is simply the difference between the final volume and the stock solution volume:

$$
[ V_{\text{diluent}} = V_{\text{final}} - V_{\text{stock}} ]
$$

3. **Concentration**: The concentration of the solution at each step is calculated by dividing the initial concentration by the dilution factor:

$$
[ C_{\text{new}} = \frac{C_{\text{initial}}}{\text{dilution factor}} ]
$$

Where:

* $$C_{\text{new}}$$ is the new concentration after dilution.
* $$C_{\text{initial}}$$ is the concentration before dilution.

This process is repeated for each dilution step to generate the full table.

### Python Code

The following Python code takes the user inputs and performs the calculations to generate a standard curve table. The results are displayed in a well-formatted table.

```python
import pandas as pd

def calculate_standard_curve(stock_solution_name, diluent_name, stock_solution_conc, initial_conc, dilution_factor, final_volume, num_dilutions, num_replicates=1):
    data = []
   
    # Initial row from stock solution
    stock_solution_volume = final_volume / dilution_factor
    diluent_volume = final_volume - stock_solution_volume
    concentration = initial_conc
    data.append([1, stock_solution_volume, f"from {stock_solution_name} {stock_solution_conc} uM stock", diluent_volume, concentration, final_volume])
   
    # Loop through the remaining dilutions
    for i in range(2, num_dilutions + 1):
        stock_solution_volume = final_volume / dilution_factor
        diluent_volume = final_volume - stock_solution_volume
        concentration /= dilution_factor
        data.append([i, stock_solution_volume, f"from dilution {i-1}", diluent_volume, concentration, final_volume])

    # Convert to DataFrame for display
    df = pd.DataFrame(data, columns=["Dilution", "Stock Solution Volume (uL)", "Source",
                                     f"{diluent_name} Volume (uL)", "Concentration (uM)", "Max Volume in Well (uL)"])
   
    return df

def main():
    # Ask user for input values
    stock_solution_name = input("Enter the stock solution name (e.g. Glucose): ")
    diluent_name = input("Enter the diluent name (e.g. Water): ")
    stock_solution_conc = float(input("Enter the concentration of stock solution (uM): "))
    initial_conc = float(input("Enter the serial dilution initial concentration (uM): "))
    dilution_factor = float(input("Enter the dilution factor: "))
    final_volume = float(input("Enter the final volume of each dilution (uL): "))
    num_dilutions = int(input("Enter the number of dilutions: "))
    num_replicates = int(input("Enter the number of replicates (optional, default is 1): ") or 1)
   
    # Calculate the standard curve
    df = calculate_standard_curve(stock_solution_name, diluent_name, stock_solution_conc, initial_conc, dilution_factor, final_volume, num_dilutions, num_replicates)
   
    # Display the table
    print("\nStandard Curve Table:")
    print(df)

# Run the main function
if __name__ == "__main__":
    main()
```

Explanation of the Code

1. `calculate_standard_curve` function: This function performs the calculation of stock solution volume, diluent volume, and concentration for each dilution step. It stores the results in a list and converts the list to a pandas DataFrame for easy tabulation and display.
2. User Input: The user is prompted to enter the values for the parameters listed above. The input is parsed and passed to the calculate\_standard\_curve function.
3. Output: The final table is displayed, showing each dilution step with the corresponding stock solution volume, diluent volume, concentration, and final volume in each well.
