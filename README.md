# Back-Propogation-Architectural-Basics


## Part 1 - Back Propogation

This part expands on how Back Propogation works. We take an example with 2 inputs and 2 outputs and 1 hidden layer. (image below)  

The foward calculations the network uses are shown in block 1. We know the inputs & outputs and we need to learn what our weights will be so that when i1 and i2 are inputs, our model should give us outputs o1 and o2. The initial weights are random and by minimising the difference between the actual outputs & model outputs, we try to bring the inital random weights closer to the weights we need them to be. Backward propogation helps us with that. Once we understand the value of Loss (E_total in Block 1) we try to minimize it for each weight. This done by using partial derivative of Loss for each weight. It gives the direction & magnitude our weights need to change. Block 3 and 6 display the calculations or partial derivative of Loss for each weight. We update them using the formula $w_{t+1}$ = $w_t-(learningRate)*(dEtotal/dw_t) $

![image](https://github.com/iris-kurapaty/Back-Propogation-Architectural-Basics/assets/52544352/1cb2bf28-15cf-42a3-a5a2-572b0c2fa957)

![image](https://github.com/iris-kurapaty/Back-Propogation-Architectural-Basics/assets/52544352/03e6dd7b-1c4f-4daf-8001-27f4d848b299)

### Error Results with Different Learning Rates

The images below shows the rate of change of Loss with each iteration.

1. For Learning rate 0.1\
  ![image](https://github.com/iris-kurapaty/Back-Propogation-Architectural-Basics/assets/52544352/097f111d-6bde-4265-bb7f-2d3a311bda61)

2. For Learning rate 0.2\
  ![image](https://github.com/iris-kurapaty/Back-Propogation-Architectural-Basics/assets/52544352/a69fb2cb-30cc-48b9-a10a-5b3d2c42bae9)

3. For Learning rate 0.5\
  ![image](https://github.com/iris-kurapaty/Back-Propogation-Architectural-Basics/assets/52544352/f123150e-b083-4270-b475-ea8f08e21431)

4. For Learning rate 0.8\
  ![image](https://github.com/iris-kurapaty/Back-Propogation-Architectural-Basics/assets/52544352/41e8f487-3133-40d8-a6c5-de49f35138cb)

5. For Learning rate 1\
  ![image](https://github.com/iris-kurapaty/Back-Propogation-Architectural-Basics/assets/52544352/377d591e-6eef-4031-9806-ecd3f5b27921)

6. For Learning rate 2\
  ![image](https://github.com/iris-kurapaty/Back-Propogation-Architectural-Basics/assets/52544352/542d91e1-8e96-402d-baed-1ab6ca8833cf)


*Note:* PLease check the excel file Back_Propogation.xlsx on the repo to see all calculations.
## Part 2 
The objective was to build a model that gives us:
1. 99.4% validation accuracy
2. Has less than 20k parameters
3. Runs for less than 20 Epochs
4. Uses Batch Normalization & Dropout
5. Uses a Fully Connected Layer or Global Average Pooling

The architecture of the model can be seen in the Jupyter notebook uploaded in Folder S6. The results are of the experiments are in the logs of the same file. 
