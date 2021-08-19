# Criterions
This repo contains linear and polynomial regression on different loss functions and hence different loss functions are compared.

## DESCRIPTION
1.I generated a random dataset and the y_real also was set to 1/2 degree polynomial with some noise in it.<br/>
### Comparison in loss functions:
a. So the four loss functions used were:<br />
   |x -  x̂|³ <br/>
   |x -  x̂|  <br/>
   |x -  x̂|⁴ <br/>
   |x -  x̂|⁷<br/>
  
1.Linear regression was trained on first two losses and it was observed that in linear loss ,less number of iterations with considerably high learning rate gave results very close to the real values whereas the cubic loss function just gets exploded if the input data is taken randomly and not normalized(which I did) and hence a smaller learning rate and large no of epochs were able to give satisfactory results.

2.In polynomial regression also the same behaviour was observed. Seventh order loss function just amplified the loss and hence resulting in overflow.So the accuracy of the model was not so great and required large time(as learning rate is slow and no. of iterations are more) to train such a simple model. Hence it is very inefficient to use it as a loss function.<br/>

So accordingly loss function in order of their efficiency :  |x -  x̂| >> |x -  x̂|³  > |x -  x̂|⁴ >>>>> |x -  x̂|⁷
