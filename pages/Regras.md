# Decomposição SQL

"As consultas da carga de trabalho instanciada na ontologia foram submetidas ao processo de decomposição (parsing), visto que as heurísticas de tuning
dependem da estrutura dessas consultas. Esse processo usado para dividir SQL
em nós indivisíveis foram compostos por 6 (seis) spin:rules. Foi utilizado o comando CONSTRUCT para inferir novas triplas, categorizadas por seus nós e
relacionamentos baseados nas classes e propriedades da OnDBTuning." (conforme item 3.2 da Dissertação de Mestrado)

As 6 (seis) *spin:rules*, podem ser encontradas no seguinte caminho na OnDBTuning, conforme destacado na figura abaixo em amarelo:

<img src="../image/caminhoRegra.PNG">


São elas:

**QueryStatment**

<img src="../image/querystatment.PNG">

**SelectClause, ReferencedColumn, FromClause, ReferencedTable**

<img src="../image/select.PNG">

**WhereClause,ReferencedColumn, CompositeExpression, AtomicExpression, Literal**

<img src="../image/whereclause.PNG">
<img src="../image/whereclause2.PNG">

**GroupBy**

<img src="../image/groupby.PNG">

**HavingClause**

<img src="../image/having.PNG">

**OrderByClause**

<img src="../image/order.PNG">