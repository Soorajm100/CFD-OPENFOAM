REPORT ON TAYLOR COUETTE FLOW PROBLEM
Aim:To analyse the taylor couette flow in annular cylinder
Introduction : In fluid dynamics, the Taylor–Couette flow consists of a viscous fluid confined in the gap between two rotating cylinders. For low angular velocities, measured by the Reynolds number Re, the flow is steady and purely azimuthal.
Given:  omega = 6 rad/s R1 = 1m   R2 = 2m  dynamic viscosity = 0.1 Pa.s  Density = 1 kg/m3
Proceedure:This is the case of steady flow. First is the creation of the mesh. We shall consider the 2D mixer vesseland make a special case out of it so that it can  fit our problem.First we shall copy the 2D mixer vessel case form the incompressible folder from simpleFoam and then make changes in its structure.The commands to be used  in the simpleFoam folder are : cp –r  mixerVessel2D  $FOAM_RUN/test_final.
Then we finally go to the system folder and make the mesh according to our requires size.Now since the vessel got blades.The main challenge here is to make this case an approximation to our required case.So  inorder to do that we shall keep the impeller radius and Baffle tip radius to keep it near to 1 so that it can give an approximation of the levelled surface in the inside.after that we run the command  : ./makeMesh .This inturn executes the blockMesh file and creates the blockMeshDict file inorder for the creation of the mesh.This way we create a MRF region We change the  inner angular velocity to 6 rad/s according to the problem.Then we keep the turbulence property as laminar and run the simulation.we change the writeInterval and End interval for better results.Then we use the command simpleFoam too run the simulation.
We use the command touch .foam to make the meshfile which we will be opening in the paraview.we open the file .foam to load the mesh.Then we plot the velocity and shear stress in the paraview. Then coming to the analytical part it can be calculated by taylor theory.
Theory : For steady flow we have the equations
 
A= -2  B=8  after substituting in the formula.
V_azi = -2*r +8/r
We can repeat the simulation by RAS model of turbulence the results does not seem to be of changing much .The RAS model is mainly based on Reynolds averaged simulation model which mainly estimastes the parameters in average.This methodology is based  on decomposition of flow variables into a mean and a fluctuating part The navier stokes equation is solved by using the mean values. 
 First part is the averaged part .The second part is the fluctuating part .For all averaging approach the average of the fluctuating part is zero.
Observations:
The laminar flow follows with the theoretical approach of the taylor couette flow.
The velocity is maximum in the middle section of the mesh where it is marked by red region .
 Results and discussions:
Theoritically the velocity in the inner cylinder is found to be 6m/s and is in accordance with the graph.Just a slight deviation otherwise all values are close to each other both in laminar and RAS model.
Coming to the wall shear stress.we get the wall shear stress in the inner cylinder to 0.6 N/mm2.This clearly states that the shear stress goes along with the analytical ones .Same is the case for the RAS model as well 
The pressure is evenly distributed.If the angular velocity is increased.The flow would actually be changed to turbulent causing to vortises to occur.Thus flow will not be steady anymore.The shear stress can  be given by  for both the cases.
    -(1)
Analytically calculating
   
we get  0.6 N/mm2   .at the inner cylinder.
Basically when we calculate analytically the inner wall shear stress is found to 0.6N/mm2 .Since the velocity gradient reduces drastically as the radius increases so does the shear stress. Hence its clear that as the outer cylinder doesn’t move. So the outer wall shear stress is 0 analytically. And close to zero experimentally.
.Now inorder to plot the shear stress we use the formula above  given as (1).The plot can  be given  as follows:
THE SHEAR STRESS AND  VELOCITY IN LAMINAR FLOW
The velocity is 6m/s and wall shear stress can be found at x=0 ,x= 1,x=3 and x=4.The wall shear stress at the inner cylinder is equal to 0.6N/mm2.
   
THE VELOCITY AND SHEAR STRESS IN TURBULENT  FLOW
The velocity is 6m/s and wall shear stress can be found at x=0  ,x= 1,x=3 and x=4.The wall shear stress at the inner cylinder is equal to 0.89 N/mm2.Reprsented by green in second image.   
We could calculate the  shear stress with the azimuthal velocity as well by using the gradient feature in paraview as we did for experimental value.  We get the same answer  which is around 0.599 N/mm2 . By using the equation 1.Represented by blue in laminar and orange in RAS
Conclusion :
The simulation of annular taylor couette flow is analysed succcesssfully.
