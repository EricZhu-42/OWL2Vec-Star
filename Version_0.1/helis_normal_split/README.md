#### unzip files.tar.gz for relevant I/O files.

  1. train.csv, valid.csv and test.csv: training, validating and testing axioms from the original ontology helis.v1.00.origin.owl respectively.
  2. helis_v1.00.train.owl: ontology after training axioms are removed.
  3. helis_v1.00.train.projection.ttl: the projection of helis_v1.00.train.owl.
  4. classes.txt, individuals: all named classes and individuals respectively.
  5. annotations.txt, axioms: annotation axioms and normal declared axioms from helis.v1.00.train.owl respectively
  6. axioms_hermit.txt: all normal axioms plus those inferred by HermiT from helis.v1.00.train.owl
  7. inferred_classes.txt: all inferred classes of each testing individual except for its ground truth (declared class)
  8. Note that annotations.txt, axioms.txt, axioms_hermit.txt are generated by Ontology_Axioms_Annotations.java; herlis_v1.00.train.projection.ttl is generated by Ontology_Projector.java; train.csv, valid.csv, test.csv, classes.txt, individuals and inferred_classes.txt are generated by ClassAssertion_NormalSplit.java

#### To reproduce OWL2Vec Star results, see examples in OWL2Vec_Plus_Run.sh

#### To reproduce RDF2Vec (or other baselines), see example in RDF2Vec_Run.sh (or other scripts accordingly)

#### For TransR/DistMult/TransE, please train the embeddings by OpenKE, and set the learned embedding file in Baselines.py. 

#### For Quantum Embedding, please train the embeddings by its [codes](https://github.com/IBM/e2r/tree/master/neurips2019) or use the embeddings trained by us under qembeddings-27000iters, and then simply run Quantum_Run.sh
