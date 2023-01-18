# Relational-GCN (RGCN)
Applying Relational-GCN for heterogenous datasets like Amazon, IMDB, DBLP, ACM.<br>
Paper: https://arxiv.org/abs/1703.06103

## Node Classification Task
```python
python3 entity_classify.py -d [DATASET] -e [EPOCHS] --testing --gpu [CPU/ GPU]
```
where DATASET = {amazon, imdb, dplp, imdb}, gpu = 0(CPU), -1(GPU)
### Example for running RGCN on Amazon data
```python
python3 entity_classify.py -d amazon --testing --gpu 0 
```
