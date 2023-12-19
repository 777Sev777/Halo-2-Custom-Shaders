# Halo-2-Custom-Shaders
Welcome to this specialized repository dedicated to custom shaders designed for the Halo 2 Editing Kit (H2EK). This platform serves as a collaborative space for shader testing, feedback collection, and bug reporting. 

Disclaimer:
Redistribution outside the designated GitHub link is prohibited to prevent the spread
of unauthorized or modified versions, as well as to protect against the risk 
of distributing files that could damage or harm user systems. Modification, 
tampering, and redistribution of this code are permitted only with
consent. In cases where the shader is modified or adapted, proper 
credit should be given for any retained portions of the original work.

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

![56](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/7eccdb21-1f7c-47a8-8261-b4038e7c261c)
![288897878-36a58644-b950-45a9-8664-41eb7c49d8aa](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/c60e7800-5bfd-4373-aed8-669f1bf4b296)


Depth Biasing: Incorporates a float bias of approximately 0.0015 to minimize self-shadowing artifacts especially for characters faces. This bias term is crucial for avoiding the so-called "Peter Pan" effect, where shadows appear to float above the surfaces they should be attached to.

![image](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/dd040878-6b0b-4734-be0d-750a38841570)

Optimization: The shader is optimized for a shadow map resolution of 1024x1024, ensuring a balance between performance and visual fidelity.

By integrating these techniques, this shader offers a substantial improvement over the default dynamic shadow and lighting systems in Halo 2, providing a more Viable use for dynamic lights in both gameplay and cinematics.


Dynamic Lighting Documentation and Best Practices v1.0

1. Introduction
This document provides guidance on optimizing dynamic lighting within game scenes. It is crucial to understand that this is intended exclusively for dynamic lights, this shader is NOT designed to replace Lightmapping.

2. Fundamental Settings for Dynamic Lights

Shader Activation: Ensure the Light tag is set to 3tap. If it is set to 1tap, the shader will remain inactive.

Light Framerate Killer: Enable the "Light Framerate Killer" within the Light tag.

Filtering Level Adjustment: Modify the "fall off" setting in Sapien for each light to tailor the filtering levels.

3. Shadow Management in Large Areas

Optimizing Shadow Casting: In scenes with extensive instance geometry, I recommend disabling shadow casting on environment in the light tag to prevent visual inconsistencies,
such as disappearing shadows. 

Adjusting Bounding Radius: If shadows of objects like crates, scenery, or bipeds vanish at certain angles,
increment their "Bounding Radius" by 1-2 units to rectify the issue.

4. Considerations for Light Size and Field of View

Balance Between Size and Shadow Quality: Larger lights may reduce the shadow quality of smaller objects due to the stretching of shadow maps. This phenomenon is akin to enlarging a 2D image. 

Recommended Lighting Strategy: For larger environments, it is advised to use multiple moderately large lights rather than a single, oversized light source. This approach maintains shadow integrity, though experimentation is encouraged.


5. Engine Limitations and Workarounds

Dynamic Light Limit: The engine supports a maximum of 32 dynamic lights in a BSP, but creative techniques can extend this limit.

Scripting and Trigger Volumes: Employ scripting to manage dynamic lights, removing them when exiting an area and adding new ones upon entry. Other methods to circumvent this limitation should also be explored.

6. High-Resolution Performance

4K Resolution Advisory: High-resolution settings such as 4K can lead to performance issues. Operating at 1080p or using a high-end machine for 4K is recommended.


7. Achieving Sharp Shadows

Light Size and FOV for Sharpness: Utilize smaller lights (0.5x1) with a FOV of 10-60 for sharper shadows. Adjust the filtering for the desired look.

As you dive into using these dynamic lighting techniques, remember your input is invaluable in that process. and we encourage experimentation to get the most out of it

I'm genuinely excited to see how you'll use these tools. 
Your support and feedback mean the world to me and have been crucial in getting us to this point. So, thank you for downloading v1.0 of this shader, for sticking with me, and for being part of this project. I can't wait to see the amazing things you'll achieve with this new resource.

