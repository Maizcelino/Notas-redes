# Notas-redes
Estas notas sirven para construir redes desde archivos, están organizadas de la siguiente forma:
Estas notas sirven para construir redes desde archivos, están organizadas de la siguiente forma:
- $${\color{lightblue}\textrm{Instalación de la última versión de Phyton para Windows, Linux y para Mac}}$$
- $${\color{lightblue}\textrm{Instalación de pip3}}$$
- $${\color{lightblue}\textrm{Nociones básicas de Python}}$$
- $${\color{lightblue}\textrm{Construcción de gráficas con NetworkX}}$$
- $${\color{lightblue}\textrm{Medidas usuales de redes}}$$




<img width="771" alt="Screenshot" src="https://github.com/user-attachments/assets/d6388dfa-e19d-4888-a293-8c514cc860b0">



  
$${\color{lightblue}\textrm{Instalación de la última versión de Phyton para Windows, Linux y para Mac}}$$

Ir a la siguiente liga, descargar la última versión de python y seguir las instrucciones de instalación
```html
https://www.python.org/downloads/
```
$${\color{lightblue}\textrm{Instalación de pip3}}$$

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

$${\color{lightblue}\textrm{Nociones básicas de Python}}$$

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




$${\color{lightblue}\textrm{Construcción de gráficas con NetworkX}}$$

aqui se pone

$${\color{lightblue}\textrm{Medidas usuales de redes}}$$

```python
adn.count('g')
```


> [!NOTE]
> Highlights information that users should take into account, even when skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Crucial information necessary for users to succeed.

> [!WARNING]
> Critical content demanding immediate user attention due to potential risks.

> [!CAUTION]
> Negative potential consequences of an action.
> 
