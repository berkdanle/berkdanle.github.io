# Data Analyst

### Technical Skills: Python, Java, SQL, R, C++, Pandas, MATLAB, ML, Matplotlib, Seaborn, Scikit-learn, NLTK

## Education
**UC Berkeley Data Science (_May 2024_)**

## Work Experience
**Market Analyst @ Clorox (_January 2023 - May 2023_)**
- Synthesized market analysis in 7 Southeast Asian countries to identify development potential within the cleaning industry to advance Clorox’s product development decisions, integrating 15+ unique products in specific areas to reach their target audience
- Developed Product Power tool, an interactive spreadsheet leveraging the cleaning market database to evaluate an individual product’s strategic impact on a scale 1-3, likelihood of success in a specific region, facilitating Clorox’s product differentiation
- Streamlined Clorox’s health and wellness product line, analyzing data from over 200 unique SKUs to optimize product allocation within Southeast Asian Market and increase customer engagement

**User Experience Analyst @ Glad (_September 2022 - January 2023_)**
- Directed social media campaign to increase brand recognition to reach Chinese target audience through optimizing user experience and  feature updates, resulting in a 63% rise in user engagement, 42% increase in retention, and 33% growth in product conversion rate
- Aggregated data across 14 Chinese cleaning competitors social media platforms and over 1000 videos, evaluating successful marketing trends to develop strategies and conduct plans to reach a larger audience segmentation 
- Analyzed competitor’s customer journey through CTR (Click Through Rates), average view duration, and engagement, leading to development of strategic initiatives such as demo product videos, customer surveys, and amplified social media presence

## Projects
### The Effect of Airplane Construction on Flight Time | R, Python,  Linear Regression, Data Visualization

## Abstract
  How do different flight components on an airplane impact the aerodynamics of an airplane? The experimental investigation aims to examine the variables affecting paper airplane flying time. This study focuses on three crucial variables: the airplane's **overall length**, the **wing length**, and its **launch power**. To gauge our design factor's impact on the paper airplane model, we will use the average flight duration (from launch to ground contact) as our performance indicator for the experiment. 
  To test this, we will fold paper with specified treatment dimensions and then launch each paper airplane design at different levels of power in a series of runs via a rubber band mechanism at a fixed height with a fixed force. After a series of runs, we will take the average flight durations from each treatment group and evaluate the effect and possible interactions of the designated factors. 
  Our experiment’s results indicated that the wingspan had a **significant effect** on the average flight duration of the paper airplane, and the power-wingspan interaction was significant. Furthermore, depending on the combinations of treatments assigned, we evaluate different flight durations, indicating **interaction effects** within the experimental groups.

## Methodology
  The experimental design examined how different flying parameters, such as the airplane's overall length, wing length, and launch power, affect paper airplane aerodynamics. The main goal was to determine how these factors affect our response, paper airplane flying time, which we defined as the average flight time from takeoff to ground contact.
  The treatments to the paper airplane are assigned by numbering each piece of paper(up to the number of experiments we are running) and then randomizing the list of treatments to be applied to each piece of paper (in this case, the dimensions for the origami). Each unit will receive a randomized combination of the airplane model conditions: three different wing lengths, two different airplane lengths, and two different launch strengths. A **CR[3] design** is used as all three factors can affect flight time and interact with each other, but it is not definitive. Moreover, we are controlling for factors like launch height and weight of payload, a CR design is suitable, then we do not need to block for other factors. To ensure unbiased treatment assignment, we permuted the 12 different treatment combinations (width, length, power) and assigned them randomly to 12 different paper airplanes. After the assignment and folding, the paper airplanes were launched with a rubber band, stretched to either maximum or full length to adjust the launch power. Adjusting the launch power based on the assigned conditions. 5 runs were conducted for each combination to capture the different variations in the paper airplane's flight. The number of runs was determined from a power calculation, which used preliminary data to estimate the number of runs needed per treatment group to obtain a power of 0.8. While a proper experiment would have made five different paper airplanes for each treatment, we decided to fly the same plane five times to keep the experiment feasible. This was also why we chose not to use a split-plot design to help minimize the possible damage to each plane between runs. After the trials, we obtained the following data from our trial, shown in Table 1 below. 

![Table 1](/assets/img/table1.png)

  From the full data, we are able to create an **ANOVA table**, which gives us a measure of variance for each factor. We can then run **randomization inference** to find the likelihood that we achieved the results we got by chance alone, and thus, let us know if any of our factors have a **statistically significant effect** on the flight time of these paper airplanes.
  Lastly, we are also testing three separate contrasts. We are testing the difference in average flight time between treatment groups that had a wing and those that didn’t in order to see how vital having a wing is in the first place, as opposed to just letting a paper fall in freefall. We are also testing the difference in average flight time between winged groups launched at either full or half power so that we can see if the power had a different effect on the winged groups. The last contrast we are testing is the difference in average flight time between the airplanes with the largest *(30 cm length, 8 cm wingspan)* and smallest (15 cm length, 4 cm wingspan) wing size, at either power, since we hypothesize that surface area might be a factor.

## Results

  Once the data was collected, we performed some preliminary data analysis by making some exploratory graphs. In Figure 1, the mean flight time seems to be about the same depending on the plane's length, and the same goes for the launch power of the plane. However, we do see that the full-power distribution is much more varied than the half-power distribution. This could possibly be due to a higher strength launch causing the plane to catch the air more, causing it to either gain more uplift and stay in the air longer or start aiming down and crash into the ground faster, which was observed for experimental group 4.

![Figure 1](/assets/img/figure1.png)

  A similar analysis was done regarding the wingspan in Figure 2, except with a box-and-whisker plot to compare three levels of wingspan to each other easily. Here, we can see an upward trend of the mean of these distributions, which could possibly correlate with wingspan having a significant effect on flight time, though any conclusive analysis has not been done yet.

![Figure 2](/assets/img/figure2.png)

![Figure 3 A - D](/assets/img/figure3ad.png)

  After looking at the distribution of the data for each factor, we then were able to look at how each factor interacted with each other. In each of these interaction graphs, a change in slope across two different levels of a factor signals that there is a possibility that one of those factors influences how the other factor changes the response variable.
	In figure 3A, we see the interaction between the length of the airplane and the launch power. While we do see a change in the slope, which does support there being interaction between these factors, the small scale means that any interaction may **not** be statistically significant enough for us to find with this small of a data set.
	In Figures 3B and C, however, we see a much different story, as there is a clear change in slope for both graphs. This is consistent with an interaction between the pairs of factors shown in these graphs: power and wingspan for graph 3B, and length and wingspan for graph 3C. From this, we expect to possibly see some significant results for these interactions once we perform further statistical analysis.
	Our last graph is the **three-way interaction** graph shown in Figure 3D. We do see one **major** variation in this graph, the point at a length of 30 cm, a wingspan of 4 cm, and full launch power. This could be a sign of a three-way interaction between all three factors, but it could also be the result of experimental error, as the plane constructed for this experiment tended to fly straight down due to the small wings providing uplift at the back of the plane. Additionally, the significance of this variation is impossible to tell without proper analysis.
	With that, we are now ready to do that analysis. We start by running **ANOVA** on our data, and obtaining an ANOVA table with all of the calculated **F values**, as shown in Table 2. 

![Table 2](/assets/img/table2.png)

  While the normal ANOVA is also able to provide a calculated p-value for each factor, we are instead opting for randomization inference to find significance. To do this, we randomize our results, assigning each recorded time to a new treatment. Once we have these new randomized results, we run ANOVA analysis again and record each F value found this way. We repeat this process a large number of times (in our code, we chose 10,000 runs) and end up with a list of F values obtained from randomization. To calculate a p-value, we find the proportion of F values that are greater than the F value we obtained using the original data. These p-values can be seen in Table 2, and they show that we could **reject** the null hypothesis at the **α = 0.05** level for both wingspan and the interaction between wingspan and power. This means that we reject the hypothesis that wingspan **does not** have an effect on average flight time for airplanes, as well as the hypothesis that the launch power does not change the effect wingspan has on flight time. 
	For our **contrasts**, we performed a similar process. Instead of ANOVA, however, we used the difference in means. This means we started out by calculating the difference in means between winged and non-winged groups (accounting for the different number of groups), between winged groups with different powers, and between the groups with the largest and smallest wing surface areas. We then randomized the results for the flight time recalculated these means, and repeated this 10,000 times. We then obtained p-values by finding the proportion of these randomized differences in means that had a greater magnitude than the original data set. We found p-values of **0.0014, 0.8786, and 0.1672** for each of the contrasts, respectively. This means that we only reject the null hypothesis for the first contrast: that there is no difference in mean flight times between paper airplanes with and without wings.

## Discussion

  By using statistical analysis, we were able to find that the wingspan was the only significant factor in the flight time of a paper airplane, as well as the presence of a wing, and that length and power alone did not have a statistically significant impact on the flight time. Additionally, we found that the launch power and wingspan did have a **significant interaction**, where changing one factor changes how the other affects the flight time.
	In the future, many more experiments could be conducted on this topic. The launch angle or height could be investigated, as well as the size of the paper used to construct the plane. Different designs of paper airplanes could also be compared, which would then lead to the analysis of which aspects of the design affected the airtime. Distance traveled could be a new response factor to analyze, which would need to be analyzed carefully to account for things like drifting off course or travel time while on the ground. Lastly, this experiment could be run again with more improvements, such as a timing system not based on human reaction time, a more robust and controlled launch mechanism, and a larger sample size with multiple different airplanes constructed for each treatment.

 ## Below are the results of the trials: 

 ![Airplane Results](/assets/img/airplaneresults.png)
