## Learning MongoDB

<h6>Referência/Fonte: https://mongodbwise.wordpress.com/2014/05/22/mongodb-guia-rapido/</h6>

<p style="text-align:justify;">MongoDB é um banco de dados multi-plataforma orientado ao documento que fornece alta performance, alta disponibilidade e fácil escalabilidade. MongoDB funciona no conceito de coleções de documentos.</p>
<h4 style="text-align:justify;"><span style="text-decoration:underline;">Banco de Dados</span></h4>
<p style="text-align:justify;">Banco de dados é um recipiente físico para coleções. Cada banco de dados tem o seu próprio conjunto de arquivos no sistema de arquivos. Um único servidor MongoDB normalmente tem vários bancos de dados.</p>
<h4 style="text-align:justify;"><span style="text-decoration:underline;">Coleções (Collection)</span></h4>
<p style="text-align:justify;">Collection é um grupo de documentos MongoDB. É o equivalente de uma tabela de RDBMS. Uma coleção existe dentro de um único banco de dados. Coleções não impõem um esquema. Documentos dentro de uma coleção pode ter diferentes campos. Normalmente, todos os documentos em uma coleção são propositalmente  semelhantes ou afins.</p>
<h4 style="text-align:justify;"><span style="text-decoration:underline;">Documento</span></h4>
<p style="text-align:justify;">Um documento é um conjunto de pares de valores-chave. Documentos têm esquema dinâmico. Esquema dinâmico significa que os documentos na mesma coleção não precisam ter o mesmo conjunto de campos ou estrutura e campos comuns em documentos de uma coleção podem conter diferentes tipos de dados.</p>
<p style="text-align:justify;">Exemplo:</p>
<p style="text-align:justify;">O exemplo abaixo mostra a estrutura do documento de um blog onde uma simples vírgula separa o par valor da chave.</p>
<pre class="prettyprint prettyprinted"><span class="pun" style="color:#666600;">{</span><span class="pln" style="color:#000000;">
   _id</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">7df78ad8902c</span><span class="pun" style="color:#666600;">)</span><span class="pln" style="color:#000000;">
   title</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'MongoDB - Guia Rapido'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;"> 
   description</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'MongoDB - Guia Rapido'</span><span class="pun" style="color:#666600;">,</span><span class="kwd" style="color:#000088;">by</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'MongoDBWise'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">
   url</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'http://www.mongodbwise.worpress.com'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">
   tags</span><span class="pun" style="color:#666600;">:</span><span class="pun" style="color:#666600;">[</span><span class="str" style="color:#008800;">'mongodb'</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">'database'</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">'NoSQL'</span><span class="pun" style="color:#666600;">],</span><span class="pln" style="color:#000000;">
   likes</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">100</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;"> 
   comments</span><span class="pun" style="color:#666600;">:</span><span class="pun" style="color:#666600;">[</span><span class="pun" style="color:#666600;">{</span><span class="pln" style="color:#000000;">
         user</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'user1'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">
         message</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'My first comment'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">
         dateCreated</span><span class="pun" style="color:#666600;">:</span><span class="kwd" style="color:#000088;">new</span><span class="typ" style="color:#7f0055;">Date</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">2014</span><span class="pun" style="color:#666600;">,</span><span class="pun"><span style="color:#006666;">5</span></span><span class="pun" style="color:#666600;">,</span><span class="lit" style="color:#006666;">21</span><span class="pun" style="color:#666600;">,</span><span class="lit" style="color:#006666;">2</span><span class="pun" style="color:#666600;">,</span><span class="lit" style="color:#006666;">15</span><span class="pun" style="color:#666600;">),</span><span class="pln" style="color:#000000;">
         like</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">0</span><span class="pun" style="color:#666600;">},</span><span class="pun" style="color:#666600;">{</span><span class="pln" style="color:#000000;">
         user</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'user2'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">
         message</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'My second comments'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">
         dateCreated</span><span class="pun" style="color:#666600;">:</span><span class="kwd" style="color:#000088;">new</span><span class="typ" style="color:#7f0055;">Date</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">2014</span><span class="pun" style="color:#666600;">,</span><span class="pun"><span style="color:#006666;">5</span></span><span class="pun" style="color:#666600;">,</span><span class="lit" style="color:#006666;">21</span><span class="pun" style="color:#666600;">,</span><span class="lit" style="color:#006666;">7</span><span class="pun" style="color:#666600;">,</span><span class="lit" style="color:#006666;">45</span><span class="pun" style="color:#666600;">),</span><span class="pln" style="color:#000000;">
         like</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">5</span><span class="pun" style="color:#666600;">}</span><span class="pun" style="color:#666600;">]</span><span class="pun" style="color:#666600;">}</span></pre>
<h4 style="text-align:justify;"></h4>
<p><span id="more-186"></span></p>
<h4 style="text-align:justify;"><span style="text-decoration:underline;">Instalar MongoDB no Windows</span></h4>
<p style="text-align:justify;">Para instalar o MongoDB no Windows, primeiro faça o download da última versão do MongoDB no site <a href="http://www.mongodb.org/downloads" rel="nofollow">http://www.mongodb.org/downloads</a></p>
<p style="text-align:justify;">Agora extraia o arquivo baixado para uma pasta de sua escolha. Certifique-se que o nome da pasta extraída é [versão] mongodb-win32-i386 ou x86_64 mongodb-win32-[versão]. Aqui [versão] é a versão do MongoDB baixada.</p>
<p style="text-align:justify;">Agora abra uma janela com Prompt de comando e execute o seguinte comando:</p>
<pre>C:\&gt;move mongodb-win64-* mongodb
 1 dir(s) moved.
C:\&gt;</pre>
<p style="text-align:justify;">No caso de ter extraído o mondodb em local diferente, em seguida, ir para esse caminho usando o comando cd FOLDER/DIR e executar o processo acima indicado.</p>
<p style="text-align:justify;">O MongoDB requer uma pasta de dados para armazenar seus arquivos. O local padrão para o diretório de dados MongoDB é c: \data\db. Então, você precisa criar essa pasta usando o Prompt de Comando. Execute a seguinte sequência de comandos:</p>
<pre>C:\&gt;md data
C:\md data\db</pre>
<p style="text-align:justify;">Se você tem instalar o MongoDB em local diferente então você precisa especificar qualquer caminho alternativo para \data\db, definindo o caminho <em><strong>dbpath</strong></em> no mongod.exe. Para a mesma questão execute os seguintes comandos</p>
<p style="text-align:justify;">No prompt de comando vá para o diretório <em><strong>bin</strong></em> localizado na pasta de instalação do MongoDB. Suponha que a pasta de instalação seja  <strong>D:\set up\mongodb</strong></p>
<pre>C:\Users\XYZ&gt;d:
D:\&gt;cd "set up"
D:\set up&gt;cd mongodb
D:\set up\mongodb&gt;cd bin
D:\set up\mongodb\bin&gt;mongod.exe --dbpath "d:\set up\mongodb\data"</pre>
<p style="text-align:justify;">Isto irá mostrar à espera de conexões mensagem na saída do console indicando que o processo mongod.exe está sendo executado com sucesso.</p>
<p style="text-align:justify;">Agora, para executar o mongodb você precisa abrir outro prompt de comando e executar o seguinte comando</p>
<pre>D:\set up\mongodb\bin&gt;mongo.exe
MongoDB shell version: 2.6.1
connecting to: test
&gt;db.test.save( { a: 1 } )
&gt;db.test.find()
{ "_id" : ObjectId(5879b0f65a56a454), "a" : 1 }
&gt;</pre>
<p>Isso vai mostrar que o MongoDB foi instalado e executado com sucesso. Da próxima vez quando você executa mongodb você precisa emitir apenas comandos:</p>
<pre>D:\set up\mongodb\bin&gt;mongod.exe --dbpath "d:\set up\mongodb\data" 
D:\set up\mongodb\bin&gt;mongo.exe</pre>
<h4><span style="text-decoration:underline;">Create Database<br />
</span></h4>
<p>Para criar um banco de dados basta utilizar o comando &#8220;use database_name&#8221;, o comando irá criar um novo banco de dados se caso ele não existir, de outra forma ele irá retornar o banco de dados existente.</p>
<p><strong>Sintaxe: </strong></p>
<p>A sintaxe básica para a utilização do USE_DATABASE é a seguinte:</p>
<p><strong>use DATABASE_NAME</strong></p>
<p><strong>Exemplo</strong></p>
<p>Se você quer criar um banco de dados com o nome &lt;mydb&gt;, então a sintaxe seria a seguinte:</p>
<pre>&gt;use mydb
switched to db mydb</pre>
<p>Para verificar o banco de dados selecionado atualmente usar o comando <strong>db</strong></p>
<pre>&gt;db
mydb</pre>
<p>Se você quiser verificar a sua lista de bancos de dados, em seguida, use o comando <strong>show dbs</strong>.</p>
<pre>&gt;show dbs
local 0.78125GB
test 0.23012GB</pre>
<p>Você deve ter notado que seu banco de dados criado (mydb) não está presente na lista. Para exibir dados é necessário inserir pelo menos um documento para ele.</p>
<pre class="prettyprint prettyprinted"><span class="pun" style="color:#666600;">&gt;</span><span class="pln" style="color:#000000;">db</span><span class="pun" style="color:#666600;">.</span><span class="pun"><span style="color:#000000;">mydb</span></span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">insert</span><span class="pun" style="color:#666600;">({</span><span class="str" style="color:#008800;">"name"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"mongodbwise"</span><span class="pun" style="color:#666600;">})
</span><span class="pun" style="color:#666600;">&gt;</span><span class="pln" style="color:#000000;">show dbs
</span><span class="kwd" style="color:#000088;">local</span><span class="lit" style="color:#006666;">0.78125GB</span><span class="pln" style="color:#000000;">
mydb       </span><span class="lit" style="color:#006666;">0.23012GB</span><span class="pln" style="color:#000000;">
test       </span><span class="lit" style="color:#006666;">0.23012GB</span></pre>
<p><em><strong>Nota : No banco de dados &#8220;test&#8221; é o padrão do MongoDB, portanto se você não criar qualquer banco de dados, as coleções serão armazenadas no banco de dados de teste.</strong></em></p>
<h4><span style="text-decoration:underline;">Drop Database</span></h4>
<p>Para dropar um banco de dados no MongoDB utilizamos o comando <strong>db.dropDatabase()</strong>.</p>
<p>A sintaxe básica do comando <strong>dropDatabase ()</strong>  é a seguinte:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pln" style="color:#000000;">db</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">dropDatabase</span><span class="pun" style="color:#666600;">()</span></pre>
<p>Isso excluirá o banco de dados selecionado. Se você não tiver selecionado qualquer banco de dados, então ele vai apagar dados do banco de dados default &#8216;test&#8217;</p>
<p><strong>Exemplo</strong></p>
<p>Se você deseja excluir o novo banco de dados <strong>&lt;mydb&gt;</strong>, então o comando <strong>dropDatabase()</strong> seria o seguinte:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="kwd" style="color:#000088;">use</span><span class="pln" style="color:#000000;"> mydb
switched to db mydb
</span><span class="pun" style="color:#666600;">&gt;</span><span class="pln" style="color:#000000;">db</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">dropDatabase</span><span class="pun" style="color:#666600;">()</span><span class="pun" style="color:#666600;">&gt;{</span><span class="str" style="color:#008800;">"dropped"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"mydb"</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">"ok"</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">}</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<h4><span style="text-decoration:underline;">Create Collection</span></h4>
<p>Para esta tarefa, utilizaremos o comando db.createCollection(name, options), onde &#8220;name&#8221; é o nome da Collection e &#8220;options&#8221; é utilizada para especificar as configurações da Colletion.</p>
<table class="src" style="color:#000000;">
<tbody>
<tr>
<th>Parameter</th>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td>Name</td>
<td>String</td>
<td>Nome da coleção a ser criada</td>
</tr>
<tr>
<td>Options</td>
<td>Document</td>
<td>(Opcional) Especifica opções sobre tamanho de memoria e indices</td>
</tr>
</tbody>
</table>
<p>Opções parâmetro é opcional, por isso você precisa especificar apenas o nome da coleção.</p>
<p><strong>Sintaxe</strong></p>
<p>A sintaxe básica do método <strong>createCollection ()</strong> é como se segue:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="kwd" style="color:#000088;">use</span><span class="pln" style="color:#000000;"> test
switched to db test
</span><span class="pun" style="color:#666600;">&gt;</span><span class="pln" style="color:#000000;">db</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">createCollection</span><span class="pun" style="color:#666600;">(</span><span class="str" style="color:#008800;">"mycollection"</span><span class="pun" style="color:#666600;">)</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"ok"</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">}</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<p>Você pode verificar a coleção criada usando o comando show collections</p>
<p class="prettyprint prettyprinted" style="color:#000000;">
<pre class="prettyprint prettyprinted"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">show collections
mycollection
system</span><span class="pun" style="color:#666600;">.</span><span class="pln">indexes</span></pre>
<p class="prettyprint prettyprinted" style="color:#000000;"><span class="pln" style="color:#000000;"><br />
Também podemos utilizar o comando show tables que irá retornar o mesmo resultado</p>
<p></span></p>
<pre class="prettyprint prettyprinted"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">show tables
mycollection
system</span><span class="pun" style="color:#666600;">.</span><span class="pln">indexes</span></pre>
<p class="prettyprint prettyprinted" style="color:#000000;"><span class="pln" style="color:#000000;"> </span></p>
<h4 style="color:#000000;">Lista de Opções</h4>
<table class="src" style="color:#000000;">
<tbody>
<tr>
<th>Field</th>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td>capped</td>
<td>Boolean</td>
<td>(Opcional) Se &#8220;true&#8221;, habilita uma &#8220;capped collection&#8221;. Capped collection é uma coleção com tamanho fixo que sobrescreve automaticamente as atualizações antigas sempre que atinge o tamanho máximo. <strong>Se você especificar &#8220;true&#8221;</strong><b>, será necessário especificar também o parametro &#8220;size&#8221;.</b></td>
</tr>
<tr>
<td>autoIndexID</td>
<td>Boolean</td>
<td>(Opcional) Se true, o indice é criado automaticamente no campo _id. O Valor Default é &#8220;false&#8221;.</td>
</tr>
<tr>
<td>size</td>
<td>number</td>
<td>(Opcional) Especifica o tamanho máximo em bytes para uma capped collection. Se <b>capped is true, então será necessário especificar este campo também.</b></td>
</tr>
<tr>
<td>max</td>
<td>number</td>
<td>(Opcional) Especifica o numero máximo de documentos permitidos em uma the capped collection.</td>
</tr>
</tbody>
</table>
<p>Ao inserir o documento, o MongoDB primeiro verifica o tamanho do campo na Capped Collection, em seguida, ele verifica o campo max.</p>
<p><strong>Sintaxe</strong></p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">createCollection</span><span class="pun" style="color:#666600;">(</span><span class="str" style="color:#008800;">"mycol"</span><span class="pun" style="color:#666600;">,</span><span class="pun" style="color:#666600;">{</span><span class="pln"> capped </span><span class="pun" style="color:#666600;">:</span><span class="kwd" style="color:#000088;">true</span><span class="pun" style="color:#666600;">,</span><span class="pln"> autoIndexID </span><span class="pun" style="color:#666600;">:</span><span class="kwd" style="color:#000088;">true</span><span class="pun" style="color:#666600;">,</span><span class="pln"> size </span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">6142800</span><span class="pun" style="color:#666600;">,</span><span class="pln"> max </span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">10000</span><span class="pun" style="color:#666600;">}</span><span class="pun" style="color:#666600;">)</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"ok"</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">}</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<p>No mongoDB você não precisa criar a coleção, pois o MongoDB cria a coleção automaticamente quando você insere algum documento.</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln" style="color:#000000;">db</span><span class="pun" style="color:#666600;">.mongodbwise</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">insert</span><span class="pun" style="color:#666600;">({</span><span class="str" style="color:#008800;">"name"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"mongodbwise"</span><span class="pun" style="color:#666600;">})
</span><span class="pun" style="color:#666600;">&gt;</span><span class="pln" style="color:#000000;">show collections
mycol
mycollection
system</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">indexes
mongodbwise
</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<h4><span style="text-decoration:underline;">Drop Collection</span></h4>
<p>No MongoDB utilizamos o comando <strong>db.collection.drop()</strong>  para descartar (dropar) uma coleção (Collection)</p>
<p><strong>Sintaxe</strong></p>
<p>A sintaxe básica do comando <strong>drop()</strong> é a seguinte:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pln" style="color:#000000;">db</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">COLLECTION_NAME</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">drop</span><span class="pun" style="color:#666600;">()</span></pre>
<p><strong>Exemplo</strong></p>
<p>Abaixo veremos um exemplo onde vamos dropar a coleção com o nome  <strong>myCollection</strong></p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="kwd" style="color:#000088;">use</span><span class="pln"> mydb
switched to db mydb
</span><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">mycollection</span><span class="pun" style="color:#666600;">.</span><span class="pln">drop</span><span class="pun" style="color:#666600;">()</span><span class="kwd" style="color:#000088;">true</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<h4><span style="text-decoration:underline;">Inserir Documentos (Insert Document)</span></h4>
<p>Para inserir dados em uma coleção MongoDB, você precisa usar o comando <strong>insert()</strong> do MongoDB.</p>
<p><strong>Sintaxe</strong></p>
<p>A sintaxe básica do comando<strong> insert()</strong> é a seguinte:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">COLLECTION_NAME</span><span class="pun" style="color:#666600;">.</span><span class="pln">insert</span><span class="pun" style="color:#666600;">(</span><span class="pln">document</span><span class="pun" style="color:#666600;">)</span></pre>
<p><strong>Exemplo</strong></p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln">insert</span><span class="pun" style="color:#666600;">({</span><span class="pln">
   _id</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">7df78ad8902c</span><span class="pun" style="color:#666600;">),</span><span class="pln">
   title</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'MongoDB Guia Rapido'</span><span class="pun" style="color:#666600;">,</span><span class="pln"> 
   description</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'MongoDB - Guia Rapido'</span><span class="pun" style="color:#666600;">,</span><span class="kwd" style="color:#000088;">by</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'MongodbWise'</span><span class="pun" style="color:#666600;">,</span><span class="pln">
   url</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'http://www.mongodbwise.wordpress.com'</span><span class="pun" style="color:#666600;">,</span><span class="pln">
   tags</span><span class="pun" style="color:#666600;">:</span><span class="pun" style="color:#666600;">[</span><span class="str" style="color:#008800;">'mongodb'</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">'database'</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">'NoSQL'</span><span class="pun" style="color:#666600;">],</span><span class="pln">
   likes</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">100</span><span class="pun" style="color:#666600;">})</span></pre>
<p>Aqui é a nossa coleção mycol. Se a coleção não existir no banco de dados, então o MongoDB irá criar esta coleção e  em seguida, inserir documento para ele.</p>
<p>No documento inserido, se não especificar o parâmetro <strong>_id</strong>, então MongoDB atribui um ObjectId exclusivo para esse documento.</p>
<p>O <strong>_id</strong> é de 12 bytes é um número hexadecimal exclusivo para cada documento em uma coleção. 12 bytes serão divididos da seguinte forma:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pln">_id</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">4</span><span class="pln"> bytes timestamp</span><span class="pun" style="color:#666600;">,</span><span class="lit" style="color:#006666;">3</span><span class="pln"> bytes machine id</span><span class="pun" style="color:#666600;">,</span><span class="lit" style="color:#006666;">2</span><span class="pln"> bytes process id</span><span class="pun" style="color:#666600;">,</span><span class="lit" style="color:#006666;">3</span><span class="pln"> bytes incrementer</span><span class="pun" style="color:#666600;">)</span></pre>
<p>Para inserir vários documentos em única query, você pode passar uma matriz de documentos no comando <strong>insert()</strong>.</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">post</span><span class="pun" style="color:#666600;">.</span><span class="pln">insert</span><span class="pun" style="color:#666600;">([</span><span class="pun" style="color:#666600;">{</span><span class="pln">
   title</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'MongoDB - Guia Rapido'</span><span class="pun" style="color:#666600;">,</span><span class="pln"> 
   description</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'MongoDB - Guia Rapido'</span><span class="pun" style="color:#666600;">,</span><span class="kwd" style="color:#000088;">by</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'MongoDBWise'</span><span class="pun" style="color:#666600;">,</span><span class="pln">
   url</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'http://www.mongodbwise.wordpress.com'</span><span class="pun" style="color:#666600;">,</span><span class="pln">
   tags</span><span class="pun" style="color:#666600;">:</span><span class="pun" style="color:#666600;">[</span><span class="str" style="color:#008800;">'mongodb'</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">'database'</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">'NoSQL'</span><span class="pun" style="color:#666600;">],</span><span class="pln">
   likes</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">100</span><span class="pun" style="color:#666600;">},</span><span class="pun" style="color:#666600;">{</span><span class="pln">
   title</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'NoSQL Database'</span><span class="pun" style="color:#666600;">,</span><span class="pln"> 
   description</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'NoSQL database doesn'</span><span class="pln">t have tables</span><span class="str" style="color:#008800;">',
   by: '</span><span class="pln">tutorials point</span><span class="str" style="color:#008800;">',
   url: '</span><span class="pln">http</span><span class="pun" style="color:#666600;">:</span><span class="com" style="color:#880000;">//www.mongodbwise.wordpress.com',</span><span class="pln">
   tags</span><span class="pun" style="color:#666600;">:</span><span class="pun" style="color:#666600;">[</span><span class="str" style="color:#008800;">'mongodb'</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">'database'</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">'NoSQL'</span><span class="pun" style="color:#666600;">],</span><span class="pln">
   likes</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">20</span><span class="pun" style="color:#666600;">,</span><span class="pln"> 
   comments</span><span class="pun" style="color:#666600;">:</span><span class="pun" style="color:#666600;">[</span><span class="pun" style="color:#666600;">{</span><span class="pln">
         user</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'user1'</span><span class="pun" style="color:#666600;">,</span><span class="pln">
         message</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'My first comment'</span><span class="pun" style="color:#666600;">,</span><span class="pln">
         dateCreated</span><span class="pun" style="color:#666600;">:</span><span class="kwd" style="color:#000088;">new</span><span class="typ" style="color:#7f0055;">Date</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">2013</span><span class="pun" style="color:#666600;">,</span><span class="lit" style="color:#006666;">11</span><span class="pun" style="color:#666600;">,</span><span class="lit" style="color:#006666;">10</span><span class="pun" style="color:#666600;">,</span><span class="lit" style="color:#006666;">2</span><span class="pun" style="color:#666600;">,</span><span class="lit" style="color:#006666;">35</span><span class="pun" style="color:#666600;">),</span><span class="pln">
         like</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">0</span><span class="pun" style="color:#666600;">}</span><span class="pun" style="color:#666600;">]</span><span class="pun" style="color:#666600;">}</span><span class="pun" style="color:#666600;">])</span></pre>
<h4><span style="text-decoration:underline;">Consulta de Documentos</span></h4>
<p>Para consultar os dados de Collection MongoDB, você precisa usar o comando <strong>find()</strong> do MongoDB.</p>
<p><strong>Sintaxe</strong></p>
<p>A sintaxe básica do comando <strong>find()</strong> é como se segue:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">COLLECTION_NAME</span><span class="pun" style="color:#666600;">.</span><span class="pln">find</span><span class="pun" style="color:#666600;">()</span></pre>
<p>O comando<strong> find ()</strong> irá exibir todos os documentos de uma forma não estruturada. Para exibir os resultados de uma forma estruturada, você pode usar o comando <strong>pretty()</strong>.</p>
<p>Sintaxe</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln">find</span><span class="pun" style="color:#666600;">().</span><span class="pln">pretty</span><span class="pun" style="color:#666600;">()</span></pre>
<p>Exemplo</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln">find</span><span class="pun" style="color:#666600;">().</span><span class="pln">pretty</span><span class="pun" style="color:#666600;">()
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"_id"</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">7df78ad8902c</span><span class="pun" style="color:#666600;">),
</span><span class="str" style="color:#008800;"> "title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDB - Guia Rapido"</span><span class="pun" style="color:#666600;">,
</span><span class="str" style="color:#008800;"> "description"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDB - Guia Rapido"</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">"by"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDBWise"</span><span class="pun" style="color:#666600;">,
</span><span class="str" style="color:#008800;"> "url"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"http://www.mongodbwise.wordpress.com"</span><span class="pun" style="color:#666600;">,
</span><span class="str" style="color:#008800;"> "tags"</span><span class="pun" style="color:#666600;">:</span><span class="pun" style="color:#666600;">[</span><span class="str" style="color:#008800;">"mongodb"</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">"database"</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">"NoSQL"</span><span class="pun" style="color:#666600;">],
</span><span class="str" style="color:#008800;"> "likes"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"100"</span><span class="pun" style="color:#666600;">}</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<p>Além do comando find(), existe também o comando findOne() que irá retornar tudo em um único documento</p>
<h4><strong> </strong><span style="text-decoration:underline;">Cláusula Where equivalentes entre RDBMS e MongoDB</span></h4>
<p>Para consultar o documento com base em alguma condição, você pode usar seguintes operações</p>
<p style="color:#000000;">
<table class="src" style="color:#000000;">
<tbody>
<tr>
<th>Operação</th>
<th>Syntaxe</th>
<th>Examplo</th>
<th>RDBMS Equivalente</th>
</tr>
<tr>
<td>Equality</td>
<td>{&lt;key&gt;:&lt;value&gt;}</td>
<td>db.mycol.find({&#8220;by&#8221;:&#8221;tutorials point&#8221;}).pretty()</td>
<td>where by = &#8216;tutorials point&#8217;</td>
</tr>
<tr>
<td>Less Than</td>
<td>{&lt;key&gt;:{$lt:&lt;value&gt;}}</td>
<td>db.mycol.find({&#8220;likes&#8221;:{$lt:50}}).pretty()</td>
<td>where likes &lt; 50</td>
</tr>
<tr>
<td>Less Than Equals</td>
<td>{&lt;key&gt;:{$lte:&lt;value&gt;}}</td>
<td>db.mycol.find({&#8220;likes&#8221;:{$lte:50}}).pretty()</td>
<td>where likes &lt;= 50</td>
</tr>
<tr>
<td>Greater Than</td>
<td>{&lt;key&gt;:{$gt:&lt;value&gt;}}</td>
<td>db.mycol.find({&#8220;likes&#8221;:{$gt:50}}).pretty()</td>
<td>where likes &gt; 50</td>
</tr>
<tr>
<td>Greater Than Equals</td>
<td>{&lt;key&gt;:{$gte:&lt;value&gt;}}</td>
<td>db.mycol.find({&#8220;likes&#8221;:{$gte:50}}).pretty()</td>
<td>where likes &gt;= 50</td>
</tr>
<tr>
<td>Not Equals</td>
<td>{&lt;key&gt;:{$ne:&lt;value&gt;}}</td>
<td>db.mycol.find({&#8220;likes&#8221;:{$ne:50}}).pretty()</td>
<td>where likes != 50</td>
</tr>
</tbody>
</table>
<h2 style="color:#000000;"></h2>
<p><span style="text-decoration:underline;"><strong>&#8220;AND&#8221; no MongoDB</strong></span></p>
<p>No comando find () se você passar várias chaves, separando-os por &#8216;,&#8217; então MongoDB irá tratar como condição AND. A sintaxe básica é mostrada abaixo:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln" style="color:#000000;">db</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">find</span><span class="pun" style="color:#666600;">({</span><span class="pln" style="color:#000000;">key1</span><span class="pun" style="color:#666600;">:</span><span class="pln" style="color:#000000;">value1</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;"> key2</span><span class="pun" style="color:#666600;">:</span><span class="pln" style="color:#000000;">value2</span><span class="pun" style="color:#666600;">}).</span><span class="pln" style="color:#000000;">pretty</span><span class="pun" style="color:#666600;">()</span></pre>
<p><strong>Exemplo</strong></p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln">find</span><span class="pun" style="color:#666600;">()</span><span class="pun" style="color:#666600;">
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"_id"</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">7df78ad8902c</span><span class="pun" style="color:#666600;">),
</span><span class="str" style="color:#008800;"> "title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDB - Guia Rapido"</span><span class="pun" style="color:#666600;">,
</span><span class="str" style="color:#008800;"> "description"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDB - Guia Rapido"</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">"by"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDBWise"</span><span class="pun" style="color:#666600;">,
</span><span class="str" style="color:#008800;"> "url"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"http://www.mongodbwise.wordpress.com"</span><span class="pun" style="color:#666600;">,
</span><span class="str" style="color:#008800;"> "tags"</span><span class="pun" style="color:#666600;">:</span><span class="pun" style="color:#666600;">[</span><span class="str" style="color:#008800;">"mongodb"</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">"database"</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">"NoSQL"</span><span class="pun" style="color:#666600;">],
</span><span class="str" style="color:#008800;"> "likes"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"100"</span><span class="pun" style="color:#666600;">}</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<p>No exemplo acima, onde  a clausula &#8216; where by=&#8217;MongoDBWise&#8217; AND title=&#8217;MongoDB &#8211; Guia Rapido&#8217; &#8216;.Você pode passar qualquer número de pares de chaves de valor na cláusula find.</p>
<h4><span style="text-decoration:underline;">&#8220;OR&#8221; no MongoDB</span></h4>
<p><strong>Sintaxe</strong></p>
<p>Para consultar os documentos com base na condição OR, você precisa usar $or como palavra-chave. A sintaxe básica de OR é mostrado abaixo:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln" style="color:#000000;">db</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">find</span><span class="pun" style="color:#666600;">(</span><span class="pun" style="color:#666600;">{</span><span class="pln" style="color:#000000;">
      $or</span><span class="pun" style="color:#666600;">:</span><span class="pun" style="color:#666600;">[</span><span class="pun" style="color:#666600;">{</span><span class="pln" style="color:#000000;">key1</span><span class="pun" style="color:#666600;">:</span><span class="pln" style="color:#000000;"> value1</span><span class="pun" style="color:#666600;">},</span><span class="pun" style="color:#666600;">{</span><span class="pln" style="color:#000000;">key2</span><span class="pun" style="color:#666600;">:</span><span class="pln" style="color:#000000;">value2</span><span class="pun" style="color:#666600;">}
</span><span class="pun" style="color:#666600;">]</span><span class="pun" style="color:#666600;">}
</span><span class="pun" style="color:#666600;">).</span><span class="pln" style="color:#000000;">pretty</span><span class="pun" style="color:#666600;">()</span></pre>
<p>Abaixo dado exemplo mostrará todos os documentos escritos por &#8216;mongoDBWise&#8221;ou cujo título é&#8217; MongoDB &#8211; Guia Rapido &#8216;</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln">find</span><span class="pun" style="color:#666600;">({</span><span class="pln">$or</span><span class="pun" style="color:#666600;">:[{</span><span class="str" style="color:#008800;">"by"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"tutorials point"</span><span class="pun" style="color:#666600;">},{</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDB Overview"</span><span class="pun" style="color:#666600;">}]}).</span><span class="pln">pretty</span><span class="pun" style="color:#666600;">()
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"_id"</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">7df78ad8902c</span><span class="pun" style="color:#666600;">),
</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDB - Guia Rapido"</span><span class="pun" style="color:#666600;">,
</span><span class="str" style="color:#008800;">"description"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDB - Guia Rapido"</span><span class="pun" style="color:#666600;">,
</span><span class="str" style="color:#008800;">"by"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDBWise"</span><span class="pun" style="color:#666600;">,
</span><span class="str" style="color:#008800;">"url"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"http://www.mongodbwise.wordpress.com"</span><span class="pun" style="color:#666600;">,
</span><span class="str" style="color:#008800;">"tags"</span><span class="pun" style="color:#666600;">:</span><span class="pun" style="color:#666600;">[</span><span class="str" style="color:#008800;">"mongodb"</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">"database"</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">"NoSQL"</span><span class="pun" style="color:#666600;">],
</span><span class="str" style="color:#008800;">"likes"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"100"</span><span class="pun" style="color:#666600;">}</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<h4><span style="text-decoration:underline;">Utilizando &#8220;AND&#8221; e &#8220;OR&#8221; juntos</span></h4>
<p>O exemplo a seguir mostra documentos que possuem &#8220;likes&#8221; acima de 100 e cujo o titulo é &#8220;MongoDB &#8211; Guia Rapido&#8221; escrito por &#8220;MongoDBWise&#8221;. Seria o equivalente a clausula &#8220;where likes&gt;10 AND (by = &#8220;MongoDBWise&#8221; OR title=&#8221;MongoDB &#8211; Guia Rapido&#8221;.</p>
<pre>&gt;db.mycol.find("likes": {$gt:10}, $or: [{"by": "MongoDBWise"}, {"title": "MongoDB - Guia Rapido"}] }).pretty()
{
 "_id": ObjectId(7df78ad8902c),
 "title": "MongoDB - Guia Rapido", 
 "description": "MongoDB - Guia Rapido",
 "by": "MongoDBWise",
 "url": "http://www.mongodbwise.wordpress.com",
 "tags": ["mongodb", "database", "NoSQL"],
 "likes": "100"
}
&gt;</pre>
<p><span style="text-decoration:underline;"><strong>Atualização de Documentos (Update Document)</strong></span></p>
<p style="text-align:justify;">As atualizações de documentos em uma coleção no MongoDB são feitas através dos comandos update() e save(). O comando update() atualiza os valores enquanto o comando save() substitui os documentos existentes com os novos documentos passados através do comando save().</p>
<h4><span style="text-decoration:underline;">MongoDB Update()</span></h4>
<p><strong>Sinataxe</strong></p>
<p>A sintaxe básica do comando update() é como segue abaixo:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">COLLECTION_NAME</span><span class="pun" style="color:#666600;">.</span><span class="pln">update</span><span class="pun" style="color:#666600;">(</span><span class="pln">SELECTIOIN_CRITERIA</span><span class="pun" style="color:#666600;">,</span><span class="pln"> UPDATED_DATA</span><span class="pun" style="color:#666600;">)</span></pre>
<p>Vamos considerar que a Collection Mycol possui os seguintes dados:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"_id"</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">5983548781331adf45ec5</span><span class="pun" style="color:#666600;">),</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDB - Guia Rapido"</span><span class="pun" style="color:#666600;">}
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"_id"</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">5983548781331adf45ec6</span><span class="pun" style="color:#666600;">),</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"NoSQL Overview"</span><span class="pun" style="color:#666600;">}
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"_id"</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">5983548781331adf45ec7</span><span class="pun" style="color:#666600;">),</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDB - Overview"</span><span class="pun" style="color:#666600;">}

</span></pre>
<p>Seguindo o exemplo, vamos definir o novo título &#8216;New MongoDB &#8211; Guia Rapido&#8217; dos documentos cujo título é &#8220;MongoDB &#8211; Overview &#8216;</p>
<pre>&gt;db.mycol.update({'title':'MongoDB Overview'},{$set:{'title':'New MongoDB - Guia Rapido'}})
&gt;db.mycol.find()
{ "_id" : ObjectId(5983548781331adf45ec5), "title":"MongoDB - Guia Rapido"}
{ "_id" : ObjectId(5983548781331adf45ec6), "title":"NoSQL Overview"}
{ "_id" : ObjectId(5983548781331adf45ec7), "title":"New MongoDB - Guia Rapido"}
&gt;</pre>
<p>Por default o mongodb irá atualizar somente um único documento, para atualizações múltiplas, é necessário definir o parâmetro, &#8220;multi&#8221; para true.</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pln" style="color:#000000;">db</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">update</span><span class="pun" style="color:#666600;">({</span><span class="str" style="color:#008800;">'title'</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'MongoDB Overview'</span><span class="pun" style="color:#666600;">},{</span><span class="pln" style="color:#000000;">$set</span><span class="pun" style="color:#666600;">:{</span><span class="str" style="color:#008800;">'title'</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'New MongoDB - Guia Rapido'</span><span class="pun" style="color:#666600;">}},{</span><span class="pln" style="color:#000000;">multi</span><span class="pun" style="color:#666600;">:</span><span class="kwd" style="color:#000088;">true</span><span class="pun" style="color:#666600;">})</span></pre>
<h4><span style="text-decoration:underline;">MongoDB Save() Method</span></h4>
<p>O método save() substitui o documento existente com o novo documento passado pelo comando save()</p>
<p>A Sintaxe básica para o comando save() é como passada a seguir:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">COLLECTION_NAME</span><span class="pun" style="color:#666600;">.</span><span class="pln">save</span><span class="pun" style="color:#666600;">({</span><span class="pln">_id</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(),</span><span class="pln">NEW_DATA</span><span class="pun" style="color:#666600;">})</span></pre>
<p>Seguindo o exemplo vamos substituir o documento com a_id &#8216;5983548781331adf45ec7&#8217;</p>
<pre>&gt;db.mycol.save(
 {
 "_id" : ObjectId(5983548781331adf45ec7), "title":"New MongoDB - Guia Rapido", "by":"MongoDBWise"</pre>
<pre> }
)
&gt;db.mycol.find()
{ "_id" : ObjectId(5983548781331adf45ec5), "title":"MongoDB - Guia Rapido", "by":"MongoDBWise"}
{ "_id" : ObjectId(5983548781331adf45ec6), "title":"NoSQL Overview"}
{ "_id" : ObjectId(5983548781331adf45ec7), "title":"New MongoDB - Guia Rapido"}
&gt;</pre>
<h4><span style="text-decoration:underline;">Excluir Documentos (Delete Document)</span></h4>
<p style="text-align:justify;">O método remove() de MongoDB  é usado para remover documentos da coleção. O método remove() aceita dois parâmetros. Um deles é critério de exclusão e segundo é o Flag Justone</p>
<ol>
<li>Critérios de exclusão: (Opcional) Critérios de exclusão de acordo com documentos serão removidos.</li>
<li>Justone: (opcional) Se definido como &#8220;true&#8221; ou 1, em seguida, retira apenas um documento.</li>
</ol>
<p>Abaixo segue a sitaxe básica para o comando remove():</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">COLLECTION_NAME</span><span class="pun" style="color:#666600;">.</span><span class="pln">remove</span><span class="pun" style="color:#666600;">(</span><span class="pln">DELLETION_CRITTERIA</span><span class="pun" style="color:#666600;">)</span></pre>
<p>Considerando que a coleção &#8220;mycol&#8221;  tem os seguintes dados:</p>
<pre>{ "_id" : ObjectId(5983548781331adf45ec5), "title":"MongoDB - Guia Rapido"}
{ "_id" : ObjectId(5983548781331adf45ec6), "title":"NoSQL Overview"}
{ "_id" : ObjectId(5983548781331adf45ec7), "title":"New MongoDB - Guia Rapido"}


</pre>
<p>Seguindo o exemplo vamos remover todos os documentos cujo título é &#8216;MongoDB &#8211; Guia Rapido&#8221;</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln">remove</span><span class="pun" style="color:#666600;">({</span><span class="str" style="color:#008800;">'title'</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'MongoDB - Guia Rapido'</span><span class="pun" style="color:#666600;">})
</span><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln">find</span><span class="pun" style="color:#666600;">()
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"_id"</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">5983548781331adf45ec6</span><span class="pun" style="color:#666600;">),</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"NoSQL Overview"</span><span class="pun" style="color:#666600;">}
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"_id"</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">5983548781331adf45ec7</span><span class="pun" style="color:#666600;">),</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"New MongoDB - Guia Rapido"</span><span class="pun" style="color:#666600;">}</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<p><span style="text-decoration:underline;"><strong>Removendo apenas um documento</strong></span></p>
<p>Se houver vários registros e você quer apagar apenas o primeiro registro, em seguida, defina o parâmetro Justone no comando remove()</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">COLLECTION_NAME</span><span class="pun" style="color:#666600;">.</span><span class="pln">remove</span><span class="pun" style="color:#666600;">(</span><span class="pln">DELETION_CRITERIA</span><span class="pun" style="color:#666600;">,</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">)</span></pre>
<p>Se você não especificar os critérios de exclusão, então o mongodb vai excluir todos documentos  da coleção. Isto seria o equivalente do comando de SQL truncate.</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln">remove</span><span class="pun" style="color:#666600;">()
</span><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln">find</span><span class="pun" style="color:#666600;">()
</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<h4><span style="text-decoration:underline;">MongoDB Projection</span></h4>
<p style="text-align:justify;">O significado de uma projeção mongodb é que você está selecionando apenas os dados necessários ao invés de selecionar todo os dados de um documento. Se um documento tem 5 campos e você precisa mostrar apenas 3, e em seguida selecionar apenas 3 campos a partir deles.</p>
<p style="text-align:justify;">O comando <strong>find()</strong> do MongoDB, como explicado anteriormente, aceita um segundo parâmetro opcional que é a lista de campos que você deseja recuperar. Em MongoDB quando você executar o método <strong>find()</strong>,  ele exibe todos os campos de um documento. Para limitar isso, você precisa configurar como vai querer a lista de campos, definindo com valor 1 ou 0. 1 é usado para mostrar a arquivado enquanto 0 é usado para ocultar o campo.</p>
<p style="text-align:justify;">A sintaxe básica do método <strong>find()</strong> com projeção é a seguinte:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">COLLECTION_NAME</span><span class="pun" style="color:#666600;">.</span><span class="pln">find</span><span class="pun" style="color:#666600;">({},{</span><span class="pln">KEY</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">})</span></pre>
<p>Considerando que a coleção<strong> &#8220;mycol&#8221;</strong>  tem os seguintes dados:</p>
<pre>{ "_id" : ObjectId(5983548781331adf45ec5), "title":"MongoDB - Guia Rapido"}
{ "_id" : ObjectId(5983548781331adf45ec6), "title":"NoSQL Overview"}
{ "_id" : ObjectId(5983548781331adf45ec7), "title":"New MongoDB - Guia Rapido"}

</pre>
<p>Seguindo o exemplo, irá exibir o título do documento ao consultar o documento.</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln" style="color:#000000;">db</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">find</span><span class="pun" style="color:#666600;">({},{</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">_id</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">0</span><span class="pun" style="color:#666600;">})
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDB - Guia Rapido"</span><span class="pun" style="color:#666600;">}
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"NoSQL Overview"</span><span class="pun" style="color:#666600;">}
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"New MongoDB - Guia Rapido"</span><span class="pun" style="color:#666600;">}</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<p>Por favor, note campo _id sempre é exibido ao executar o comando <strong>find()</strong>, se você não quer que este campo seja listado, então você precisará configurá-lo como 0.</p>
<h4><span style="text-decoration:underline;">Limite de Documentos</span></h4>
<p><span style="text-decoration:underline;"><strong>MongoDB Limit() Method</strong></span></p>
<p>Para limitar os registros no MongoDB, você precisa usar o método <strong>limit()</strong>. O método <strong>limit()</strong> aceita um argumento de tipo de número, que é o número de documentos a serem exibidos.</p>
<p><span style="color:#000000;">A sintaxe básica do método </span><b style="color:#000000;">limit()</b><span style="color:#000000;"> é como segue:</span></p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln" style="color:#000000;">db</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">COLLECTION_NAME</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">find</span><span class="pun" style="color:#666600;">().</span><span class="pln" style="color:#000000;">limit</span><span class="pun" style="color:#666600;">(</span><span class="pln" style="color:#000000;">NUMBER</span><span class="pun" style="color:#666600;">)</span></pre>
<p>Considerando que a coleção<strong> mycol</strong> possui os seguintes dados</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"_id"</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">5983548781331adf45ec5</span><span class="pun" style="color:#666600;">),</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDB - Guia Rapido"</span><span class="pun" style="color:#666600;">}
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"_id"</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">5983548781331adf45ec6</span><span class="pun" style="color:#666600;">),</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"NoSQL Overview"</span><span class="pun" style="color:#666600;">}
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"_id"</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">5983548781331adf45ec7</span><span class="pun" style="color:#666600;">),</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"New MongoDB - Guia Rapido"</span><span class="pun" style="color:#666600;">}</span></pre>
<p>O exemplo a seguir irá mostrar apenas 2 documentos ao consultarmos o documento.</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln" style="color:#000000;">db</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">find</span><span class="pun" style="color:#666600;">({},{</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">_id</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">0</span><span class="pun" style="color:#666600;">}).</span><span class="pln" style="color:#000000;">limit</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">2</span><span class="pun" style="color:#666600;">)
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDB - Guia Rapido"</span><span class="pun" style="color:#666600;">}</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"NoSQL Overview"</span><span class="pun" style="color:#666600;">}
</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<p>Se você não especificar o argumento número no método limit(), em seguida, ele irá mostrar todos os documentos da coleção.</p>
<h4><span style="text-decoration:underline;">MongoDB Skip() Method</span></h4>
<p>Além de método <strong>limit()</strong> não é nada mais um método <strong>Skip()</strong>, que também aceita argumento de tipo de número e usado para pular número de documentos.</p>
<p>A sintaxe básica do método skip() é como segue abaixo:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">COLLECTION_NAME</span><span class="pun" style="color:#666600;">.</span><span class="pln">find</span><span class="pun" style="color:#666600;">().</span><span class="pln">limit</span><span class="pun" style="color:#666600;">(</span><span class="pln">NUMBER</span><span class="pun" style="color:#666600;">).</span><span class="pln">skip</span><span class="pun" style="color:#666600;">(</span><span class="pln">NUMBER</span><span class="pun" style="color:#666600;">)</span></pre>
<p>No exemplo a seguir deverá ser exibido apenas o segundo documento.</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln" style="color:#000000;">db</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">find</span><span class="pun" style="color:#666600;">({},{</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">_id</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">0</span><span class="pun" style="color:#666600;">}).</span><span class="pln" style="color:#000000;">limit</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">).</span><span class="pln" style="color:#000000;">skip</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">)</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"NoSQL Overview"</span><span class="pun" style="color:#666600;">}</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<p><strong>Nota: O valor default no método skip() é 0</strong></p>
<h4><span style="text-decoration:underline;">Classificando documentos</span></h4>
<p style="text-align:justify;">Para classificar documentos no MongoDB, você precisa usar o método <strong>sort()</strong>. O método<strong> sort()</strong> aceita uma lista de documentos que contém campos, juntamente com a sua ordem de classificação. Para especificar a ordem utiliza-se 1 e -1 como ​​classificação. 1 é usado para a ordem crescente enquanto -1 é usado para a ordem descendente.</p>
<p>A sintaxe básica do comando sort() é como segue abaixo:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">COLLECTION_NAME</span><span class="pun" style="color:#666600;">.</span><span class="pln">find</span><span class="pun" style="color:#666600;">().</span><span class="pln">sort</span><span class="pun" style="color:#666600;">({</span><span class="pln">KEY</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">})</span></pre>
<p>Considerando que a coleção mycol possui os seguintes dados</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"_id"</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">5983548781331adf45ec5</span><span class="pun" style="color:#666600;">),</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDB - Guia Rapido"</span><span class="pun" style="color:#666600;">}
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"_id"</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">5983548781331adf45ec6</span><span class="pun" style="color:#666600;">),</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"NoSQL Overview"</span><span class="pun" style="color:#666600;">}
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"_id"</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">5983548781331adf45ec7</span><span class="pun" style="color:#666600;">),</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"New MongoDB - Guia Rapido"</span><span class="pun" style="color:#666600;">}</span></pre>
<p>O exemplo a seguir irá exibir os documentos ordenados por título em ordem decrescente.</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln">find</span><span class="pun" style="color:#666600;">({},{</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">,</span><span class="pln">_id</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">0</span><span class="pun" style="color:#666600;">}).</span><span class="pln">sort</span><span class="pun" style="color:#666600;">({</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:-</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">})
</span><span class="pun" style="color:#666600;"><span class="pun">{</span><span class="str" style="color:#008800;">"title"</span><span class="pun">:</span><span class="str" style="color:#008800;">"NoSQL Overview"</span><span class="pun">}</span>
{</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"New MongoDB - Guia Rapido</span><span class="str" style="color:#008800;">"</span><span class="pun" style="color:#666600;">}
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"MongoDB - Guia Rapido"</span><span class="pun" style="color:#666600;">}
</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<p>Observe se você não especificar a preferência de classificação, então o método <strong>sort()</strong> irá exibir os documentos em ordem crescente.</p>
<h4><span style="text-decoration:underline;">Indexação no MongoDB</span></h4>
<p style="text-align:justify;">Índices servem para apoiar a resolução eficiente de consultas. Sem índices, o MongoDB deverá digitalizar todos os documentos de uma coleção para depois selecionar os documentos que correspondem a instrução de consulta. Essa verificação é altamente ineficiente e exigem muito do mongod para processar um grande volume de dados.</p>
<p style="text-align:justify;">Índices são estruturas de dados especiais, que armazenam uma pequena parte do conjunto de dados em um formato mais prático. O índice armazena o valor de um campo específico ou um conjunto de campos, ordenados pelo valor do campo, tal como especificado no índice.</p>
<p style="text-align:justify;">Para criar um índice que você precisa para usar o método <strong>ensureIndex()</strong> do MongoDB.</p>
<p><strong>Sintaxe:</strong></p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">COLLECTION_NAME</span><span class="pun" style="color:#666600;">.</span><span class="pln">ensureIndex</span><span class="pun" style="color:#666600;">({</span><span class="pln">KEY</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">})</span></pre>
<p>Aqui chave é o nome do registro em qual você deseja criar o índice e 1 é para ordem crescente. Para criar o índice em ordem decrescente você precisa usar -1.</p>
<p><strong>Exemplo</strong></p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln">ensureIndex</span><span class="pun" style="color:#666600;">({</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">})</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<p>No método <strong>ensureIndex()</strong> você pode passar vários campos, para criar um índice em vários campos.</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln">ensureIndex</span><span class="pun" style="color:#666600;">({</span><span class="str" style="color:#008800;">"title"</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">"description"</span><span class="pun" style="color:#666600;">:-</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">})</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<p>O método <strong>ensureIndex()</strong> também aceita uma lista de opções (que são opcionais), cuja lista é a seguinte:</p>
<table class="src" style="color:#000000;">
<tbody>
<tr>
<th>Parameter</th>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td>background</td>
<td>Boolean</td>
<td>Constrói o índice em segundo plano para que a construção de um índice não bloqueie outras atividades de banco de dados. Especifique true para construir em segundo plano. O valor padrão é <strong>false</strong>.</td>
</tr>
<tr>
<td>unique</td>
<td>Boolean</td>
<td>Cria um índice exclusivo para que a coleção aceite a inserção de documentos em que a chave de índice ou as chaves que correspondam a um valor existente no índice. Especifique <strong>true</strong> para criar um índice exclusivo. O valor padrão é <strong>false</strong>.</td>
</tr>
<tr>
<td>name</td>
<td>string</td>
<td>O nome do índice. Se não for especificado, o MongoDB gera um nome de índice concatenando os nomes dos campos indexados e a ordem de classificação.</td>
</tr>
<tr>
<td>dropDups</td>
<td>Boolean</td>
<td>Cria um índice exclusivo em um campo que pode ter duplicatas. Índices MongoDB  registram apenas a primeira ocorrência de uma chave e removem de todos os documentos da coleção que contêm ocorrências subsequentes desta chave. Especifique <strong>true</strong> para criar um índice único. O valor padrão é <strong>false</strong>.</td>
</tr>
<tr>
<td>sparse</td>
<td>Boolean</td>
<td>Se for <strong>&#8220;true&#8221;</strong>, o índice só faz referência a documentos com o campo especificado. Estes índices usam menos espaço, mas se comportam de forma diferente em algumas situações (particularmente os tipos). O valor padrão é<strong> false</strong>.</td>
</tr>
<tr>
<td>expireAfterSeconds</td>
<td>integer</td>
<td>Especifica um valor, em segundos, como um TTL para controlar quanto tempo MongoDB retém documentos nesta coleção.</td>
</tr>
<tr>
<td>v</td>
<td>index version</td>
<td>O número da versão do índice. A versão índice padrão depende da versão do mongod em execução durante a criação do índice.</td>
</tr>
<tr>
<td>weights</td>
<td>document</td>
<td>O peso é um número que varia de 1 a 99.999 e denota a importância do campo em relação aos outros campos indexados em termos de pontuação.</td>
</tr>
<tr>
<td>default_language</td>
<td>string</td>
<td>Para um índice de texto, a linguagem que determina a lista de palavras de parada e as regras para a <strong>stemmer</strong> e <strong>tokenizador</strong>. O <strong>isenglish</strong> é valor padrão.</td>
</tr>
<tr>
<td>language_override</td>
<td>string</td>
<td>Para um índice de texto, especifique o nome do campo no documento que contém, a linguagem para substituir o idioma padrão. O valor padrão é a linguagem.</td>
</tr>
</tbody>
</table>
<h4><span style="text-decoration:underline;">MongoDB Aggregation</span></h4>
<p>Operações de agregações (Aggregation) processa todos os registros de dados e retorna o resultado calculado. Grupo de operações de agregação de valores a partir de vários documentos juntos podem executar uma variedade de operações nos dados agrupados para retornar um único resultado. Os comandos SQL &#8220;count (*)&#8221; com  &#8220;grupo by&#8221;  seria equivalentes aos grupos de agregação no MongoDB. Para a agregação em mongodb você deve usar o método agregate().</p>
<p>Sintaxe</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">db</span><span class="pun" style="color:#666600;">.</span><span class="pln">COLLECTION_NAME</span><span class="pun" style="color:#666600;">.</span><span class="pln">aggregate</span><span class="pun" style="color:#666600;">(</span><span class="pln">AGGREGATE_OPERATION</span><span class="pun" style="color:#666600;">)</span></pre>
<p>Na coleção você tem os seguintes dados:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">{</span><span class="pln" style="color:#000000;">
   _id</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">7df78ad8902c</span><span class="pun" style="color:#666600;">)</span><span class="pln" style="color:#000000;">
   title</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'MongoDB - Guia Rapido'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;"> 
   description</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'MongoDB - Guia Rapido'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">
   by_user</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'mongodbwise'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">
   url</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'http://www.mongodbwise.wordpress.com'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">
   tags</span><span class="pun" style="color:#666600;">:</span><span class="pun" style="color:#666600;">[</span><span class="str" style="color:#008800;">'mongodb'</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">'database'</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">'NoSQL'</span><span class="pun" style="color:#666600;">],</span><span class="pln" style="color:#000000;">
   likes</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">100
</span><span class="pun" style="color:#666600;">},
</span><span class="pun" style="color:#666600;">{</span><span class="pln" style="color:#000000;">
   _id</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">7df78ad8902d</span><span class="pun" style="color:#666600;">)</span><span class="pln" style="color:#000000;">
   title</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'NoSQL Overview'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;"> 
   description</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'No sql database is very fast'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">
   by_user</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'mongodbwise'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">
   url</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'http://www.mongodbwise.wordpress.com'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">
   tags</span><span class="pun" style="color:#666600;">:</span><span class="pun" style="color:#666600;">[</span><span class="str" style="color:#008800;">'mongodb'</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">'database'</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">'NoSQL'</span><span class="pun" style="color:#666600;">],</span><span class="pln" style="color:#000000;">
   likes</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">10
</span><span class="pun" style="color:#666600;">},
</span><span class="pun" style="color:#666600;">{</span><span class="pln" style="color:#000000;">
   _id</span><span class="pun" style="color:#666600;">:</span><span class="typ" style="color:#7f0055;">ObjectId</span><span class="pun" style="color:#666600;">(</span><span class="lit" style="color:#006666;">7df78ad8902e</span><span class="pun" style="color:#666600;">)</span><span class="pln" style="color:#000000;">
   title</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'MongoDB Java'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;"> 
   description</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'New MongoDB - Guia Rapido'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">
   by_user</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'mongodbbrazil'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">
   url</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">'http://www.mongodbwise.wordpress.com'</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;">
   tags</span><span class="pun" style="color:#666600;">:</span><span class="pun" style="color:#666600;">[</span><span class="str" style="color:#008800;">'java'</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">'database'</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">'NoSQL'</span><span class="pun" style="color:#666600;">],</span><span class="pln" style="color:#000000;">
   likes</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">750
</span><span class="pun" style="color:#666600;">},</span></pre>
<p>Agora, a partir da coleção acima, se você quiser exibir uma lista que quantos tutoriais são escritos por cada usuário, você vai usar o método aggregate()  como mostrado abaixo:</p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln" style="color:#000000;"> db</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">mycol</span><span class="pun" style="color:#666600;">.</span><span class="pln" style="color:#000000;">aggregate</span><span class="pun" style="color:#666600;">([{</span><span class="pln" style="color:#000000;">$group </span><span class="pun" style="color:#666600;">:</span><span class="pun" style="color:#666600;">{</span><span class="pln" style="color:#000000;">_id </span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"$by_user"</span><span class="pun" style="color:#666600;">,</span><span class="pln" style="color:#000000;"> num_tutorial </span><span class="pun" style="color:#666600;">:</span><span class="pun" style="color:#666600;">{</span><span class="pln" style="color:#000000;">$sum </span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">1</span><span class="pun" style="color:#666600;">}}}])
</span><span class="pun" style="color:#666600;">{</span><span class="str" style="color:#008800;">"result"</span><span class="pun" style="color:#666600;">:</span><span class="pun" style="color:#666600;">[
</span><span class="pun" style="color:#666600;">             {</span><span class="str" style="color:#008800;">"_id"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"mongodbwise"</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">"num_tutorial"</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">2
</span><span class="pun" style="color:#666600;">},
</span><span class="pun" style="color:#666600;">             {</span><span class="str" style="color:#008800;">"_id"</span><span class="pun" style="color:#666600;">:</span><span class="str" style="color:#008800;">"mongodbbrazil"</span><span class="pun" style="color:#666600;">,</span><span class="str" style="color:#008800;">"num_tutorial"</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">1
</span><span class="pun" style="color:#666600;">}
</span><span class="pun" style="color:#666600;">],
</span><span class="str" style="color:#008800;">"ok"</span><span class="pun" style="color:#666600;">:</span><span class="lit" style="color:#006666;">1
</span><span class="pun" style="color:#666600;">}
</span><span class="pun" style="color:#666600;">&gt;</span></pre>
<p>O SQL Query equivalente para o caso de uso acima seria<em><strong> &#8220;select by_user, count(*) from mycol group by by_user&#8221;</strong></em></p>
<p>No exemplo acima, temos  documentos agrupados pelo campo <strong>by_user</strong> e em cada ocorrência de<strong> by_user,</strong> o valor anterior da soma é incrementado. Abaixo uma lista de expressões de agregação disponíveis.</p>
<p style="color:#000000;">
<table class="src" style="color:#000000;">
<tbody>
<tr>
<th>Expression</th>
<th>Description</th>
<th>Example</th>
</tr>
<tr>
<td>$sum</td>
<td>Soma-se o valor definido a partir de todos os documentos da coleção.</td>
<td>db.mycol.aggregate([{$group : {_id : &#8220;$by_user&#8221;, num_tutorial : {$sum : &#8220;$likes&#8221;}}}])</td>
</tr>
<tr>
<td>$avg</td>
<td>Calcula a média de todos os valores dados a partir de todos os documentos da coleção.</td>
<td>db.mycol.aggregate([{$group : {_id : &#8220;$by_user&#8221;, num_tutorial : {$avg : &#8220;$likes&#8221;}}}])</td>
</tr>
<tr>
<td>$min</td>
<td>Obtém o mínimo dos valores correspondentes de todos os documentos da coleção.</td>
<td>db.mycol.aggregate([{$group : {_id : &#8220;$by_user&#8221;, num_tutorial : {$min : &#8220;$likes&#8221;}}}])</td>
</tr>
<tr>
<td>$max</td>
<td>Obtém o máximo dos valores correspondentes de todos os documentos da coleção.</td>
<td>db.mycol.aggregate([{$group : {_id : &#8220;$by_user&#8221;, num_tutorial : {$max : &#8220;$likes&#8221;}}}])</td>
</tr>
<tr>
<td>$push</td>
<td>Insere o valor de uma matriz no documento resultante.</td>
<td>db.mycol.aggregate([{$group : {_id : &#8220;$by_user&#8221;, url : {$push: &#8220;$url&#8221;}}}])</td>
</tr>
<tr>
<td>$addToSet</td>
<td>Insere o valor de uma matriz no documento resultante, mas não cria duplicatas.</td>
<td>db.mycol.aggregate([{$group : {_id : &#8220;$by_user&#8221;, url : {$addToSet : &#8220;$url&#8221;}}}])</td>
</tr>
<tr>
<td>$first</td>
<td>Obtém o primeiro documento dos documentos de origem de acordo com o agrupamento. Normalmente, isso só faz sentido em conjunto com alguns anteriormente aplicada “$sort”-stage.</td>
<td>db.mycol.aggregate([{$group : {_id : &#8220;$by_user&#8221;, first_url : {$first : &#8220;$url&#8221;}}}])</td>
</tr>
<tr>
<td>$last</td>
<td>Obtém o último documento dos documentos de origem de acordo com o agrupamento. Normalmente, isso só faz sentido em conjunto com alguns anteriormente aplicada “$sort”-stage.</td>
<td>db.mycol.aggregate([{$group : {_id : &#8220;$by_user&#8221;, last_url : {$last : &#8220;$url&#8221;}}}])</td>
</tr>
</tbody>
</table>
<h4 style="color:#000000;"><span style="text-decoration:underline;">MongoDB Replication</span></h4>
<p style="color:rgb(0,0,0);text-align:justify;">Replicação é o processo de sincronização de dados entre vários servidores. A replicação oferece redundância e aumenta a disponibilidade de dados com várias cópias dos dados em diferentes servidores de banco de dados. A  replicação de um banco de dados além de proteger da perda de um único servidor, também permite que você recupere devido a uma falha de hardware ou interrupções de serviço. Com as cópias adicionais dos dados, você pode dedicar uma para recuperação de desastres, relatórios, ou backup.</p>
<p><strong>Por que replicação?</strong></p>
<ul>
<li>Para manter seus dados seguros</li>
<li>Alta disponibilidade de dados (24&#215;7)</li>
<li>Recuperação de Desastres</li>
<li>Falta de tempo de inatividade para manutenção (como backups, reconstrução de índices, compactação)</li>
<li>Escala  de Leitura(cópias extras para ler)</li>
<li>Conjunto de réplicas transparentes para o aplicativo</li>
</ul>
<p><span style="text-decoration:underline;"><strong>Como a replicação trabalha no MongoDB</strong></span></p>
<p style="text-align:justify;">MongoDB obtêm sua  replicação através da utilização do conjunto de réplicas. Um conjunto de réplicas é um grupo de instances mongod que hospedam o mesmo conjunto de dados. Em uma réplica, um dos nós é o nó principal, que recebe todas as operações de escrita. Todos as outras instances, secundários, aplicam operações do primário de modo que eles tenham o mesmo conjunto de dados. Um conjunto de réplicas (Replica Set) pode ter apenas um nó principal.</p>
<ol>
<li>Conjunto de réplicas é um grupo de dois ou mais nós (geralmente são necessárias 3 nós no mínimo).</li>
<li>Em um conjunto de réplicas, um nó é o nó principal e nós restantes são secundários.</li>
<li>Todos os dados replicam do primário para o nó secundário.</li>
<li>No momento do failover automático ou manutenção, a eleição estabelece qual será o primário e um novo nó principal é eleito.</li>
<li>Após a recuperação do nó que falhou, ele novamente irá se juntar ao conjunto de réplicas e trabalhará como um nó secundário. .</li>
</ol>
<p>Um diagrama típico de replicação mongodb é mostrado abaixo no qual a aplicação do cliente sempre interage com o nó principal, e em seguida, o nó principal repete os dados para os nós secundários.</p>
<p><a href="https://mongodbwise.files.wordpress.com/2014/05/replication.png"><img data-attachment-id="198" data-permalink="https://mongodbwise.wordpress.com/2014/05/22/mongodb-guia-rapido/replication/" data-orig-file="https://mongodbwise.files.wordpress.com/2014/05/replication.png" data-orig-size="500,409" data-comments-opened="1" data-image-meta="{&quot;aperture&quot;:&quot;0&quot;,&quot;credit&quot;:&quot;&quot;,&quot;camera&quot;:&quot;&quot;,&quot;caption&quot;:&quot;&quot;,&quot;created_timestamp&quot;:&quot;0&quot;,&quot;copyright&quot;:&quot;&quot;,&quot;focal_length&quot;:&quot;0&quot;,&quot;iso&quot;:&quot;0&quot;,&quot;shutter_speed&quot;:&quot;0&quot;,&quot;title&quot;:&quot;&quot;}" data-image-title="replication" data-image-description="" data-medium-file="https://mongodbwise.files.wordpress.com/2014/05/replication.png?w=300" data-large-file="https://mongodbwise.files.wordpress.com/2014/05/replication.png?w=500" class="aligncenter wp-image-198 size-full" src="https://mongodbwise.files.wordpress.com/2014/05/replication.png?w=620" alt="replication" srcset="https://mongodbwise.files.wordpress.com/2014/05/replication.png 500w, https://mongodbwise.files.wordpress.com/2014/05/replication.png?w=150 150w, https://mongodbwise.files.wordpress.com/2014/05/replication.png?w=300 300w" sizes="(max-width: 500px) 100vw, 500px"   /></a></p>
<p>&nbsp;</p>
<p><strong>Características do conjunto de réplicas</strong></p>
<ul>
<li>Um Cluster de N nodess</li>
<li>Qualquer nó pode ser o primário</li>
<li>Todas as operações de gravação são efetuadas no nó primário</li>
<li>Failover automático</li>
<li>Recuperação Automática</li>
<li>Consenso de eleição primária</li>
</ul>
<h4><span style="text-decoration:underline;">Configurar um conjunto de réplicas</span></h4>
<p>Neste tutorial vamos converter instância mongod autônoma em um conjunto de réplicas. Para converter em um conjunto de réplicas, siga os passos abaixo indicados:</p>
<ul>
<li>Shutdown do servidor MongoDB</li>
<li>Agora inicie o servidor MongoDB, especificando a opção<strong> &#8211; replSet</strong>. Sintaxe básica do <strong>&#8211; replSet</strong> é dada abaixo:</li>
</ul>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pln">mongod </span><span class="pun" style="color:#666600;">--</span><span class="pln">port </span><span class="str" style="color:#008800;">"PORT"</span><span class="pun" style="color:#666600;">--</span><span class="pln">dbpath </span><span class="str" style="color:#008800;">"YOUR_DB_DATA_PATH"</span><span class="pun" style="color:#666600;">--</span><span class="pln">replSet </span><span class="str" style="color:#008800;">"REPLICA_SET_INSTANCE_NAME"</span></pre>
<p><strong>Exemplo</strong></p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pln">mongod </span><span class="pun" style="color:#666600;">--</span><span class="pln">port </span><span class="lit" style="color:#006666;">27017</span><span class="pun" style="color:#666600;">--</span><span class="pln">dbpath </span><span class="str" style="color:#008800;">"D:\set up\mongodb\data"</span><span class="pun" style="color:#666600;">--</span><span class="pln">replSet rs0</span></pre>
<p>Ele vai iniciar uma instância mongod com o nome RS0, na porta 27017</p>
<ul>
<li>Agora inicie o prompt de comando e se conecte a essa instância mongod.</li>
<li>No console do Mongo execute o comando <strong>rs.initiate()</strong>  para iniciar o novo conjunto de replicas (replica set)</li>
<li>Para verificar algum problema no Conjunto de Replicas (Replica Set), execute o comando <b style="color:#000000;">rs.conf()</b><span style="color:#000000;">.</span></li>
<li>Para verificar o status do Conjunto de Replicas (Replica Set), execute o comando <strong>rs.status()</strong>.</li>
</ul>
<h4><span style="text-decoration:underline;">Geração de Backups no MongoDB</span></h4>
<p><strong>Dump MongoDB Data</strong></p>
<p>Para criar um backup de banco de dados no MongoDB você deve usar o comando <strong>mongodump</strong>. Este comando irá copiar todos os dados de seu servidor no diretório de dump. Há muitas opções disponíveis através do qual você pode limitar a quantidade de dados ou criar backup do seu servidor remoto.</p>
<p><strong>Sintaxe</strong></p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">mongodump</span></pre>
<p><strong>Exemplo</strong></p>
<p>Inicie o seu servidor mongod. Supondo-se que o servidor mongod está sendo executado no localhost e na porta 27017. Agora, abra um prompt de comando e vá para o diretório bin da sua instância MongoDB e digite o comando <em><strong>mongodump</strong></em></p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">mongodump</span></pre>
<p>O comando vai se conectar ao servidor rodando em 127.0.0.1 e na porta 27017 e em seguida envia todos os dados do servidor para o diretório /bin/dump/. Saída do comando é mostrado abaixo:</p>
<p><a href="https://mongodbwise.files.wordpress.com/2014/05/mongodump.png"><img data-attachment-id="199" data-permalink="https://mongodbwise.wordpress.com/2014/05/22/mongodb-guia-rapido/mongodump/" data-orig-file="https://mongodbwise.files.wordpress.com/2014/05/mongodump.png" data-orig-size="680,298" data-comments-opened="1" data-image-meta="{&quot;aperture&quot;:&quot;0&quot;,&quot;credit&quot;:&quot;&quot;,&quot;camera&quot;:&quot;&quot;,&quot;caption&quot;:&quot;&quot;,&quot;created_timestamp&quot;:&quot;0&quot;,&quot;copyright&quot;:&quot;&quot;,&quot;focal_length&quot;:&quot;0&quot;,&quot;iso&quot;:&quot;0&quot;,&quot;shutter_speed&quot;:&quot;0&quot;,&quot;title&quot;:&quot;&quot;}" data-image-title="mongodump" data-image-description="" data-medium-file="https://mongodbwise.files.wordpress.com/2014/05/mongodump.png?w=300" data-large-file="https://mongodbwise.files.wordpress.com/2014/05/mongodump.png?w=620" class="aligncenter wp-image-199 size-large" src="https://mongodbwise.files.wordpress.com/2014/05/mongodump.png?w=620&#038;h=271" alt="mongodump" width="620" height="271" srcset="https://mongodbwise.files.wordpress.com/2014/05/mongodump.png?w=618&amp;h=271 618w, https://mongodbwise.files.wordpress.com/2014/05/mongodump.png?w=150&amp;h=66 150w, https://mongodbwise.files.wordpress.com/2014/05/mongodump.png?w=300&amp;h=131 300w, https://mongodbwise.files.wordpress.com/2014/05/mongodump.png 680w" sizes="(max-width: 620px) 100vw, 620px" /></a></p>
<p>&nbsp;</p>
<p>Abaixo, uma lista de opções disponíveis que podem ser utilizados com o comando mongodump.</p>
<table class="src" style="color:#000000;">
<tbody>
<tr>
<th>Syntax</th>
<th>Description</th>
<th>Example</th>
</tr>
<tr>
<td>mongodump &#8211;host HOST_NAME &#8211;port PORT_NUMBER</td>
<td>Este comando irá fazer obackup todos os bancos de dados especificados na Instance mongod.</td>
<td>mongodump &#8211;host tutorialspoint.com &#8211;port 27017</td>
</tr>
<tr>
<td>mongodump &#8211;dbpath DB_PATH &#8211;out BACKUP_DIRECTORY</td>
<td></td>
<td>mongodump &#8211;dbpath /data/db/ &#8211;out /data/backup/</td>
</tr>
<tr>
<td>mongodump &#8211;collection COLLECTION &#8211;db DB_NAME</td>
<td>Este comando irá fazer o backup somente da collection do banco de dados, especificada.</td>
<td>mongodump &#8211;collection mycol &#8211;db test</td>
</tr>
</tbody>
</table>
<p><span style="text-decoration:underline;"><strong>Restaurando Dados (Restore Data)</strong></span></p>
<p>O comando para restaurar dados de backup do MongoDB é o <em><strong>mongorestore</strong></em>. Este comando irá restaurar todos os dados do diretório de backup.</p>
<p><strong>Sintaxe</strong></p>
<pre class="prettyprint prettyprinted" style="color:#000000;"><span class="pun" style="color:#666600;">&gt;</span><span class="pln">mongorestore</span></pre>