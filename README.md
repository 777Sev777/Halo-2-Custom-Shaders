# Halo-2-Custom-Shaders
Important Note: Prior to replacing any original shaders with the custom versions available here, it is a good idea to create backup copies of the originals to prevent any unintended loss of data. - THIS IS NOT A REPLACEMENT OF LIGHTMAPPING

Enhanced Shadow Mapping and Dynamic Lighting for Halo 2 to significantly improve the shadow mapping and dynamic lighting within Halo 2. This shader employs advanced techniques to deliver more realistic and visually pleasing result.

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
![image](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/dd040878-6b0b-4734-be0d-750a38841570)
![Hog_2](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/eea0e6a8-5fe9-49ef-93c3-058c27322c54)
![Hog](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/9edf4781-5963-4904-b170-363c31214eb5)
![ChainGun_Hog](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/9a17200c-94c9-443b-907a-63245fa73a6d)
![BR_Magazine_2](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/070e4a9d-84ee-4646-af89-e30a99d907fe)
![SMG_2](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/6692668e-0769-43d4-84e0-7d187ca0673d)
![SMG_1](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/dae93273-9f77-4de3-9cd7-479340f226d6)
![Mongoose_2](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/7bc9363d-f263-45e4-baae-1bddb108dc26)
![Mongoose_1](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/44c317e9-965d-4016-804e-a4753efdd3d0)
![Hog_3](https://github.com/777Sev777/Halo-2-Custom-Shaders/assets/134644571/1bde6309-ee62-454c-b743-e49d65ddcba8)

