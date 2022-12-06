# Sesion_Practica_Unity

Simulación del movimiento de un juego de ajedrez en Unity.
Descargar unity 

Ir a este link: https://unity.com/es/download 

Oprimir donde dice Descargar para Windows, una vez que se haya descargado ahora compilamos el UnityHubSetup y esperamos que instale en el ordenador, esto tomara unos minutos. 

# Crear proyecto 2D 

Ya que este instalado crearemos un projecto 2D con el nombre de tu elección, para eso hacemos clic en “New Project”, luego seleccionamos la opción de 2D, nombrar el proyecto con cualquier nombre y elegir la ubicación donde se guardará; por último, hacer clic en “Create project” 

![image](https://user-images.githubusercontent.com/89043970/205838252-978bcaf0-a8f3-4a15-b321-33dd1a49d814.png)

Descargar chess.png, que se encuentra en este repo (IMPORTANTE: Recordar donde lo guardaste) 

# Crear tilemaps 

Entramos a Window, de ahí nos vamos a 2D y luego a Tile Palette, esto nos abrirá una ventana que podemos poner a lado del Inspector 
![image](https://user-images.githubusercontent.com/89043970/205838340-3f0a1177-ee47-42e8-b02f-8ed9e9317eda.png)

Crear carpeta Sprites dentro de la carpeta Assets, si por default ya la tienen no crearla 
![image](https://user-images.githubusercontent.com/89043970/205838414-03f52bed-7ddb-4f57-af7d-7ec5dc3c577c.png)

Hacer doble clic en la carpeta Sprites para abrirla y luego poner el archivo chess.png dentro 
![image](https://user-images.githubusercontent.com/89043970/205838460-fd1b9f28-15af-4756-aa9e-db28643440bb.png)

Debe quedar de esta manera: 
![image](https://user-images.githubusercontent.com/89043970/205838591-e67af068-7fa2-49be-bb87-5757c8bc052c.png)

Hacerle doble clic, lo que abrirá el inspector, en Sprite Mode poner “Multiple”, en Filter Mode poner “no filter” y en Pixels Per Unit poner “32” 
![image](https://user-images.githubusercontent.com/89043970/205838671-56c40783-27ce-49a1-942c-ba94e80b25b2.png)

Hacer clic en el botón “Apply”, después hacer clic en el botón “Sprite Editor”, lo que abrirá una nueva ventana en la que cortaremos el Sprite en varios pedazos de tamaño 32x32 pixeles. 
![image](https://user-images.githubusercontent.com/89043970/205838736-41bdd44e-64b6-4e2a-81d8-3fac44f8afeb.png)

Hacer clic en Slide y en Pivot poner “Grid by Cell Size” 
![image](https://user-images.githubusercontent.com/89043970/205839038-10df71bc-1ad9-46d4-8f25-17224927f050.png)

Al hacer eso, se nos dará estas opciones y pondremos en Pixel SIze: 32 x 32, luego hacer clic en “Slice” 
![image](https://user-images.githubusercontent.com/89043970/205839078-017f7fcd-4576-4d84-9fe5-4fe78140ce4d.png)

El Sprite cortado debe quedar de esta manera: 
![image](https://user-images.githubusercontent.com/89043970/205838889-2e321b82-19fa-4e3d-8805-ebc1811329e7.png)

Cerrar la ventana y guardar los cambios 
![image](https://user-images.githubusercontent.com/89043970/205839127-30b33692-884f-4dae-93fb-c528ea21c9ca.png)

Crear otras 2 carpetas dentro de Assets llamadas Tiles y TilesPalettes 
![image](https://user-images.githubusercontent.com/89043970/205839259-bccb590e-ed15-4bed-af5a-4c8890cb6a5f.png)

Ahora ir al apartado de Tile Palette y hacer clic en Create New Palette para crear una nueva paleta, como nombre de la paleta pondremos “Chess”, en Grid ponemos “Rectangle” y en Cell Size lo dejamos en “Automatic”; por último, hacer clic en Create 
![image](https://user-images.githubusercontent.com/89043970/205839312-dc35409f-69ca-4ecf-8bf0-fa6382f2a68d.png)

Al crear la paleta nos abrirá una ventana, en la cual tendremos que seleccionar la carpeta TilesPalettes 
![image](https://user-images.githubusercontent.com/89043970/205839360-908452a7-68b4-4ea7-bcfb-d491926a30c2.png)

Arrastrar el archivo chess al Tile Palette y guardarlo en la carpeta TilesPalettes, se verá de esta manera: 
![image](https://user-images.githubusercontent.com/89043970/205839406-6ee27872-0e0c-4e88-862c-3995774b792d.png)

Hacer clic derecho en Hierarchy, seleccionar 2D Object/Tilemap/Rectangular, por defecto crea un Grid como objeto padre, dentro de este se encontrarán todos los Tilemaps creados, al tilemap nombrarlo Background, de la misma manera, hacer el mismo procedimiento y crear otro Tilemap llamado Foreground 
![image](https://user-images.githubusercontent.com/89043970/205839480-1ea50e6d-456c-4a48-bb73-dd86ea67f5f0.png)

Los 2 Tilemaps creados deben verse de esta manera: 
![image](https://user-images.githubusercontent.com/89043970/205839510-c78fb6db-83cd-48cf-992b-c7be550880e4.png)

Seleccionamos Background y vamos al Inspector, en el Inspector ubicar el apartado de Additional Settings y crear una “Sorting Layer”, a la que nombraremos Background, después crear otra y nombrarla Foreground 
![image](https://user-images.githubusercontent.com/89043970/205839559-4cf4a741-9b4d-4b69-a2c7-ea1c35a5390c.png)

Seleccionar el tilemap Background y en Additional Settings seleccionar el Sorting Layer creado llamado Bakground, lo mismo para el tilemap Foreground, seleccionar su Sorting Layer creado llamado Foreground 

Ahora regresar a Tile Palette y en Active Tilemap seleccionar Background 
![image](https://user-images.githubusercontent.com/89043970/205839595-de1b6867-925b-4f23-811e-e895c8c72c99.png)

Seleccionar estos 2 assets y pintarlos en el Scene, hasta crear un pequeño ajedrez 
![image](https://user-images.githubusercontent.com/89043970/205839659-2c4b8743-9b0a-40f6-adcd-718bfa57dcb8.png)

De manera que el Background debe quedar de esta manera: 
![image](https://user-images.githubusercontent.com/89043970/205839698-1164b117-4f89-4620-b822-fc08f56de668.png)

Ahora seleccionar Foreground en Active Tilemap para pintar los bordes 
![image](https://user-images.githubusercontent.com/89043970/205839736-a43f09fd-6f50-4bdc-a134-1d69f85cb82f.png)

Seleccionar estos assets y pintar los bordes hasta que se vea de esta manera: 
![image](https://user-images.githubusercontent.com/89043970/205839772-a64e20cc-f3aa-4d74-b2fa-afbc2b7d6720.png)

Falta agregar al Player que en este caso será la pieza de ajedrez, para esto a crearemos objeto fuera de los Tilemaps, haciendo clic dercho en Hierarchy y luego en 2D Object/Sprites/Square. 
![image](https://user-images.githubusercontent.com/89043970/205839957-b6b05091-9801-4d4d-bf0d-b360ff988a9c.png)

Para que sea visible y este por encima de los que ya aparece en la escena debemos crear un Sorting Layer y asignarselo 
![image](https://user-images.githubusercontent.com/89043970/205840003-814b1291-27da-45a9-a0ce-84bae7435744.png)

Se vera un cuadrado en blanco al que lo podemos pintar con el asset de la pieza de ajedrez 
![image](https://user-images.githubusercontent.com/89043970/205840026-a446b72d-315b-4aef-92da-23c4c1bd654c.png)


# Añadir Coliders 

Para esto, primero debemos agregar ciertos componentes, haremos clic en el botón “Add Component” que se encuentra en el Inspector 
![image](https://user-images.githubusercontent.com/89043970/205840069-38dccd1a-b394-427d-9a95-68edb0234f3e.png)

Sin salir del objecto Player, buscamos los componentes Rigidbody 2D y Box Colider 2D y los agregamos 
![image](https://user-images.githubusercontent.com/89043970/205840114-d3979558-cf97-4df8-88e4-dfd9b3d4fc92.png)

Seleccionar el Tilemap Foreground y añadirle los componentes Tilemap Colider 2D y Composite Colider 2D 
![image](https://user-images.githubusercontent.com/89043970/205840151-cad46435-7741-401e-b49f-0c7107e2f50e.png)

Dentro del Inspector ir al componente Tilemap Colider 2D y habilitar Used By Composite, luego en el componente Rigidbody 2D cambiar Body Type a “Static” 
![image](https://user-images.githubusercontent.com/89043970/205840201-a2aab5f1-52f5-40c1-ac70-ef3ba5ae7fda.png)

Hemos terminado la parte gráfica, a continuación, pasaremos al código para programar el movimiento 


# Código GridMovement  

Crear un Script en la carpeta Assets (un Script representa una clase), para esto hacemos clic derecho en la carpeta Assets luego Create/C# Script y se creara el Script, en el programaremos el codigo para el movimiento de la pieza de ajedrez. Nombrar el archivo “GridMovement” 
![image](https://user-images.githubusercontent.com/89043970/205840302-b0120536-1b3f-4546-96b1-f77aa4e69067.png)

Arrastrar el archivo al Inspector y hacer clic en los 3 puntos ubicados en la esquina superior derecha, seguido de “Edit Sprint”, esto nos abrira una ventana en la que en pesaremos a programar, es importante recordar que Unity esta porgramdo en C# 
![image](https://user-images.githubusercontent.com/89043970/205840439-d74a7652-307e-4d29-93a8-d722cadad39b.png)

Al crear el archivo con los atributos de clase siendo la posición y los inputs del usuario. Tiene dos funciones: actualizar la posición y la que calcula la posición nueva. 

```

using System.Collections; 

using UnityEngine; 

 
 

public class GridMovement : MonoBehaviour 

{ 

    private Vector2 targetPosition; 

    private float xInput, yInput; 

 
 

    void update() 

    { 

        xInput = Input.GetAxisRaw("Horizontal"); 

        yInput = Input.GetAxisRaw("Vertical"); 

 
 

        if (xInput != 0f || yInput != 0f) 

        { 

            CalculateTargetPosition(); 

        } 

    } 

 
 

    private void CalculateTargetPosition() 

    { 

        if (xInput == 1f) 

        { 

            targetPosition = (Vector2)transform.position + Vector2.right; 

        } 

        else if (xInput == -1f) 

        { 

            targetPosition = (Vector2)transform.position + Vector2.left; 

        } 

        else if (yInput == 1f) 

        { 

            targetPosition = (Vector2)transform.position + Vector2.up; 

        } 

        else if (yInput == -1f) 

        { 

            targetPosition = (Vector2)transform.position + Vector2.down; 

        } 

    } 

} 
```
 

Se agrega la función: 
```
private void OnDrawGizmos() 

    { 

        Gizmos.DrawWireSphere(targetPosition, 0.15f); 

    } 
```
 

Se actualiza: 
```

    void update() 

    { 

        private float moveTime = 0.15f; 

 
 

        xInput = Input.GetAxisRaw("Horizontal"); 

        yInput = Input.GetAxisRaw("Vertical"); 

 
 

        if (xInput != 0f || yInput != 0f) 

        { 

            CalculateTargetPosition(); 

            StartCoroutine(Move()); 

        } 

    } 

 
 

    IEnumerator Move() 

    { 

        float timeElapsed = 0f; 

        Vector2 startPosition = transform.position; 

 
 

        while(timeElapsed < moveTime) 

        { 

            transform.position = Vector2.Lerp(startPosition, targetPosition, timeElapsed / moveTime); 

            timeElapsed += Time.deltaTime; 

            yield return null; 

        } 

 
 

        transform.position = targetPosition; 

    } 

 ```
 

Se termina: 
```
using System.Collections; 

using UnityEngine; 

 
 

public class GridMovement : MonoBehaviour 

{ 

    private Vector2 targetPosition; 

    private float xInput, yInput; 

 
 

    void update() 

    { 

        private float moveTime = 0.15f; 

 
 

        xInput = Input.GetAxisRaw("Horizontal"); 

        yInput = Input.GetAxisRaw("Vertical"); 

        private bool isMoving; 

 
 

        if ((xInput != 0f || yInput != 0f) && !isMoving && Input.anyKeyDown) 

        { 

            CalculateTargetPosition(); 

            StartCoroutine(Move()); 

        } 

    } 

 
 

    IEnumerator Move() 

    { 

        isMoving = true; 

        float timeElapsed = 0f; 

        Vector2 startPosition = transform.position; 

 
 

        while(timeElapsed < moveTime) 

        { 

            transform.position = Vector2.Lerp(startPosition, targetPosition, timeElapsed / moveTime); 

            timeElapsed += Time.deltaTime; 

            yield return null; 

        } 

 
 

        transform.position = targetPosition; 

    } 

 
 
 

    private void CalculateTargetPosition() 

    { 

        if (xInput == 1f) 

        { 

            targetPosition = (Vector2)transform.position + Vector2.right; 

        } 

        else if (xInput == -1f) 

        { 

            targetPosition = (Vector2)transform.position + Vector2.left; 

        } 

        else if (yInput == 1f) 

        { 

            targetPosition = (Vector2)transform.position + Vector2.up; 

        } 

        else if (yInput == -1f) 

        { 

            targetPosition = (Vector2)transform.position + Vector2.down; 

        } 

    } 

 
 

    private void OnDrawGizmos() 

    { 

        Gizmos.DrawWireSphere(targetPosition, 0.15f); 

    } 

} 
```
 
