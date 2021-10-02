
# Session 2 Backpropagation

## Few key points about the file 'BackProp.xlsx'

<br />The excel file demonstrated backpropagation with a 2 layer fully connected neural network .There are two inputs being i1 and i2. We have 1 hidden layer and 1 output layer. It has Sigmoid  as its activation function at both layers.  The E_Total represents the cumulative loss from E1 and E2. E_Total is the loss and not a neuron.
<p align="center">
  <img src="https://user-images.githubusercontent.com/90038094/135690470-e26fe6fb-6390-44bd-a22b-07087095a2de.JPG" />
</p>
<br />Highlighted in green are the target output expected from the input i1 and i2 highlighted in purple text. Red are the initial weights which are adjusted by back propogation at every epoch after taking into consideration the cumulative loss from E1 and E2 in blue colour which is cumulitavely represented in orange background fill.

<p align="center">
  <br /><img src="https://user-images.githubusercontent.com/90038094/135690949-075ff26c-eeb5-49e4-a69c-1493f440154d.JPG" />
</p>

## Learning rate.

<br />We are trying to minimize the loss between actual output and our given samples. The process to reach the minimized loss occurs over several steps. We generally start with arbitrarily set weights and slowly move closer towards the minimized loss. The learning rate decides the size of steps we take to reach the minimized loss. Learning rate is a hyperparameter which is generally set between 0.1 and 0.0001 when starting training. When Learning rate is set too high, we might take a step which might step ahead of the minimum loss and miss it whereas if we set the Learning rate too low, it would take forever to reach the point of minimized loss.

### Below we will see the rate of error reduction with changes in Learning rate.

<br />![LR01](https://user-images.githubusercontent.com/90038094/135686967-828409cc-79b6-43c5-880a-e3849d0970fb.JPG)
<br />In the above image, the learning rate is set at 0.1. The rate of loss reduction is very low and even after 48 epochs it only reches to a mere 0.18 accumulated loss.
<br />![LR01](https://user-images.githubusercontent.com/90038094/135687839-58408457-1261-46a3-985a-fba164439002.JPG)
<br />In the above image, the learning rate is set at 0.2. The increase of learning rate to 0.2 attains the result of the previous 48 epochs at LR= 0.1 in just 25 epochs thus leading the model towards loss minimization faster.
<br />![LR01](https://user-images.githubusercontent.com/90038094/135687921-82c3bbd0-2d0e-4486-891d-6f819ee98e75.JPG)
<br />In the above image, the learning rate is set at 0.5 which further bolsters the result leading to a mere 0.06 accumulated loss.
<br />![LR01](https://user-images.githubusercontent.com/90038094/135687985-c0966b0f-af83-4f8e-a607-bc1e68105910.JPG)
<br />In the above image, the learning rate is set at 0.8 and the accumulated loss level of 0.05 is breached for the first time in 48 epochs
<br />
<p align="center">
  <img src="https://user-images.githubusercontent.com/90038094/135688078-8269445c-5f7e-419d-a158-728afdd2e6cc.JPG" />
  <img src="https://user-images.githubusercontent.com/90038094/135688124-25fcf6bc-5de5-483e-9c13-b26b404bcef5.JPG" />
</p>
<br />In the above images, the learning rate is set at 1 & 2 respectively. Here we see that the cumulative loss has been reached at a sufficient level quite early on and the additional epochs of training is a waste of compute power and not leading to much of a gain.
<br />
<br />Thus in conclusion a learning rate is a hyperparameter which helps in reducing the compute required to reach a certain level of loss if used at a correct rate on the right type of data.
