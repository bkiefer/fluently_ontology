# Ontology adaptations for the Prima Additiva use case
This repository contains a top-level ontology (`cim.owl`) importing the original Fluently ontology created by University of Bath, and adds some concepts necessary for implementing the adaptive robot behaviour.

# Usage
For use with hfc or hfc-thrift, the n-triples files may need to be created from OWL XML files, if the OWL files are modified. For the current version, these files (with extension .nt) have been commited to the repository.

To do this, (under linux) install the raptor2 utilities:

    sudo apt install raptor2-utils

Then, run the following script in the root directory of the repository:

    ./ntcreate.sh

Now, you should be able to start an ontology server from hfc-thrift:

    <hfc-thrift-root>/bin/startServer -i -p 7777 fluently.yml

The `cimbase.nt` file is for experimentation purposes, to simply add instances needed for testing or demonstrating purposes. It's easier most of the time to immediately create n-triples in text form than an OWL file using, e.g., Protégé.
