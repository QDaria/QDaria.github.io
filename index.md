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
![D25C](_static/D25C.png)
```

::::
:::::


---

```{code-cell} ipython3
:tags: [hide-input]

data = {
    "name": "Quantum Computers",
    "children": [
        {
            "name": "Spin Qubit",
            "description": "Utilizes the spin of electrons to represent qubits.",
            "children": [
                {"name": "Silicon Spin Qubits", "description": "Operate in silicon."},
                {"name": "Quantum Dot Spin Qubits", "description": "Operate using quantum dots."}
            ]
        },
        {
            "name": "Photonic",
            "description": "Uses photons for computation, inherently quantum in nature."
        },
        {
            "name": "NV Center",
            "description": "Uses nitrogen vacancy centers in diamond."
        },
        {
            "name": "Superconducting",
            "description": "Uses circuits made of superconducting materials.",
            "children": [
                {"name": "Transmon Qubits", "description": "A type of superconducting qubit."},
                {"name": "Flux Qubits", "description": "Another type of superconducting qubit."}
            ]
        },
        {
            "name": "Topological",
            "description": "Uses anyons and braiding for computation.",
            "children": [
                {"name": "Anyons", "description": "Quasiparticles used in topological quantum computing."}
            ]
        }
    ]
}

width_increase = 1.2
height_increase = 1.2
import pandas as pd
import plotly.express as px

# Convert nested dictionary into a flat DataFrame
def flatten(data, parent="", path=[]):
    rows = []
    name = data["name"]
    description = data.get("description", "")
    new_path = path + [name]
    rows.append({"id": "/".join(new_path), "parent": "/".join(path), "name": name, "description": description})
    for child in data.get("children", []):
        rows.extend(flatten(child, name, new_path))
    return rows

df = pd.DataFrame(flatten(data))

# Define base width and height
base_width = 500
base_height = 500

# Assigning a numerical value for visualization purpose
df['value'] = 1

#width_increase = 1.3
#height_increase = 1.3

# Treemap
fig1 = px.treemap(df, path=['parent', 'id'], values='value', title="Types of Quantum Computers Treemap", hover_data=['description'])
fig1.update_layout(width=base_width * width_increase, height=base_height * height_increase)
fig1.show()

# Sunburst
fig2 = px.sunburst(df, path=['parent', 'id'], values='value', title="Types of Quantum Computers Sunburst", hover_data=['description'])
fig2.update_layout(width=base_width * width_increase, height=base_height * height_increase)
fig2.show()

# Increase factor

#width_increase = 1.3
#height_increase = 1.3

# Adjusted width and height

adjusted_width = base_width *width_increase
adjusted_height = base_height* height_increase

# Treemap

fig1 = px.treemap(df, path=['parent', 'id'], values='value', color='id',
                  title="Types of Quantum Computers Treemap",
                  hover_data=['description'],
                  color_discrete_sequence=px.colors.qualitative.Set3)
fig1.update_layout(width=adjusted_width, height=adjusted_height)
fig1.show()

# Sunburst

fig2 = px.sunburst(df, path=['parent', 'id'], values='value', color='id',
                   title="Types of Quantum Computers Sunburst",
                   hover_data=['description'],
                   color_discrete_sequence=px.colors.qualitative.Set3)
fig2.update_layout(width=adjusted_width, height=adjusted_height)
fig2.show()

```


```{tableofcontents}
```

```{nb-exec-table}
```

[![Jupyter Book Badge](https://jupyterbook.org/badge.svg)](<https://qdaria.com/intro.html>)

::::{grid-item-card}
:shadow: lg

```{admonition} Introduction
Welcome to our comprehensive guide on Quantum Technology and its implications in the world of computing. This book provides insights into our core values, our mission, and dives deep into the technical aspects of quantum mechanics applied to computing. See also [D. Mo Houshmand interactive lectures on Quantum Hardware and Quantum Machine Learning](http://www.mohoushmand.com/).
- We welcome and appreciate all forms of feedback - if you spot any errors, typos, or see opportunities for improvement, please do not hesitate to share!
```

::::
