# TNA_NETS
Clandestine Network Datasets


This collection consists of annotated networks developed from documents related to various terrorist attacks in India. Each dataset is named after a specific case and visualizes relationships and interactions among individual entities involved in these incidents. These networks are instrumental for analyzing key actors, hierarchies, and patterns within terrorist organizations. Below is an overview of each file:

 - **ClandestineNet1**: Captures the network associated with the 2001 Parliament attack in India. This dataset outlines connections between key individuals, detailing both direct and inferred associations critical for understanding the network structure behind this event.
 - **ClandestineNet2**: Documents the network based on the 2008 Mumbai 26/11 attacks. It highlights the coordination among individuals and entities involved in the planning and execution, giving insights into the operational dynamics of the group.
 - **ClandestineNet3**: Maps the network involved in the 1993 Bombay blasts, displaying connections between perpetrators, facilitators, and key locations involved in the coordinated attacks across Mumbai.
 - **ClandestineNet4**: Represents the network surrounding the 1996 Dausa blast, in which a bomb exploded in a Rajasthan State Transport Corporation (RSTC) bus traveling from Agra to Bikaner. The explosion occurred at Samleti village in Dausa district, Rajasthan, killing 14 people and injuring 37. The incident took place a day after a similar blast in Delhi’s Lajpat Nagar. This dataset captures the interactions among involved individuals and entities, shedding light on the logistical and operational aspects of this tragic event.
 - **ClandestineNet5**: Represents the network on the assassination of former Indian Prime Minister Rajiv Gandhi occurred on May 21, 1991, when a suicide bomber from the Liberation Tigers of Tamil Eelam (LTTE) detonated explosives near him during an election rally in Tamil Nadu. The attack was carried out as retaliation for India's involvement in the Sri Lankan Civil War, supporting the Sri Lankan government against the LTTE.
 - **ClandestineNet6**: Maps the network based on the 2006 Mumbai train bombings took place on July 11, when seven coordinated bomb blasts targeted local trains during rush hour, killing over 180 people and injuring more than 700. The attack was attributed to militant groups, including Lashkar-e-Taiba and Indian Mujahideen, with the aim of causing communal tension and widespread panic. 

These datasets are a resource for studying the structure and influence of clandestine networks in terrorist operations. They can support research on network centrality, influence analysis, and resilience, offering insights into the organizational dynamics of terror groups

## Reading Data
```{python}
import networkx as nx
import matplotlib.pyplot as plt

# Load the GML file
file_path = "<Dataset Path>"  # Replace with the path to your GML file
graph = nx.read_gml(file_path)

# Print basic information about the graph
print("Number of nodes:", graph.number_of_nodes())
print("Number of edges:", graph.number_of_edges())

# Visualize the graph
plt.figure(figsize=(10, 8))
nx.draw(graph, with_labels=True, node_size=500, node_color="skyblue", font_size=8, font_color="black", edge_color="gray")
plt.title("Network Graph from GML File")
plt.show()

```
