[![arXiv](https://img.shields.io/badge/arXiv-2404.07344-orange.svg?style=plastic)](https://arxiv.org/abs/2404.07344)
[![Video](http://img.shields.io/badge/video-1min-green.svg?style=plastic)](https://drive.google.com/file/d/1LNwkGz3Jj9cxx5AZNUekmo0SnyXVAyS3/view?usp=sharing)

<p align="center">
  <img src="_src_images/actsel_github_banner.png" alt="Action Selection algorithm to explore the physical properties in broader term.">
</p>

# ACTSEL source code repository
We introduce ACTSEL. A method for automatic selection of actions that help optimally determine physical object properties that are not readily available through vision. Originally part of the publication:   **Interactive Learning of Physical Object Properties Through Robot Manipulation and Database of Object Measurements**
### Link to paper
Link to [arXiv](https://arxiv.org/abs/2404.07344).

## Graphical model overview
<p align="center">
  <img src="_src_images/actsel_general_diagram.png" alt="General diagram of ACTSEL algorithm in action."
  height="250"
  style="margin-right: 20px;">
  <img src="_src_images/actsel_actions_network.png" alt="Bayesian network" height="250">
</p>
<p align="center">
  <em>General overview of the algorithm (left), Bayesian network and action relations (right)</em>
</p>

## Running the model
> For best experience install conda environment as `numpy`, `scipy` and `scikit-learn` are needed for algorithm operation
  1) To run the model, fill in the templates for nodes, actions and their relevant confusion matrices in `configs/templates`. In order to update the actual config `.json` files, run the `scripts/templates_to_cfgs.py` from root directory as:
  ```
  python3 scripts/templates_to_cfgs.py
  ```

  2) Customize the `main.py` to meet your action and object requirements byt customizing `experiment_object_names` and action to node mapping.

### Implementation remarks
The algorithm and results presented in the paper were obtained offline on pre-measured dataset for broader statistical understanding. This fact is reflected in `main.py`.


### Citation
Please cite this paper as:
```
@article{kruzliak2024interactive,
      title={Interactive Learning of Physical Object Properties Through Robot Manipulation and Database of Object Measurements}, 
      author={Andrej Kruzliak and Jiri Hartvich and Shubhan P. Patni and Lukas Rustler and Jan Kristof Behrens and Fares J. Abu-Dakka and Krystian Mikolajczyk and Ville Kyrki and Matej Hoffmann},
      year={2024},
      eprint={2404.07344},
      archivePrefix={arXiv},
      primaryClass={cs.RO}
}
```

