# NPG_kgraph

Go to the root directory of DNG and make.    

```shell
cd NPG_kgraph/
mkdir build && cd build
cmake ..
make
```

## How To Use

### Build DNG 
First: 

```shell
cd NPG_kgraph/build/tests/
```

Then: 

```shell
./test_dng_index data_file save_graph K L iter S R RANGE PL B M
```

 Meaning of the parameters:    

    **data_file** is the path of the origin data.
    **save_graph** is the path of the DNG to be saved.
    **K** is the 'K' of kNN graph.
    **L** is the parameter controlling the graph quality, larger is more accurate but slower, no smaller than K.
    **iter** is the parameter controlling the iteration times, iter usually < 30.
    **S** is the parameter contollling the graph quality, larger is more accurate but slower.
    **R** is the parameter controlling the graph quality, larger is more accurate but slower.
    **RANGE** controls the index size of the graph, the best R is related to the intrinsic dimension of the dataset.
    **PL** controls the quality of the DNG, the larger the better.
    **B** controls the quality of the DNG.
    **M** control the edge selection of DNG.

### DNG Search
```shell
./test_dng_optimized_search graph_path data_path query_path groundtruth_path
```

 Meaning of the parameters:    

```
graph_path is the path of the pre-built DNG.
data_path is the path of the origin data.
query_path is the path of the query data.
groundtruth_path is the path of the groundtruth data.
```
### DNG hybrid_Search
```shell
./test_dng_hybrid_search graph_path data_path query_path base_att_path query_att_path groundtruth_path
```

 Meaning of the parameters:  

```
graph_path is the path of the pre-built DNG.
data_path is the path of the origin data.
query_path is the path of the query data.
base_att_path is the path of the corresponding structured labels of the origin data.
query_att_path is the path of the corresponding structured labels of the query data.
groundtruth_path is the path of the groundtruth data.
```

