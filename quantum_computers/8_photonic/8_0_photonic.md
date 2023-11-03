---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

:::::{grid}
::::{grid-item-card}
:shadow: lg

```{grid-item-card}
:shadow: lg
![D53](_static/D53.png)
```

::::
:::::

# Photonic and Optical Approaches

Photonic and optical approaches leverage the quantum properties of light to process and store information. Here, the fundamental quantum particles are photons. Given that photons don't typically interact with their surroundings as easily as, say, electrons in a solid, they can be excellent carriers of quantum information.

## Photonic Qubits

Photonic qubits exploit the quantum properties of photons, which can exist in superposition states, just like other quantum systems.

1. **Encoding Information:** Photons have several degrees of freedom where quantum information can be encoded: polarization, time-bin, frequency, and orbital angular momentum, among others. For instance, a horizontal polarization might represent a `0`, while a vertical polarization represents a `1`.
2. **Generation and Detection:** Single photons can be generated through a variety of means, including parametric down-conversion in nonlinear crystals and quantum dots. On the detection end, single-photon detectors, which can register the arrival of individual photons, are used.
3. **Quantum Gates with Photons:** Photonic quantum gates can be a challenge since photons naturally don't interact with each other in free space. However, certain effects, like the Kerr effect in nonlinear media, can induce interactions. Alternatively, measurement-based approaches, where measurements can conditionally enact quantum gates, are also explored.
4. **Advantages & Challenges:** Photons are fast, can retain coherence over long distances, and are less susceptible to decoherence, making them perfect for quantum communication. However, building a fully photonic quantum computer is challenging due to difficulties in creating deterministic photon-photon interactions and efficiently storing photonic qubits.

## Boson Sampling:

Boson Sampling represents a specific task that quantum systems (using photons) can purportedly do more efficiently than classical computers. While it isn't universal quantum computing, demonstrating an advantage in Boson Sampling would be a step towards proving the quantum computational supremacy.

1. **Setup:** The setup for Boson Sampling involves sending multiple indistinguishable photons into a linear optical network (like an interferometer) and then measuring the output in multiple single-photon detectors.
2. **Task:** The task is to sample from the distribution of possible output patterns of the photons. The complexity arises due to the quantum interference of the multiple paths the photons can take.
3. **Significance:** While the task is relatively abstract and doesn't have direct practical applications, it's believed to be hard for classical computers. A quantum system that can perform Boson Sampling faster than a classical computer would showcase an instance of quantum advantage.
4. **Advancements & Controversies:** In recent years, there have been claims to achieving quantum advantage through Boson Sampling with 50-70 photons. However, these claims are not without controversies, with debates on the actual computational costs for classical systems and potential errors in the quantum setups.

**Conclusion:**
Photonic and optical quantum systems offer a unique avenue in the quantum computing landscape. Their inherent suitability for long-distance transmission makes them front-runners in quantum communication and teleportation. While building a fully photonic quantum computer remains a challenge, specific tasks like Boson Sampling provide avenues to showcase the strengths of quantum over classical processing in specific scenarios. Advances in integrated photonics, which miniaturize optical components onto chip-scale platforms, might further bolster the feasibility of large-scale photonic quantum computation in the future.
