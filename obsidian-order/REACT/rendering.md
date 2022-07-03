# rendering
Rendering is a process when React finds out how the layout tree should be, it happens when mounting and updating. During the update, Reconciliation is executed to collect the difference between the new tree and the old tree, once a component is marked needing update, React re-renders all of its children, even those child components stay unchanged. In this regard, wasted renders appear and might cost much effort,

#REACT #rendering