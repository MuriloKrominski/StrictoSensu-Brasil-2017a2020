Por Murilo Krominski.

## RESULTADO: https://murilokrominski.github.io/StrictoSensu-Brasil-2017a2020/

# [2017 a 2020] Programas da Pós-Graduação Stricto Sensu no Brasil<br>
Os dados da seção contêm informações sobre os programas de pós-graduação stricto sensu no Brasil.

Esta versão apresenta os dados para os anos de 2017 e 2018, os dois primeiros anos do novo período de avaliação, e será atualizada até completar-se os quatro anos do ciclo (2017-2020).<br>

## DADOS e METADADOS.
Ultima atualização:	25-Junho-2020<br>
Criado:	10-Outubro-2019<br>
Formato:	CSV<br>
Licença:	Creative Commons Attribution<br>
ID:	0f1737bd-6227-4193-9d11-0f9e981e9789<br>
Package ID:	903b4215-ea91-4927-8975-d1484891374f<br>
Revision ID:	995258cb-3743-4fef-9011-964c73e7c9c7<br>
State:	active<br>

br-capes-colsucup-prog-2018-2020-06-12.csv
https://dadosabertos.capes.gov.br/dataset/903b4215-ea91-4927-8975-d1484891374f/resource/0f1737bd-6227-4193-9d11-0f9e981e9789/download/br-capes-colsucup-prog-2018-2020-06-12.csv

ddi-documentation-portuguese-165.pdf
https://metadados.capes.gov.br/index.php/catalog/165

4357 rows × 32 columns

# Procedimento


```python
!pip install --upgrade pandas
```

    Collecting pandas
      Downloading pandas-1.1.4-cp38-cp38-win_amd64.whl (8.9 MB)
    Requirement already satisfied, skipping upgrade: pytz>=2017.2 in c:\programdata\anaconda3\lib\site-packages (from pandas) (2020.1)
    Requirement already satisfied, skipping upgrade: numpy>=1.15.4 in c:\programdata\anaconda3\lib\site-packages (from pandas) (1.19.2)
    Requirement already satisfied, skipping upgrade: python-dateutil>=2.7.3 in c:\programdata\anaconda3\lib\site-packages (from pandas) (2.8.1)
    Requirement already satisfied, skipping upgrade: six>=1.5 in c:\programdata\anaconda3\lib\site-packages (from python-dateutil>=2.7.3->pandas) (1.15.0)
    Installing collected packages: pandas
      Attempting uninstall: pandas
        Found existing installation: pandas 1.1.3
        Uninstalling pandas-1.1.3:
          Successfully uninstalled pandas-1.1.3
    Successfully installed pandas-1.1.4
    


```python
import pandas as pd
```


```python
url = 'https://dadosabertos.capes.gov.br/dataset/903b4215-ea91-4927-8975-d1484891374f/resource/0f1737bd-6227-4193-9d11-0f9e981e9789/download/br-capes-colsucup-prog-2018-2020-06-12.csv'
```


```python
dados = pd.read_csv(url, sep=';', encoding='latin-1')
```


```python
dados.shape
```




    (4357, 32)




```python
dados.columns = ["AN_BASE","NM_GRANDE_AREA_CONHECIMENTO","NM_AREA_CONHECIMENTO","NM_AREA_BASICA","NM_SUBAREA_CONHECIMENTO","NM_ESPECIALIDADE","CD_AREA_AVALIACAO","NM_AREA_AVALIACAO","CD_ENTIDADE_CAPES","CD_ENTIDADE_EMEC","SG_ENTIDADE_ENSINO","NM_ENTIDADE_ENSINO","IN_REDE","SG_ENTIDADE_ENSINO_REDE","CS_STATUS_JURIDICO","DS_DEPENDENCIA_ADMINISTRATIVA","DS_ORGANIZACAO_ACADEMICA","NM_REGIAO","SG_UF_PROGRAMA","NM_MUNICIPIO_PROGRAMA_IES","NM_MODALIDADE_PROGRAMA","CD_PROGRAMA_IES","NM_PROGRAMA_IES","NM_PROGRAMA_IDIOMA","NM_GRAU_PROGRAMA","CD_CONCEITO_PROGRAMA","AN_INICIO_PROGRAMA","AN_INICIO_CURSO","DS_SITUACAO_PROGRAMA","DT_SITUACAO_PROGRAMA","ID_ADD_FOTO_PROGRAMA_IES","ID_ADD_FOTO_PROGRAMA"]
```


```python
dados.head()
```





<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>AN_BASE</th>
      <th>NM_GRANDE_AREA_CONHECIMENTO</th>
      <th>NM_AREA_CONHECIMENTO</th>
      <th>NM_AREA_BASICA</th>
      <th>NM_SUBAREA_CONHECIMENTO</th>
      <th>NM_ESPECIALIDADE</th>
      <th>CD_AREA_AVALIACAO</th>
      <th>NM_AREA_AVALIACAO</th>
      <th>CD_ENTIDADE_CAPES</th>
      <th>CD_ENTIDADE_EMEC</th>
      <th>...</th>
      <th>NM_PROGRAMA_IES</th>
      <th>NM_PROGRAMA_IDIOMA</th>
      <th>NM_GRAU_PROGRAMA</th>
      <th>CD_CONCEITO_PROGRAMA</th>
      <th>AN_INICIO_PROGRAMA</th>
      <th>AN_INICIO_CURSO</th>
      <th>DS_SITUACAO_PROGRAMA</th>
      <th>DT_SITUACAO_PROGRAMA</th>
      <th>ID_ADD_FOTO_PROGRAMA_IES</th>
      <th>ID_ADD_FOTO_PROGRAMA</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2018</td>
      <td>MULTIDISCIPLINAR</td>
      <td>CIÊNCIAS AMBIENTAIS</td>
      <td>CIÊNCIAS AMBIENTAIS</td>
      <td>NÃO SE APLICA</td>
      <td>NÃO SE APLICA</td>
      <td>49</td>
      <td>CIÊNCIAS AMBIENTAIS</td>
      <td>53001010</td>
      <td>2</td>
      <td>...</td>
      <td>DESENVOLVIMENTO SUSTENTÁVEL</td>
      <td>SUSTAINABLE DEVELOPMENT</td>
      <td>MESTRADO/DOUTORADO</td>
      <td>7</td>
      <td>1996</td>
      <td>1998/1996</td>
      <td>EM FUNCIONAMENTO</td>
      <td>27FEB2013:00:00:00</td>
      <td>137750</td>
      <td>73634</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2018</td>
      <td>ENGENHARIAS</td>
      <td>ENGENHARIA CIVIL</td>
      <td>ENGENHARIA CIVIL</td>
      <td>NÃO SE APLICA</td>
      <td>NÃO SE APLICA</td>
      <td>10</td>
      <td>ENGENHARIAS I</td>
      <td>32005016</td>
      <td>576</td>
      <td>...</td>
      <td>ENGENHARIA CIVIL</td>
      <td>POST-GRADUATE PROGRAM IN CIVIL ENGINEERING</td>
      <td>MESTRADO</td>
      <td>3</td>
      <td>2017</td>
      <td>2017</td>
      <td>EM FUNCIONAMENTO</td>
      <td>06MAR2017:00:00:00</td>
      <td>137737</td>
      <td>73622</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2018</td>
      <td>ENGENHARIAS</td>
      <td>ENGENHARIA MECÂNICA</td>
      <td>ENGENHARIA MECÂNICA</td>
      <td>NÃO SE APLICA</td>
      <td>NÃO SE APLICA</td>
      <td>13</td>
      <td>ENGENHARIAS III</td>
      <td>42046017</td>
      <td>5322</td>
      <td>...</td>
      <td>ENGENHARIA</td>
      <td>GRADUATE PROGRAM IN ENGINEERING</td>
      <td>MESTRADO</td>
      <td>3</td>
      <td>2011</td>
      <td>2011</td>
      <td>EM FUNCIONAMENTO</td>
      <td>23APR2012:00:00:00</td>
      <td>138443</td>
      <td>74281</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2018</td>
      <td>CIÊNCIAS DA SAÚDE</td>
      <td>ODONTOLOGIA</td>
      <td>ODONTOLOGIA</td>
      <td>NÃO SE APLICA</td>
      <td>NÃO SE APLICA</td>
      <td>18</td>
      <td>ODONTOLOGIA</td>
      <td>33063010</td>
      <td>322</td>
      <td>...</td>
      <td>ODONTOLOGIA</td>
      <td>PROGRAMME OF MASTER¿S DEGREE COURSE IN DENTISTRY</td>
      <td>MESTRADO/DOUTORADO</td>
      <td>4</td>
      <td>1993</td>
      <td>1993/2015</td>
      <td>EM FUNCIONAMENTO</td>
      <td>29OCT2012:00:00:00</td>
      <td>138620</td>
      <td>74392</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2018</td>
      <td>CIÊNCIAS SOCIAIS APLICADAS</td>
      <td>PLANEJAMENTO URBANO E REGIONAL</td>
      <td>PLANEJAMENTO URBANO E REGIONAL</td>
      <td>NÃO SE APLICA</td>
      <td>NÃO SE APLICA</td>
      <td>30</td>
      <td>PLANEJAMENTO URBANO E REGIONAL / DEMOGRAFIA</td>
      <td>41002016</td>
      <td>43</td>
      <td>...</td>
      <td>PLANEJAMENTO TERRITORIAL E DESENVOLVIMENTO SÓC...</td>
      <td>TERRITORIAL PLANNING AND SOCIO ENVIRONMENTAL D...</td>
      <td>DOUTORADO</td>
      <td>4</td>
      <td>2016</td>
      <td>2016</td>
      <td>EM FUNCIONAMENTO</td>
      <td>14APR2016:00:00:00</td>
      <td>138696</td>
      <td>74468</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 32 columns</p>
</div>




```python
#!pip install pandas-profiling
!pip install https://github.com/pandas-profiling/pandas-profiling/archive/master.zip
```

    Collecting https://github.com/pandas-profiling/pandas-profiling/archive/master.zip
      Downloading https://github.com/pandas-profiling/pandas-profiling/archive/master.zip
    Requirement already satisfied (use --upgrade to upgrade): pandas-profiling==2.9.0 from https://github.com/pandas-profiling/pandas-profiling/archive/master.zip in c:\programdata\anaconda3\lib\site-packages
    Requirement already satisfied: joblib in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (0.17.0)
    Requirement already satisfied: scipy>=1.4.1 in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (1.5.0)
    Requirement already satisfied: pandas!=1.0.0,!=1.0.1,!=1.0.2,!=1.1.0,>=0.25.3 in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (1.1.4)
    Requirement already satisfied: matplotlib>=3.2.0 in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (3.3.2)
    Requirement already satisfied: confuse>=1.0.0 in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (1.3.0)
    Requirement already satisfied: jinja2>=2.11.1 in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (2.11.2)
    Requirement already satisfied: visions[type_image_path]==0.5.0 in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (0.5.0)
    Requirement already satisfied: numpy>=1.16.0 in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (1.19.2)
    Requirement already satisfied: attrs>=19.3.0 in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (20.2.0)
    Requirement already satisfied: htmlmin>=0.1.12 in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (0.1.12)
    Requirement already satisfied: missingno>=0.4.2 in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (0.4.2)
    Requirement already satisfied: phik>=0.9.10 in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (0.10.0)
    Requirement already satisfied: tangled-up-in-unicode>=0.0.6 in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (0.0.6)
    Requirement already satisfied: requests>=2.23.0 in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (2.24.0)
    Requirement already satisfied: tqdm>=4.43.0 in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (4.50.2)
    Requirement already satisfied: ipywidgets>=7.5.1 in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (7.5.1)
    Requirement already satisfied: seaborn>=0.10.1 in c:\programdata\anaconda3\lib\site-packages (from pandas-profiling==2.9.0) (0.11.0)
    Requirement already satisfied: pytz>=2017.2 in c:\programdata\anaconda3\lib\site-packages (from pandas!=1.0.0,!=1.0.1,!=1.0.2,!=1.1.0,>=0.25.3->pandas-profiling==2.9.0) (2020.1)
    Requirement already satisfied: python-dateutil>=2.7.3 in c:\programdata\anaconda3\lib\site-packages (from pandas!=1.0.0,!=1.0.1,!=1.0.2,!=1.1.0,>=0.25.3->pandas-profiling==2.9.0) (2.8.1)
    Requirement already satisfied: cycler>=0.10 in c:\programdata\anaconda3\lib\site-packages (from matplotlib>=3.2.0->pandas-profiling==2.9.0) (0.10.0)
    Requirement already satisfied: kiwisolver>=1.0.1 in c:\programdata\anaconda3\lib\site-packages (from matplotlib>=3.2.0->pandas-profiling==2.9.0) (1.2.0)
    Requirement already satisfied: pillow>=6.2.0 in c:\programdata\anaconda3\lib\site-packages (from matplotlib>=3.2.0->pandas-profiling==2.9.0) (8.0.1)
    Requirement already satisfied: certifi>=2020.06.20 in c:\programdata\anaconda3\lib\site-packages (from matplotlib>=3.2.0->pandas-profiling==2.9.0) (2020.6.20)
    Requirement already satisfied: pyparsing!=2.0.4,!=2.1.2,!=2.1.6,>=2.0.3 in c:\programdata\anaconda3\lib\site-packages (from matplotlib>=3.2.0->pandas-profiling==2.9.0) (2.4.7)
    Requirement already satisfied: pyyaml in c:\programdata\anaconda3\lib\site-packages (from confuse>=1.0.0->pandas-profiling==2.9.0) (5.3.1)
    Requirement already satisfied: MarkupSafe>=0.23 in c:\programdata\anaconda3\lib\site-packages (from jinja2>=2.11.1->pandas-profiling==2.9.0) (1.1.1)
    Requirement already satisfied: networkx>=2.4 in c:\programdata\anaconda3\lib\site-packages (from visions[type_image_path]==0.5.0->pandas-profiling==2.9.0) (2.5)
    Requirement already satisfied: imagehash; extra == "type_image_path" in c:\programdata\anaconda3\lib\site-packages (from visions[type_image_path]==0.5.0->pandas-profiling==2.9.0) (4.1.0)
    Requirement already satisfied: numba>=0.38.1 in c:\programdata\anaconda3\lib\site-packages (from phik>=0.9.10->pandas-profiling==2.9.0) (0.51.2)
    Requirement already satisfied: urllib3!=1.25.0,!=1.25.1,<1.26,>=1.21.1 in c:\programdata\anaconda3\lib\site-packages (from requests>=2.23.0->pandas-profiling==2.9.0) (1.25.11)
    Requirement already satisfied: chardet<4,>=3.0.2 in c:\programdata\anaconda3\lib\site-packages (from requests>=2.23.0->pandas-profiling==2.9.0) (3.0.4)
    Requirement already satisfied: idna<3,>=2.5 in c:\programdata\anaconda3\lib\site-packages (from requests>=2.23.0->pandas-profiling==2.9.0) (2.10)
    Requirement already satisfied: ipython>=4.0.0; python_version >= "3.3" in c:\programdata\anaconda3\lib\site-packages (from ipywidgets>=7.5.1->pandas-profiling==2.9.0) (7.18.1)
    Requirement already satisfied: nbformat>=4.2.0 in c:\programdata\anaconda3\lib\site-packages (from ipywidgets>=7.5.1->pandas-profiling==2.9.0) (5.0.8)
    Requirement already satisfied: widgetsnbextension~=3.5.0 in c:\programdata\anaconda3\lib\site-packages (from ipywidgets>=7.5.1->pandas-profiling==2.9.0) (3.5.1)
    Requirement already satisfied: traitlets>=4.3.1 in c:\programdata\anaconda3\lib\site-packages (from ipywidgets>=7.5.1->pandas-profiling==2.9.0) (5.0.5)
    Requirement already satisfied: ipykernel>=4.5.1 in c:\programdata\anaconda3\lib\site-packages (from ipywidgets>=7.5.1->pandas-profiling==2.9.0) (5.3.4)
    Requirement already satisfied: six>=1.5 in c:\programdata\anaconda3\lib\site-packages (from python-dateutil>=2.7.3->pandas!=1.0.0,!=1.0.1,!=1.0.2,!=1.1.0,>=0.25.3->pandas-profiling==2.9.0) (1.15.0)
    Requirement already satisfied: decorator>=4.3.0 in c:\programdata\anaconda3\lib\site-packages (from networkx>=2.4->visions[type_image_path]==0.5.0->pandas-profiling==2.9.0) (4.4.2)
    Requirement already satisfied: PyWavelets in c:\programdata\anaconda3\lib\site-packages (from imagehash; extra == "type_image_path"->visions[type_image_path]==0.5.0->pandas-profiling==2.9.0) (1.1.1)
    Requirement already satisfied: llvmlite<0.35,>=0.34.0.dev0 in c:\programdata\anaconda3\lib\site-packages (from numba>=0.38.1->phik>=0.9.10->pandas-profiling==2.9.0) (0.34.0)
    Requirement already satisfied: setuptools in c:\programdata\anaconda3\lib\site-packages (from numba>=0.38.1->phik>=0.9.10->pandas-profiling==2.9.0) (50.3.0.post20201006)
    Requirement already satisfied: prompt-toolkit!=3.0.0,!=3.0.1,<3.1.0,>=2.0.0 in c:\programdata\anaconda3\lib\site-packages (from ipython>=4.0.0; python_version >= "3.3"->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (3.0.8)
    Requirement already satisfied: colorama; sys_platform == "win32" in c:\programdata\anaconda3\lib\site-packages (from ipython>=4.0.0; python_version >= "3.3"->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.4.4)
    Requirement already satisfied: pickleshare in c:\programdata\anaconda3\lib\site-packages (from ipython>=4.0.0; python_version >= "3.3"->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.7.5)
    Requirement already satisfied: backcall in c:\programdata\anaconda3\lib\site-packages (from ipython>=4.0.0; python_version >= "3.3"->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.2.0)
    Requirement already satisfied: jedi>=0.10 in c:\programdata\anaconda3\lib\site-packages (from ipython>=4.0.0; python_version >= "3.3"->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.17.1)
    Requirement already satisfied: pygments in c:\programdata\anaconda3\lib\site-packages (from ipython>=4.0.0; python_version >= "3.3"->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (2.7.1)
    Requirement already satisfied: jupyter-core in c:\programdata\anaconda3\lib\site-packages (from nbformat>=4.2.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (4.6.3)
    Requirement already satisfied: ipython-genutils in c:\programdata\anaconda3\lib\site-packages (from nbformat>=4.2.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.2.0)
    Requirement already satisfied: jsonschema!=2.5.0,>=2.4 in c:\programdata\anaconda3\lib\site-packages (from nbformat>=4.2.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (3.2.0)
    Requirement already satisfied: notebook>=4.4.1 in c:\programdata\anaconda3\lib\site-packages (from widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (6.1.4)
    Requirement already satisfied: jupyter-client in c:\programdata\anaconda3\lib\site-packages (from ipykernel>=4.5.1->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (6.1.7)
    Requirement already satisfied: tornado>=4.2 in c:\programdata\anaconda3\lib\site-packages (from ipykernel>=4.5.1->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (6.0.4)
    Requirement already satisfied: wcwidth in c:\programdata\anaconda3\lib\site-packages (from prompt-toolkit!=3.0.0,!=3.0.1,<3.1.0,>=2.0.0->ipython>=4.0.0; python_version >= "3.3"->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.2.5)
    Requirement already satisfied: parso<0.8.0,>=0.7.0 in c:\programdata\anaconda3\lib\site-packages (from jedi>=0.10->ipython>=4.0.0; python_version >= "3.3"->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.7.0)
    Requirement already satisfied: pywin32>=1.0; sys_platform == "win32" in c:\programdata\anaconda3\lib\site-packages (from jupyter-core->nbformat>=4.2.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (227)
    Requirement already satisfied: pyrsistent>=0.14.0 in c:\programdata\anaconda3\lib\site-packages (from jsonschema!=2.5.0,>=2.4->nbformat>=4.2.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.17.3)
    Requirement already satisfied: Send2Trash in c:\programdata\anaconda3\lib\site-packages (from notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (1.5.0)
    Requirement already satisfied: pyzmq>=17 in c:\programdata\anaconda3\lib\site-packages (from notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (19.0.2)
    Requirement already satisfied: terminado>=0.8.3 in c:\programdata\anaconda3\lib\site-packages (from notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.9.1)
    Requirement already satisfied: argon2-cffi in c:\programdata\anaconda3\lib\site-packages (from notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (20.1.0)
    Requirement already satisfied: nbconvert in c:\programdata\anaconda3\lib\site-packages (from notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (6.0.7)
    Requirement already satisfied: prometheus-client in c:\programdata\anaconda3\lib\site-packages (from notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.8.0)
    Requirement already satisfied: pywinpty>=0.5 in c:\programdata\anaconda3\lib\site-packages (from terminado>=0.8.3->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.5.7)
    Requirement already satisfied: cffi>=1.0.0 in c:\programdata\anaconda3\lib\site-packages (from argon2-cffi->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (1.14.3)
    Requirement already satisfied: pandocfilters>=1.4.1 in c:\programdata\anaconda3\lib\site-packages (from nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (1.4.2)
    Requirement already satisfied: jupyterlab-pygments in c:\programdata\anaconda3\lib\site-packages (from nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.1.2)
    Requirement already satisfied: nbclient<0.6.0,>=0.5.0 in c:\programdata\anaconda3\lib\site-packages (from nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.5.1)
    Requirement already satisfied: mistune<2,>=0.8.1 in c:\programdata\anaconda3\lib\site-packages (from nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.8.4)
    Requirement already satisfied: defusedxml in c:\programdata\anaconda3\lib\site-packages (from nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.6.0)
    Requirement already satisfied: bleach in c:\programdata\anaconda3\lib\site-packages (from nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (3.2.1)
    Requirement already satisfied: testpath in c:\programdata\anaconda3\lib\site-packages (from nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.4.4)
    Requirement already satisfied: entrypoints>=0.2.2 in c:\programdata\anaconda3\lib\site-packages (from nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.3)
    Requirement already satisfied: pycparser in c:\programdata\anaconda3\lib\site-packages (from cffi>=1.0.0->argon2-cffi->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (2.20)
    Requirement already satisfied: nest-asyncio in c:\programdata\anaconda3\lib\site-packages (from nbclient<0.6.0,>=0.5.0->nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (1.4.1)
    Requirement already satisfied: async-generator in c:\programdata\anaconda3\lib\site-packages (from nbclient<0.6.0,>=0.5.0->nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (1.10)
    Requirement already satisfied: packaging in c:\programdata\anaconda3\lib\site-packages (from bleach->nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (20.4)
    Requirement already satisfied: webencodings in c:\programdata\anaconda3\lib\site-packages (from bleach->nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.5.1->pandas-profiling==2.9.0) (0.5.1)
    Building wheels for collected packages: pandas-profiling
      Building wheel for pandas-profiling (setup.py): started
      Building wheel for pandas-profiling (setup.py): finished with status 'done'
      Created wheel for pandas-profiling: filename=pandas_profiling-2.9.0-py2.py3-none-any.whl size=258957 sha256=0c602dfed34adc6d0084cf3ec1a5140d8eef8ae3cb8e624942ef8c72aa760e65
      Stored in directory: C:\Users\mkrom\AppData\Local\Temp\pip-ephem-wheel-cache-hl2l9st1\wheels\64\b6\85\dfc808b23666a5910371784e349d28818006ff63ed9cfeca59
    Successfully built pandas-profiling
    


```python
from pandas_profiling import ProfileReport
```


```python
import warnings
warnings.filterwarnings('ignore')
```


```python
profile = ProfileReport(dados, title='StrictoSensu ProfileReport', html={'style':{'full_width':True}})
```


```python
profile.to_notebook_iframe()
```
    <a href="https://raw.githubusercontent.com/MuriloKrominski/StrictoSensu-Brasil-2017a2020/master/StrictoSensu%20ProfileReport.html">StrictoSensu ProfileReport.html</a>

```python
profile.to_file(output_file="StrictoSensu ProfileReport")
```

<a href="https://murilokrominski.github.io/StrictoSensu-Brasil-2017a2020/">StrictoSensu ProfileReport.html</a>    
  

```python
pip install sweetviz
```

    Requirement already satisfied: sweetviz in c:\programdata\anaconda3\lib\site-packages (1.1.2)
    Requirement already satisfied: pandas!=1.0.0,!=1.0.1,!=1.0.2,>=0.25.3 in c:\programdata\anaconda3\lib\site-packages (from sweetviz) (1.1.4)
    Requirement already satisfied: jinja2>=2.11.1 in c:\programdata\anaconda3\lib\site-packages (from sweetviz) (2.11.2)
    Requirement already satisfied: scipy>=1.3.2 in c:\programdata\anaconda3\lib\site-packages (from sweetviz) (1.5.0)
    Requirement already satisfied: tqdm>=4.43.0 in c:\programdata\anaconda3\lib\site-packages (from sweetviz) (4.50.2)
    Requirement already satisfied: matplotlib>=3.1.3 in c:\programdata\anaconda3\lib\site-packages (from sweetviz) (3.3.2)
    Requirement already satisfied: importlib-resources>=1.2.0 in c:\programdata\anaconda3\lib\site-packages (from sweetviz) (3.3.0)
    Requirement already satisfied: numpy>=1.16.0 in c:\programdata\anaconda3\lib\site-packages (from sweetviz) (1.19.2)
    Requirement already satisfied: pytz>=2017.2 in c:\programdata\anaconda3\lib\site-packages (from pandas!=1.0.0,!=1.0.1,!=1.0.2,>=0.25.3->sweetviz) (2020.1)
    Requirement already satisfied: python-dateutil>=2.7.3 in c:\programdata\anaconda3\lib\site-packages (from pandas!=1.0.0,!=1.0.1,!=1.0.2,>=0.25.3->sweetviz) (2.8.1)
    Requirement already satisfied: MarkupSafe>=0.23 in c:\programdata\anaconda3\lib\site-packages (from jinja2>=2.11.1->sweetviz) (1.1.1)
    Requirement already satisfied: certifi>=2020.06.20 in c:\programdata\anaconda3\lib\site-packages (from matplotlib>=3.1.3->sweetviz) (2020.6.20)
    Requirement already satisfied: cycler>=0.10 in c:\programdata\anaconda3\lib\site-packages (from matplotlib>=3.1.3->sweetviz) (0.10.0)
    Requirement already satisfied: pillow>=6.2.0 in c:\programdata\anaconda3\lib\site-packages (from matplotlib>=3.1.3->sweetviz) (8.0.1)
    Requirement already satisfied: pyparsing!=2.0.4,!=2.1.2,!=2.1.6,>=2.0.3 in c:\programdata\anaconda3\lib\site-packages (from matplotlib>=3.1.3->sweetviz) (2.4.7)
    Requirement already satisfied: kiwisolver>=1.0.1 in c:\programdata\anaconda3\lib\site-packages (from matplotlib>=3.1.3->sweetviz) (1.2.0)
    Requirement already satisfied: six>=1.5 in c:\programdata\anaconda3\lib\site-packages (from python-dateutil>=2.7.3->pandas!=1.0.0,!=1.0.1,!=1.0.2,>=0.25.3->sweetviz) (1.15.0)
    Note: you may need to restart the kernel to use updated packages.
    


```python
import sweetviz as sv
```


```python
eda = sv.analyze(dados)
eda.show_html(filepath = 'StrictoSensu sweetviz.html')
```


 
```python
from IPython.display import IFrame
IFrame(src = 'StrictoSensu sweetviz.html',width=1000,height=600)
```

<a href="https://murilokrominski.github.io/StrictoSensu-Brasil-2017a2020/">StrictoSensu sweetviz.html</a>    
 
 ## RESULTADO: https://murilokrominski.github.io/StrictoSensu-Brasil-2017a2020/
