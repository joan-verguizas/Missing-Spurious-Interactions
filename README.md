# Missing and Spurious Interactions in Complex Networks

### Course: Information Theory and Inference (2023-2024)  
### Master's Degree: Physics of Data, University of Padova (IT)

## Overview

This project was developed as part of the final exam for the Information Theory and Inference course during the academic year 2023-2024. The work was carried out individually during my second year in the Master's degree program in *Physics of Data* at the University of Padova.

The goal of the project is to address the challenge of network reliability by developing a model that detects spurious and missing links (edges) between nodes in a complex network. Network reliability is a significant issue when analyzing real-world networks, as data imperfections often lead to incomplete or erroneous observations of network structures.

To tackle this, we implemented the model developed by [R. Guimerà et al.](https://www.pnas.org/doi/10.1073/pnas.0908366106), which has been proven effective for such tasks. This model was applied to two well-known and extensively studied complex networks:
- **[The Karate Club Network](https://www.jstor.org/stable/3629752)**: A social network of friendships between members of a karate club, famously studied by Wayne Zachary.
- **[The Dolphins Network](https://link.springer.com/article/10.1007/s00265-003-0651-y)**: A social network representing interactions among a group of dolphins in New Zealand.

By applying this model, the project aims to improve the understanding and reliability of the network structures, thereby aiding in better analysis and decision-making in fields where network data is critical.

## Methods and Models

The core of this project is based on the work of [A. Guimerà et al.](https://www.nature.com/articles/nature01939), who proposed a model to infer missing and spurious links in complex networks by leveraging both local and global network properties. The approach takes into account various network attributes, such as node connectivity and community structure, to improve the detection of anomalies and missing links. The overall strategy is as follows:

- Initialize the network with a random community structure.
- Use a Metropolis Algorithm in order to obtain a sample of the partitions.
- Create a fake observed network using the true data with a certain number of either missing or spurious interactions.
- Compute the reliability for each possible connection.
- Calculate the accuracy at detecting spurious/missing interactions using the true network.
- Repeat the process for different fraction of missing/spurious interactions as well as for a number of iterations for better results.

## Conclusion

The project is able to recover both the spurious and missing interactions quite effectively. As expected as the number of either missing/spurious interactions grows the accuracy of the model diminishes. But even with that, this model can be applied to improve the reliability of network data, to ensure more accurate and meaningful results in network analysis.

