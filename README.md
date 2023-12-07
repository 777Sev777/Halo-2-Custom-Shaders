# Halo-2-Custom-Shaders
Welcome to this specialized repository dedicated to custom shaders designed for the Halo 2 Editing Kit (H2EK). This platform serves as a collaborative space for shader testing, feedback collection, and bug reporting. 

Disclaimer:
All shaders are proprietary software developed solely by SEV. Redistribution 
outside the designated GitHub link is strictly prohibited to prevent the spread
of unauthorized or modified versions, as well as to protect against the risk 
of distributing files that could damage or harm user systems. Modification, 
tampering, and redistribution of this code are permitted only with explicit 
consent. In cases where the shader is modified or adapted, proper 
credit must be given for any retained portions of the original work.

Important Note: Prior to replacing any original shaders with the custom versions available here, it is imperative to create backup copies of the originals to prevent any unintended loss of data.

Featured Shader: Enhanced Shadow Mapping and Dynamic Lighting for Halo 2
aims to significantly improve the shadow mapping and dynamic lighting within Halo 2. This shader employs advanced techniques to deliver more realistic and visually pleasing result.

Technical Specifications:
Texture Sampling: Utilizes DirectX 11's DX11_tex2Dproj function for precise texture sampling.

Shadow Mapping: Description:
This advanced HLSL shader combines two prominent techniques for shadow mapping: 
Percentage-Closer Filtering (PCF) and Poisson Disk Sampling. PCF is used to 
smooth out the hard edges often found in basic shadow mapping, making the 
shadows look more natural. Poisson Disk Sampling adds a randomization aspect 
to the shadow edges, making them appear softer and more realistic. The shader 
includes a bias term to minimize self-shadowing artifacts and uses a 5-tap 
kernel for the PCF combined with 12 Poisson Disk samples, ensuring a balanced 
compromise between performance and visual quality:

![4235634562](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/d4ad5d52-16c8-4be0-92e9-312ede8e31da)

![sdffsfdssssssssssssss4](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/51d2c163-da4a-419c-880d-ba13ed9126cc)

![image](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/36a58644-b950-45a9-8664-41eb7c49d8aa)

![jnkhbjhbhbhb](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/d746d3b1-13b2-4f33-807c-4ddd659806e7)

Depth Biasing: Incorporates a float bias of approximately 0.0015 to minimize self-shadowing artifacts especially for characters faces. This bias term is crucial for avoiding the so-called "Peter Pan" effect, where shadows appear to float above the surfaces they should be attached to.

![image](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/dd040878-6b0b-4734-be0d-750a38841570)

Optimization: The shader is optimized for a shadow map resolution of 1024x1024, ensuring a balance between performance and visual fidelity.

By integrating these techniques, this shader offers a substantial improvement over the default shadow and lighting systems in Halo 2, providing a more Viable use for dynamic lights in both gameplay and cinematics.





