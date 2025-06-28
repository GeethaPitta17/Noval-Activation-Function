# Noval-Activation-Function
Introduc on: 
The primary objec ve of this novel ac va on func on is to provide an 
alterna ve to popular ac va on func ons like Relu, sigmoid, and tanh. 
 We focused on   reducing issues like dying neurons , vanishing gradient, 
exploding gradient  ensuring good computa onal efficiency and non 
linearity. 
Problem Statement: 
Develop an ac va on func on that sa sfies the following 
requirements: 
Non-linearity: Effec vely introduces non-linearity to enable                    
the network  to capture complex pa erns. 
Gradient Issues: Addresses the challenges of vanishing or 
exploding gradients during backpropaga on. 
Smoothness: Guarantees smoothness and differen ability 
throughout its domain to support gradient-based opmiza on. 
Bounded Output: Op onally restricts the output within a 
specific range to avoid excessively large ac va ons. 
Efficiency: Ensures computa onal simplicity for prac cal 
implementa on. 
Methodology:  
We chose our custom ac va on func ons based on its proper es 
listed below. We proposed two func ons out of which one is best. 
Unlike ReLU, it avoids the issue of dying neurons by ensuring a 
gradient exists for all inputs, including nega ve values. Compared to 
tanh, it does not compress large posi ve inputs, allowing be er 
informa on flow. Addi onally, the use of smooth transi ons makes it 
easier for opmiza on algorithms to learn effec vely. 
It ensures computa onal efficiency and stability, making it a be er 
choice for addressing gradient-related problems while retaining 
f
 lexibility for complex pa erns. 
Advantages of proposed Func on2(RTHIN): 
1. No Exploding Gradients: The bounded nega ve region (tanh + atan) 
avoids the risk of large nega ve gradients during training. 
2. Smooth Nega ve Handling: The combina on of tanh and atan ensures 
smoother gradient flow for nega ve inputs compared to ReLU's zero or 
ELU's exponen al behavior. 
3. No Exploding Gradients: The bounded nega ve region (tanh + atan) 
avoids the risk of large nega ve gradients during training. 
4. Linear Behavior in Posi ve Region:  Like ReLU, it retains linear behavior 
for posi ve values but adds more flexibility in the nega ve region. 
5. Be er Convergence for Complex Models: Adding non-linear yet bounded 
terms in the nega ve region can help the model explore a richer set of 
representa ons while maintaining stability.
