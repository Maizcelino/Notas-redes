# Notas-redes
Estas notas sirven para construir redes desde archivos, están organizadas de la siguiente forma:
Estas notas sirven para construir redes desde archivos, están organizadas de la siguiente forma:
- $${\color{lightblue}\textrm{Instalación de la última versión de Phyton para Windows, Linux y para Mac}}$$
- $${\color{lightblue}\textrm{Instalación de pip3}}$$
- $${\color{lightblue}\textrm{Nociones básicas de Python}}$$
- $${\color{lightblue}\textrm{Construcción de gráficas con NetworkX}}$$
- $${\color{lightblue}\textrm{Medidas usuales de redes}}$$


  
$${\color{lightblue}\textrm{\large Instalación de la última versión de Phyton para Windows, Linux y para Mac}}$$

Ir a la siguiente liga, descargar la última versión de python y seguir las instrucciones de instalación
```html
https://www.python.org/downloads/
```
Se recomienda instalar Visual Studio Code y usarlo como editor de texto. Ir a la siguiente liga, descargar e instalar.
```html
https://code.visualstudio.com/download
```
$${\color{lightblue}\textrm{\large Instalación de pip3}}$$

$${\color{lightblue}\textrm{Windows}}$$

Abrir terminal en windows
1. Haz clic derecho en el menú Inicio de Windows
2. Haz clic izquierdo en la opción Run o Ejecutar.
3. Escribe en el recuadro "cmd" y haz clic en "Aceptar" para abrir la terminal:

Para instalar pip3 copiar lo siguiente en la terminal

```python
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
```
Con CD moverse a la carpeta donde fue descargado y escribir el siguiente comando para instalar pip3 y todas sus dependencias
```python
python3 get-pip.py
```
$${\color{lightblue}\textrm{Mac o Linux}}$$

En terminal escribir
```python
curl -O https://bootstrap.pypa.io/get-pip.py
```
Nuevamente en terminal escribir
```python
sudo python3 get-pip.py
```

$${\color{lightblue}\textrm{\large Nociones básicas de Python}}$$

$${\color{lightblue}\textrm{Variables}}$$

No se necesitan declarar las variables

```python
x=13
y=x+3.0
```

Asignación múltiple

```python
a,b=4,5
```

Tipos de variable
```python
type(y) 
float(x)
int(y)
```

En python una cadena se declara con comilla simple 
```python
adn='agtcaggagttaaccata'
adn_corto='cgta'
```
o se declara con comillas
```python
frase="I can’t Believe It, It’s amazing"
texto='UPN 201, Educar para transformar'
```

```python
adn+adn_corto
texto*3
frase.lower()
len(adn)
adn.count('g')
adn.replace('g','TAZA')
'a' in adn
texto.split()
texto.split(',')
cadena='3*una,*español-ingles,*algo'
cadena.split('*')
```

> [!IMPORTANT]
> Ejercicio
> 
> Escribir una cadena con las letras a,g,t,c y calcular el porcentaje de ocurrencia de a y c.
>
> Intercambiar la a por la c y la c por la a.

> [!NOTE]
> El uso de los índices es similar tanto para listas, cadenas, etc. 


```python
# toma en la cadena desde el índice inicio hasta el indice fin-1 
pos='Escuela de Otoño de Biología Matemática'
# saltos dice de cuanto en cuanto se van tomando. Si no se pone, se va de uno en uno
pos[inicio:final:saltos]
```

```python 
pos[0]
pos[1:4]
pos[5:2]
pos[5:2:-1]
pos[1:]
pos[1:100]
pos=[::-1]
pos[:-3]
pos[-3:]
```

$${\color{lightblue}\textrm{Listas}}$$

```python
#colección de objetos
L1=[2,7,11,-3]
#distintos tipos de elementos
L2=[5,'gato',1,0]
#puede estar vacia
c=[]
#puede ser una lista de listas 
Listas=[12,[‘a’,1,2,3],[b,[c,14]]]
#genera una lista desde inicio hasta final menos uno.
#paso si se da debe ser entero,indica el tamaño de paso.
range(inicio,final,paso)
```

tutorial 
https://recursospython.com/guias-y-manuales/listas-y-tuplas/

```python
L1+L2
L2*3
x=L2[-1]
z=L1[2:4]
L1[0]=250
len(Listas)
Listas[1][2]
L1.index(11)
L2.append(-12)
```

$${\color{lightblue}\textrm{Tuplas}}$$

```python
#tupla de objetos
T=(1,2,4,'x0',-13)
#tupla de un elemento
f=(4,)
#tupla vacia para 2.x, en 3.x no lleva coma
g=(,)
#tupla de tuplas
Tupla=(12,(4,[1,3]),(3,[6,2]))
```

> [!NOTE]
> Las tuplas son inmutables

```python
#índice
T[0]
T[0]='hola'
#índice de la tupla de tuplas
Tupla[2][1]
```

$${\color{lightblue}\textrm{Diccionarios}}$$
```python
dic1={'jaguar':'venados, pecaríes, tapires','ocelote':'roedores, conejos, ciervos', 'puma':'zorros'}
#se agrega un elemento
dic1['puma']='venado, puerco espin, mapaches'    
#diccionario vacio
D={}                                  
```

```python
dic1['jaguar']
len(dic1)
dic1.keys()
dic1.values()
dic1[(3,4)]=[5,7,'si se puede']
dic1['nombre']='Miguel'
del dic1['jaguar']
dic1['ocelote'].split()
dic1['ocelote'].split(',')
dic1[[3,4]]='no se puede'
```

$${\color{lightblue}\textrm{Otra forma de hacer diccionarios}}$$

```python
#Elemento a elemento
D={}
D['Oaxaca']='Oaxaca'
#Por tuplas
D=dict([('Chiapas', 'Tuxtla Gutierrez'),('Yucatan','Merida')])
#A partir de dos listas
lista1=['a','b','c','d']
lista2=[12,13,14,15]
D=dict(zip(lista1,lista2))
```


$${\color{lightblue}\textrm{\large Construcción de gráficas con NetworkX}}$$

```python
import networkx as nx
G = nx.Graph() # Grafo no dirigido
G.add_nodes_from([2,'x','y',9])
G.add_edges_from([(2,'x'),('x','y'),('y',9)])
G.size() #cantidad de aristas
G.order() #cantidad de nodos
import matplotlib.pyplot as plt
nx.draw(G)
plt.show()
G.order()    #orden de gráfica
G.size()      #numero de aristas
```

```python
# Algunas modificaciones
G.add_node(12)				#agrega un nodo
G.add_edge(23,45)			#agrega aristas, incluso si no tiene nodos
G.nodes()			len(G)			#muestra los nodos
G.edges()						#muestra las aristas
G.remove_node(9)				#elimina nodos
G.remove_edges_from( [(2,'x'),(23,45)] ) 	#elimina aristas
```

```python 
import matplotlib.pyplot as plt
K10 = nx.complete_graph(10)
K10.nodes()
K10.size()
nx.draw(K10)
plt.show()
nx.draw_circular(K10)
plt.show()
nx.draw_circular(K10,node_color='b',node_size=500,alpha=0.3)
plt.show()
K10.degree(3)
K10.degree()
K10.neighbors(3)
```

```python 
Gw = nx.Graph()
Gw.add_edge('a','b', weight = 0.1)
Gw.add_edge('b','c', weight = 1.5)
Gw.add_edge('a','c', weight = 1.0)
Gw.add_edge('c','d', weight = 2.2)
weights = [Gw[u][v]['weight'] for u,v in Gw.edges()]
nx.draw(Gw,width=weights,with_labels=True,node_size=700)
plt.show()
```

$${\color{lightblue}\textrm{Dibujar gráfica con pesos }}$$

```python 
Gw = nx.Graph()
Gw.add_edge('a','b', weight = 3)
Gw.add_edge('b','c', weight = 1.5)
Gw.add_edge('a','c', weight = 1.0)
Gw.add_edge('c','d', weight = 2.2)
weights = [Gw[u][v]['weight'] for u,v in Gw.edges()]  
pos =nx.spring_layout(Gw)
nx.draw_networkx_nodes(Gw, pos, node_size=500) #nodos
nx.draw_networkx_edges(Gw, pos,   width=weights, alpha=0.5, edge_color='black') 
nx.draw_networkx_edge_labels(Gw,pos,edge_labels={(u,v):Gw[u][v]['weight'] for u,v in Gw.edges()} ,font_color='red')
nx.draw_networkx_labels(Gw, pos, font_size=20, font_family='sans-serif')  #etiquetas para nodos
plt.axis('off') 
plt.show()
```

> [!NOTE]
> Se le pueden poner tantos atributos a los artistas y a los nodos como se quieran, lo importante es tomar en cuenta que el conjunto de nodos y aristas es un objeto tipo diccionario: peso =  25332, etiqueta = 'ljdfñlkajs' , perrro = 'gajlkñdsa', etc.. 

```python 
GL.add_edge('a','b', weight = 3, label = 'primera', perro = "tomas")
```
$${\color{lightblue}\textrm{Tipos de gráficas}}$$

```python 
G=nx.Graph() 			# no dirigida, simple
G.to_directed()			# se convierte a dirigida
H=nx.DiGraph			# dirigida, simple
H.to_undirected()		# se convierte a no dirigida
MG=nx.MultiGraph()	# no dirigida, aristas múltiples
MD=nx.MultiDiGraph()	# dirigida, aristas múltiples
```

$${\color{lightblue}\textrm{Ejemplo digráfica}}$$

```python
yeastG = nx.read_edgelist('yeast.data', create_using=nx.DiGraph())
#cantidad de aristas
yeastG.size()
# cantidad de nodos
yeastG.order()
#lee el archivo y crea una digráfica
# se crea un diccionario 
salida=dict(yeastG.out_degree())
#accede valores del diccionario
# se hace el histograma
grado_salida=salida.values()
plt.hist(grado_salida) 
plt.show
```



$${\color{lightblue}\textrm{\large Medidas usuales de redes}}$$

$${\color{lightblue}\textrm{Tomar la componente conexa más grande (CC max)}}$$

```python
yeastG= nx.read_edgelist('yeast.data',create_using=nx.DiGraph())
YNG=yeastG.to_undirected()			#yeastG la vuelve no dirigida
largest_cc = max(nx.connected_components(YNG), key=len) #set de nodos de la CC max
MCC=YNG.subgraph(largest_cc)		#crea una subgrafica con el conjuto largest_cc
nx.draw(MCC)
plt.show()
```

$${\color{lightblue}\textrm{excentricidad, diámetro y radio de yeast.data}}$$

```python
nx.diameter(MCC)
nx.radius(MCC)
MCC.degree()
nx . closeness_centrality ( G )		#investigar
nx . betweenness_centrality ( G )		#investigar	
nx . pagerank (G , alpha =0.9)		#investigar
```

$${\color{lightblue}\textrm{Importar redes desde Excel}}$$

```python
import pandas as pd
archivo=pd.read_excel("Verticesmamiferos.xlsx") 	#se lee el archivo de excel
nombre_nodo=archivo['nombre'].values.tolist()	#la columna ‘nombre’ de excel se hace lista
clave_nodo=archivo['clave'].values.tolist()		#la columna ‘clave’ de excel se hace lista
labels=dict(zip(clave_nodo,nombre_nodo))		#se hace un diccionario con las listas
```

