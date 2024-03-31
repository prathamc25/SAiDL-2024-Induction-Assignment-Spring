# CV Assignement

## Pre Knowledge
I already had coded a mnist dataset OCR priorly without using pytorch or tensorflow as such. Just bare numpy (vectors) by creating a 2 epoch (layered fn)(F.C.) also tried to implement one CNN from scratch although failed miserably while doing so and had to refer a lot of sources

Already completed the DL specialization from Coursera  by Andrew NG priorly

## Logs
Try to maintain this section also failed to do so for the RL section as had a lot of ups and downs  
Starting with understanding the basics of what an autoencoder is  
Pretty much got the concepts of the VAE  
Starting to struggle a little bit with the math of KL divergence  
Figured it out  
Now got the final intuition and will start to build the final model  
Starting coding!

## Theory Part
Started with the KL divergence firstly  Had received its hint in a PnS tute when he was trying to approximate every distribution to a normal by the CLT  And so in the class i asked what about other distributions and why dont we approximate certain distributions to certain prob. models that was when i had first heard about KL div.

Finished KL Div.  
Started with the VAE article  
Got a lot of help with the article and stuided all the linked one also exceot the bayesian interference one spent approxiamtel 3-4 hours but then too no clear concept   
I think as far I have pretty much covered the basics of the VAE and the theory  
Would like to know about the GAn talked about in the articles  Will try to cover that after the deadline for the assignemnts.

Currently i think i have covered the necessary theory and shall move on with coding. Will edit here if i have to study more theory.

Edit 1: Tried to derive the expression for KL divergence of two distributions given the mean and variance. Struggled on it for about 2-3 hours



## Coding
Dont know what to take the bacth size for training + testing
Coded the VAE class  
Done with the Optimizer function

## 1st task
The following image attached is with the following hyperparams and the Gaussian(0,1) distribution



## Choosing the variations
### Implementing the MSE loss instead of BCE loss
The document mentioned of trying out different variations for various loss functions. Even though the BCE loss is clearly better for classification tasks present the MSE. The reason behind the thought was that since we are assuming the latent spaces to be following a gaussian distribution so the MSE follows that assumption reducing the mean square error loss

### Implementation of the bonus part with gaussian(1,2)
Clearly implementation of Gaussian(0,1) is a better implementation on the sampled latent space than Gaussian(1,2)  
The images attached below show of that
#### Intro of a MSE loss in G(1,2)
With the above same reason tried to introduce a MSE Loss functions instead of a BCE loss and clearly the results say that BCE loss function was way better at the task of reconstruction(Decoding)
__Reasoning__ : I think that that it has also been proven theoretically that G(0,1) is always a better sampling distibuton than any other in the docs of KL div. Also regarding the loss function 

# Final implementation done with
## 1. Gaussian (0,1) with MSE and BCE loss
## 2. Gaussian (1,2) with MSE and BCE loss
There are attached images of the reconstructed smaple down below.



## Doubts
### Doubt 1
Did not what was to be maintained in the architecture?  As in how many epochs??  What is the exact architecture?? How many FCs what should be the dimension of the latent space and so on.
update regarding the above doubt : got it cleared by karan bhaiya  said to follow any architectue nothing in general as such so will move on what i find from the web

### Doubt 2
Do not know what the ideal batch size for training and test size should be?  
Asked Karan bhaiya he told he has no idea moving forward with a 100 (50 test / 50 train)

