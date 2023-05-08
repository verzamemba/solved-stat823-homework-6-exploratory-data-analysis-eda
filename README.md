Download Link: https://assignmentchef.com/product/solved-stat823-homework-6-exploratory-data-analysis-eda
<br>
Using RMarkdown in RStudio, complete the following questions. Launch RStudio and open a new RMarkdown file or use the class RMarkdown template provided and save it on your working directory as a .Rmd file. At the end of the activity, save your <strong>pdf </strong>generated from RMarkdown+Knitr and submit your homework on the Blackboard.

<ol>

 <li>Use the built-in dataset cars.</li>

</ol>

<ul>

 <li>Reproduce Figure 1 by creating a scatterplot of speed versus {distance} starting with the code plot(dist <em>≥ </em>speed, data = cars. Add the following details into the plot:sub title “Using plot() in R”, x main title “Scatterplot of Speed versus Distance”, axis title “Speed (miles per hour)”, y axis title “Stopping Distance (feet)”. Make the main title to be red, axis colors to be magenta. Use filled circles for symbol type and make the symbol color to be blue and axis labels to be dark green. Make the fonts of the titles, label axes and symbol sizes to 1.5.</li>

 <li>From Figure 1, create Figure 2. This can be done by turning o the axes using plot(…,axes=FALSE). Add a line of best fit using abline(lm(dist <em>≥ </em>speed, data=cars)). Add a grid using grid(). Add a box around the plotting area using box(col=”red”, lwd=3, lty=3). Add a legend to the plot using legend(“topleft”, inset = 0.01, title = “Distance vs. Speed”, legend = c(“Observation”), col=c(“blue”), pch=19,horiz=TRUE). You can add these commands to get back the axes labels: axis(1) and axis(2).</li>

</ul>

Page -1- of 4

<h2>Scatterplot of Speed versus Distance</h2>

Speed (miles per hour)

Using plot() in R

<strong>Figure 1: </strong>Scatterplot of Speed versus Distance

<h2>Scatterplot of Speed versus Distance</h2>

speed

Using plot() in R

<strong>Figure 2: </strong>Scatterplot of Speed versus Distance

<ol start="2">

 <li>Use the economics built-in dataset and library ggplot2. Plot the time series of unemployment (Figure 3). Starting code is ggplot(economics, aes(date, unemploy)) + geom_line()</li>

</ol>

<strong>Figure 3: </strong>Time Series Graph

<ol start="3">

 <li>Use the built-in dataset survey that contains the results of a survey given to 237 students at the University of Adelaide. Download and install the MASS package and use the R help documentation to examine the contents of survey. Install Hmisc package by typing packages(“Hmisc”,dep=TRUE).</li>

</ol>

<ul>

 <li>Use the str() function to examine the structure of the dataset. Use the describe() function in the Hmisc Use des(), summ() and codebook() functions from the epiDisplay package and summary() function to visualize summaries of the 12 variables in the dataset.</li>

 <li>Load vcd and epiDisplay Use the table(),textttexttextprop.table() and tab1() functions to <em>generate frequency tables </em>describing the distribution of each of the following categorical variables: Sex, Exer and Smoke.</li>

 <li>Produce contingency tables to explore the relationships between Sex and Exercise,</li>

</ul>

Smoke and Exercise and Smoke and Sex. <em>Calculate the Pearson’s Chi-squared test or Fisher’s Exact Test if appropriate (if the expectation of at least one of the cell value is conclusion?Æ 5). From the test of independence of these categorical variables, what would be your </em>(d) Using the following code, write down the least squares regression equation describing the linear relationship between hand span and height and <em>calculate the Pearson’s</em>

<em>correlation coe  cient. What do you notice about </em><em><sub>r</sub></em><sup>2 </sup><em>from the linear regression output and the correlation coe  cient, </em><em><sub>r</sub></em><em>? Based on the Pearson’s correlation matrix Figure </em><em>4</em><em>, which continuous variables are highly correlated?</em>

<strong>data</strong>(“survey”)

ff &lt;- <strong>lm</strong>(Height <strong>~ </strong>Wr.Hnd, data = survey) <strong>summary</strong>(ff)

<em># calculation of Pearson s correlation coefficient. </em><strong>cor</strong>(survey<strong>$</strong>Wr.Hnd, survey<strong>$</strong>Height, use = “complete”)

<table width="632">

 <tbody>

  <tr>

   <td width="632"><em># This code was used to produce the correlation</em><em># matrix </em><strong>library</strong>(psych)dat0 &lt;- survey[, <strong>c</strong>(“Pulse”, “Age”, “Height”, “NW.Hnd”,“Wr.Hnd”)] <strong>pairs.panels</strong>(dat0)</td>

  </tr>

 </tbody>

</table>

20 40 60                                      14 18 22

<table width="414">

 <tbody>

  <tr>

   <td rowspan="3" width="92"></td>

   <td width="76"></td>

   <td width="76">


    <table width="63">

     <tbody>

      <tr>

       <td width="63">−0.08</td>

      </tr>

     </tbody>

    </table></td>

   <td colspan="2" width="170"></td>

  </tr>

  <tr>

   <td colspan="3" width="227">


    <table width="210">

     <tbody>

      <tr>

       <td colspan="2" rowspan="2" width="56">Age</td>

       <td rowspan="3" width="16"> </td>

       <td rowspan="3" width="63">−0.04</td>

       <td rowspan="3" width="13"> </td>

       <td rowspan="3" width="63">0.07</td>

       <td width="0"></td>

      </tr>

      <tr>

       <td width="0"></td>

      </tr>

      <tr>

       <td width="9"> </td>

       <td width="47"> </td>

       <td width="0"></td>

      </tr>

      <tr>

       <td width="19"></td>

       <td width="35"></td>

       <td width="19"></td>

       <td width="61"></td>

       <td width="19"></td>

       <td width="57"></td>

       <td width="0"> </td>

      </tr>

     </tbody>

    </table></td>

   <td width="95">


    <table width="63">

     <tbody>

      <tr>

       <td width="63">0.03</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

  <tr>

   <td colspan="4" width="322"></td>

  </tr>

  <tr>

   <td width="87"></td>

   <td width="76"></td>

   <td width="76"></td>

   <td width="71"></td>

   <td width="120"></td>

  </tr>

 </tbody>

</table>

40 70 100                                150 180                                        14 18 22

<strong>Figure 4: </strong>Pearson’s Pairwise Correlation Coe cients