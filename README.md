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
<ul>
  <li> <b>ACM</b>
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
</li>
  <li><b>IMDb</b>
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
</li>
  <li><b>DBLP</b>
<table>
  <tr>
    <th>author</th>
    <th>paper</th>
    <th>Conf</th>
    <th>Venue</th>
    <th>Paper-Author</th>
    <th>Paper-Conf</th>
    <th>Paper-Term</th>
    <th>Train</th>
    <th>Val</th>
    <th>Test</th>

  </tr>
  <tr>
    <td>4,057	</td>
    <td>14,328	</td>
    <td>20</td>
    <td>8,789</td>
    <td>19,645</td>
    <td>14,328</td>
    <td>88,420</td>
    <td>800</td>
    <td>400</td>
    <td>2,857</td>
  </tr>
</table>
</li>
  <li><b>Fraud Amazon Dataset </b><br>
    The Amazon dataset includes product reviews under the Musical Instruments category. Users with more than 80% helpful votes are labelled as benign entities and users with less than 20% helpful votes are labelled as fraudulent entities. A fraudulent user detection task can be conducted on the Amazon dataset, which is a binary classification task. 25 handcrafted features from <https://arxiv.org/pdf/2005.10150.pdf> are taken as the raw node features .

Users are nodes in the graph, and three relations are: 1. U-P-U : it connects users reviewing at least one same product 2. U-S-U : it connects users having at least one same star rating within one week 3. U-V-U : it connects users with top 5% mutual review text similarities (measured by TF-IDF) among all users.
<table>
  <tr>
    <th>Nodes</th>
    <th>U-P-U</th>
    <th>U-S-U</th>
    <th>U-V-U</th>
    <th>Positive (fraudulent)</th>
    <th>Negative (benign)</th>
    <th>Unlabeled</th>
  </tr>
  <tr>
    <td>11,944	</td>
    <td>351,216	</td>
    <td>7,132,958</td>
    <td>2,073,474</td>
    <td>821</td>
    <td>7,818</td>
    <td>3,305</td>
  </tr>
</table>
</li>
</ul>
