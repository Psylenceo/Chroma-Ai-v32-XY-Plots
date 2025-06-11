<!--- use these arrows for adding comments or commenting out stuff --->
 # **Chroma-Ai-v32-XY-Plots**  

## Introduction
Was testing out [Chroma](https://huggingface.co/lodestones/Chroma) Ai v32 and wanted to share my results on reddit, but no reddit would always delete my posts, so I'm gonna see if I can post results here.

All tests were performed using [ComfyUI](https://github.com/Comfy-Org) on a local computer using a 4090 and 64GB running in a WSL container limited to 32GB. Consistent settings across all generations: Seed 1000 Steps 20 images generated @ 1024x1024

Plots created using the [Easyuse](https://github.com/yolain/ComfyUI-Easy-Use) node pack.
Big shoutout to [rgthree](https://github.com/rgthree/rgthree-comfy) for their awsome nodes, especially the new power puter node that helped automate directory and file naming logic within my workflow!

### Positive prompt used:
> Photorealistic, 8k, ultra-detailed, full frontal body shot, beautiful white woman with amber hair standing in well
> lit studio while leaning backwards on the car between the drives door and the rear driver side passenger door of a
> vibrant deep purple 1960's style convertable muscle car with red fuzzy dice hanging from the rear view mirror
> facing the camera, she is wearing a blue halter top and white denim mini jacket with yoga pants with black and red
> angled stripes and pink tinted aviator sunglasses, the white jacket has a fur collar, there is also an orange neon
> sign in the top left cornerr with the text " Chroma UNLCOKED v32", sitting in the driver seat of the car is a cat-man
> with orange tabby face wearing a green tank top and black leather jacket and rainbow colored sunglasses, the cat-man
> has one hand on the steering wheel of the car while a leaning on the door of the car looking towards the camera
> while tilting the sunglasses down

### Negative prompt used:
> low quality, bad anatomy, extra digits, missing digits, extra limbs, extra legsm missing limbs, anime, cartoon, drawing, cgi, 3d, digital art, painting, perfect skin, blurry, distorted, airbrushed, rounded, spherical, balloon, idealized features
---

## Table of Contents
- [Euler_Results](./Euler_Results/)                                                   -40% complete
- [Euler_CFG_PP_Results](./Euler_CFG_PP_Results/)                                     -20% complete
- [Euler_ancestral_Results](./Euler_ancestral_Results/)                               -20% complete
- [Euler_ancestral_CFG_PP_Results](./Euler_ancestral_CFG_PP_Results/)                 -20% complete
- [heun_Results](./heun_Results/)                                                     -20% complete
- [heunpp2_Results](./heunpp2_Results/)                                               -20% complete
- [dpm_2_Results](./dpm_2_Results)                                                    -20% complete
- [dpm_2_ancestral_Results](./dpm_2_ancestral_Results)                                -20% complete
- [lms_Results](./lms_Results)                                                        -20% complete
- [dpm_fast_Results](./dpm_fast_Results)                                              -20% complete
- [dpm_adaptive_Results](./dpm_adaptive_Results)                                      -20% complete
- [dpmpp_2s_ancestral_Results](./dpmpp_2s_ancestral_Results)                          -20% complete
- [dpmpp_2s_ancestral_cfg_pp_Results](./dpmpp_2s_ancestral_cfg_pp_Results)            -20% complete
- [dpmpp_sde_Results](./dpmpp_sde_Results)                                            -20% complete
- [dpmpp_sde_gpu_Results](./dpmpp_sde_gpu_Results)                                    -20% complete
- [dpmpp_2m_Results](./dpmpp_2m_Results)                                              -20% complete
- [dpmpp_2m_cfg_pp_Results](./dpmpp_2m_cfg_pp_Results)                                -20% complete
- [dpmpp_2m_sde_Results](./dpmpp_2m_sde_Results)                                      -20% complete
- [dpmpp_2m_sde_gpu_Results](./dpmpp_2m_sde_gpu_Results)                              -20% complete
- [dpmpp_3m_sde_Results](./dpmpp_3m_sde_Results/)                                     -20% complete
- [dpmpp_3m_sde_gpu_Results](./dpmpp_3m_sde_gpu_Results/)                             -20% complete
- [ddpm_Results](./ddpm_Results/)                                                     -20% complete
- [lcm_Results](./lcm_Results/)                                                       -20% cpmplete
- [ipndm_Results](./ipndm_Results/)                                                   -20% cpmplete
- [ipndm_v_Results](./ipndm_v_Results/)                                               -20% cpmplete
- [deis_Results](./deis_Results/)                                                     -20% cpmplete
- [res_multistep_Results](./res_multistep_Results/)                                   -20% cpmplete
- [res_multistep_cfg_pp_Results](./res_multistep_cfg_pp_Results/)                     -20% cpmplete
- [res_multistep_ancestral_Results](./res_multistep_ancestral_Results/)               -20% cpmplete
- [res_multistep_ancestral_cfg_pp_Results](./res_multistep_ancestral_cfg_pp_Results/) -20% cpmplete
- [gradient_estimation_Results](./gradient_estimation_Results/)                       -20% cpmplete
- [gradient_estimation_cfg_pp_Results](./gradient_estimation_cfg_pp_Results/)         -20% cpmplete
- [er_sde_Results](./er_sde_Results/)                                                 -20% cpmplete
- [seeds_2_Results](./seeds_2_Results/)                                               -20% cpmplete
- [seeds_3_Results](./seeds_3_Results/)                                               -20% cpmplete
- [ddim_Results](./ddim_Results/)                                                     -20% cpmplete
- [uni_pc_Results](./uni_pc_Results/)                                                 -20% cpmplete
- [uni_pc_bh2_Results](./uni_pc_bh2_Results/)                                         -20% cpmplete
<!-- next sampler -->

- [XY Plots from Deleted Reddit post](./Deleted_reddit_post/) - had done a simple prompt at 10/20 steps, but ran through all Samplers & Schedulers, had posted on reddit but they flagged it.

- [WorkFlows](./workflows/)
---

## Workflows used
<p align="center">
  <img src="https://github.com/Psylenceo/Chroma-Ai-v32-XY-Plots/blob/main/workflows/XY Plot.png" width="400">
  <img src="https://github.com/Psylenceo/Chroma-Ai-v32-XY-Plots/blob/main/workflows/resizer.png" width="400">
</p>

---


<!--|   | A  | B  | C  |
|---|----|----|----|
| 1 | ✅ | ❌ | ✅ |
| 2 | ❌ | ✅ | ✅ |
| 3 | ✅ | ✅ | ❌ |
-->

## Results overview
Nearl all samplers work with CFG > 2.0

                schedulers
          |                                | Normal | Karras  | Exponential | sgm_uniform | simple | ddim_uniform | beta | linear_quadratic | kl_optimal |
          |--------------------------------|--------|---------|-------------|-------------|--------|--------------|------|------------------|------------|
          | Euler                          |   ✅  |    ❌   |      ❌    |       ✅    |   ✅  |       ✅     |  ✅ |        ✅        |            |
samplers  | Euler_cfg_pp                   |   ❌  |    ❌   |      ❌    |       ❌    |   ❌  |       ❌     |  ❌ |        ❌        |            |
          | euler_ancestral                |   ❌  |    ❌   |      ❌    |       ❌    |   ❌  |       ❌     |  ❌ |        ❌        |            |
          | euler_ancestral_cfg_pp         |   ❌  |    ❌   |      ❌    |       ❌    |   ❌  |       ❌     |  ❌ |        ❌        |            |
          | heun                           |
          | heunpp2                        |
          | dpm_2                          |
          | dpm_2_ancestral                |
          | lms                            |
          | dpm_fast                       |
          | dpm_adaptive                   |
          | dpmpp_2s_ancestral             |
          | dpmpp_2s_ancestral_cfg_pp      |
          | dpmpp_sde                      |
          | dpmpp_sde_gpu                  |
          | dpmpp_2m                       |
          | dpmpp_2m_cfg_pp                |
          | dpmpp_2m_sde                   |
          | dpmpp_2m_sde_gpu               |
          | dpmpp_3m_sde                   |
          | dpmpp_3m_sde_gpu               |
          | ddpm                           |
          | lcm                            |
          | ipndm                          |
          | ipndm_v                        |
          | deis                           |
          | res_multistep                  |
          | res_multistep_cfg_pp           |
          | res_multistep_ancestral        |
          | res_multistep_ancestral_cfg_pp |
          | gradient_estimation            |
          | gradient_estimation_cfg_pp     |
          | er_sde                         |
          | seeds_2                        |
          | seeds_3                        |
          | ddim                           |
          | uni_pc                         |
          | uni_pc_bh2                     |


---

## License
[MIT License](./LICENSE)
