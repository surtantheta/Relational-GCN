# Relational-GCN (RGCN)
Applying Relational-GCN for heterogenous datasets like Amazon, IMDB, DBLP, ACM.<br>
Paper: https://arxiv.org/abs/1703.06103 <br>
Popular datasets include Amazon, DBLP, IMDb and ACM.
## Node Classification Task
```python
python3 entity_classify.py -d [DATASET] -e [EPOCHS] --testing --gpu [CPU/ GPU]
```
where DATASET = {amazon, imdb, dplp, imdb}, gpu = 0(CPU), -1(GPU)
### Example for running RGCN on Amazon data
```python
python3 entity_classify.py -d amazon --testing --gpu 0 
```
## Dataset Statistics
### ACM
<table>
  <tr>
    <th>author</th>
    <th>paper</th>
    <th>Subject</th>
    <th>Paper-Author</th>
    <th>Paper-Subject</th>
    <th>Features</th>
    <th>Train</th>
    <th>Val</th>
    <th>Test</th>

  </tr>
  <tr>
    <td>5,912</td>
    <td>3,025	</td>
    <td>57</td>
    <td>9,936</td>
    <td>3,025</td>
    <td>1,902</td>
    <td>600</td>
    <td>300</td>
    <td>2,125</td>
  </tr>
</table>
					Train	Val	Test
### IMDb
<table>
  <tr>
    <th>Movie</th>
    <th>Actor</th>
    <th>Director</th>
    <th>Movie-Actor</th>
    <th>Movie-Director</th>
    <th>Train</th>
    <th>Val</th>
    <th>Test</th>

  </tr>
  <tr>
    <td>4,780	</td>
    <td>5,841	</td>
    <td>2,269</td>
    <td>14,340</td>
    <td>4,780</td>
    <td>300</td>
    <td>300</td>
    <td>2,687</td>
  </tr>
</table>
