# Calculating a Standard Curve Dilution

In this article, we will walk through the process of calculating a standard curve for serial dilutions. The general idea is to take user inputs for the parameters involved in the dilution process and generates a table showing the necessary details, including stock solution volumes, diluent volumes, and concentrations.

### Inputs Required

The following inputs are needed to generate the standard curve table:

1. **Stock solution name**: The name of the stock solution being used, for example, glucose or a protein solution.
2. **Diluent name**: The name of the substance used to dilute the stock solution, typically water or buffer.
3. **Concentration of the stock solution** ($$\mu M$$): The concentration of the stock solution in micromolar units.
4. **Serial dilution initial concentration** ($$\mu M$$): The starting concentration of the serial dilution, typically lower than the stock solution concentration.
5. **Dilution factor**: The factor by which the solution is diluted in each step. For example, a dilution factor of 2 means each dilution step halves the concentration.
6. **Final volume of each dilution** ($$\mu L$$): The total volume of each diluted solution.
7. **Number of dilutions**: The total number of dilutions to be performed.

### The Math Behind Serial Dilutions

The first step is to calculate the needed volume to make with your desired initial dilution, this will be calculated by finding the max volume in each dilution. This is the volume of your needed dilution with the addition of any volume which will be transfered out to the next dilution in the series.\
\
To do this we need to:\
1\. Find the volume to transfer between dilutions: this can be calculated using&#x20;

$$
V_{\text{transfer from one dilution to the next}} = \frac{V_\text{final volume needed}}{\text{dilution factor}-1}
$$

2. Add transfer volume to the needed volume

$$
V_{\text{max}} = V_\text{final volume needed}+V_\text{transfer from one dilution to the next}
$$

3. we can also calculate the volume of dilent needed to be added to each well in this step as well very easily by doing this&#x20;

$$
V_\text{diluent to add} = V_{\text{transfer form one dilution to the next}} - V_\text{max}
$$



***

Now that we have our max volume/volume needed to make for each resulting dilution before any volume is taken out for the next dilution we can calculate the inital dilution made from our stock concentrate (this may not be needed if your stock is at the needed concentration anyway or if it is resulting in a powder or solid being diluted)\
\
to do this we need to:\


$$
V_{\text{transfer from stock}} = \frac{V_\text{max}*{C_\text{serial dilution initial concentration needed}}}{C_\text{stock solution}}
$$

to find the amount of diluent to add to the inital well we take the volume transfered from the stock and subtracxt this from the maximum volume we are to generate

$$
V_\text{diluent to add} = V_{\text{transfer from stock}} - V_\text{max}
$$
