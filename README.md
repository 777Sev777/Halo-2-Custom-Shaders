# Halo-2-Custom-Shaders
Welcome to this specialized repository dedicated to custom shaders designed for the Halo 2 Editing Kit (H2EK). This platform serves as a collaborative space for shader testing, feedback collection, and bug reporting. While the repository currently features a single shader, I have plans for extensive expansion into other visual effects the near future. But my immediate focus is on advancing shadow mapping techniques, after which I will move into other shader types.

Important Note: Prior to replacing any original shaders with the custom versions available here, it is imperative to create backup copies of the originals to prevent any unintended loss of data.

Featured Shader: Enhanced Shadow Mapping and Dynamic Lighting for Halo 2
aims to significantly improve the shadow mapping and dynamic lighting within Halo 2. This shader employs advanced techniques to deliver more realistic and visually pleasing results.

Technical Specifications:
Texture Sampling: Utilizes DirectX 11's DX11_tex2Dproj function for precise texture sampling.

Shadow Mapping: Ive Implemented a 5x5 Percentage Closer Filtering (PCF) to produce softer, more natural-looking shadows. This technique is particularly effective in mitigating aliasing artifacts commonly associated with shadow mapping:

![4235634562](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/d4ad5d52-16c8-4be0-92e9-312ede8e31da)



Depth Biasing: Incorporates a float bias of approximately 0.0015 to minimize self-shadowing artifacts especially for characters faces. This bias term is crucial for avoiding the so-called "Peter Pan" effect, where shadows appear to float above the surfaces they should be attached to.

![image](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/dd040878-6b0b-4734-be0d-750a38841570)

Optimization: The shader is optimized for a shadow map resolution of 1024x1024, ensuring a balance between performance and visual fidelity.

By integrating these techniques, this shader offers a substantial improvement over the default shadow and lighting systems in Halo 2, providing a more Viable use for dynamic lights in both gameplay and cinematics.

If you's like to learn more about the techniques listed above here are some useful papers and sites:




