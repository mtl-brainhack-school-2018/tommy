# dSim - Diffusion Simulator

dSim is magnetic resonance diffusion simulator. dSim simulates the brownian motion of bundles of water molecules as they interact with simple membrane structures, such as tubes and spheres simulating axons and cell bodies. While the particles are diffusing, dSim can play out user-specified diffusion-weighting gradient pulses and read out the predicted MR signal from the system. The dSim system can be thought of as the sample chamber in an NMR experiment or one voxel in an MRI experiment.

To accelerate the simulation, dSim takes advantage of the massively parallel GPU in your video card. It currently requires a CUDA-capable nVidia GPU (g80 or g90 GPU), such as that in the 8x00, 9x00, and 10x00 series of GeForce graphics cards, a Quatro FX or NVS card, or a Tesla co-processor card. (See http://www.nvidia.com/object/cuda_learn_products.html). If you don't have an appropriate GPU, dSim will run (much more slowly!) on the CPU.

To build dSim, you will need the CUDA environment installed. See http://www.nvidia.com/object/cuda_get.html. You will also need libconfig (http://www.hyperrealm.com/libconfig/). On Redhat/Fedora, try "yum install libconfig-devel". On Debian/Ubuntu, try "apt-get install libconfig-devel".

To run dSim, you need to specify a configuration file that sets basic simulator parameters, a grads file that specifies the diffusion gradients to play out, and a fibers file that sets up the cylindrical fibers that the simulation will measure.
