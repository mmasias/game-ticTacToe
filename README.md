# Secuencia de versiones TicTacToe

## :information_source: Este diagrama muestra las diferentes versiones del juego TicTacToe

| Requistios  | Versión |
|:------------- |:-------------|
| [basic](https://github.com/mmasias/game-ticTacToe-domains/blob/master/1.0.basic/README.md) | [domainModel - basic](domainModel/basic) |
| [machine](https://github.com/mmasias/game-ticTacToe-domains/blob/master/1.1.machine/README.md) | [domainModel - machine](domainModel/machine) |
| [basic](https://github.com/mmasias/game-ticTacToe-domains/blob/master/1.0.basic/README.md) | [documentView - basic](documentView/basic) |
| [machine](https://github.com/mmasias/game-ticTacToe-domains/blob/master/1.1.machine/README.md) | [documentView - machine - doubleDispatching](documentView/machine/doubleDispatching) |
| [machine](https://github.com/mmasias/game-ticTacToe-domains/blob/master/1.1.machine/README.md) | [documentView - machine - prototype](documentView/machine/prototype) |
| [graphics](https://github.com/mmasias/game-ticTacToe-domains/blob/master/2.0.graphics/README.md) | [documentView - withoutFactoryMethod](documentView/withoutFactoryMethod) |
| [graphics](https://github.com/mmasias/game-ticTacToe-domains/blob/master/2.0.graphics/README.md) | [documentView - withFactoryMethod](documentView/withFactoryMethod) |
| [graphics](https://github.com/mmasias/game-ticTacToe-domains/blob/master/2.0.graphics/README.md) | [modelViewPresenter - presentationModel - basic](modelViewPresenter/presentationModel/basic) |
| [graphics](https://github.com/mmasias/game-ticTacToe-domains/blob/master/2.0.graphics/README.md) | [modelViewPresenter - presentationModel - withFacade](modelViewPresenter/presentationModel/withFacade) |
| [graphics](https://github.com/mmasias/game-ticTacToe-domains/blob/master/2.0.graphics/README.md) | [modelViewPresenter - presentationModel - withoutDoubleDispatching](modelViewPresenter/presentationModel/withoutDoubleDispatching) |
| [graphics](https://github.com/mmasias/game-ticTacToe-domains/blob/master/2.0.graphics/README.md) | [modelViewPresenter - presentationModel - withDoubleDispatching](modelViewPresenter/presentationModel/withDoubleDispatching) |
| [undoRedo](https://github.com/mmasias/game-ticTacToe-domains/blob/master/3.0.undoRedo/README.md) | [modelViewPresenter - presentationModel - withComposite](modelViewPresenter/presentationModel/withComposite) |
| [distributed](https://github.com/mmasias/game-ticTacToe-domains/blob/master/4.0.distributed/README.md) | [modelViewPresenter - presentationModel - withoutProxy](modelViewPresenter/presentationModel/withoutProxy) |
| [distributed](https://github.com/mmasias/game-ticTacToe-domains/blob/master/4.0.distributed/README.md) | [modelViewPresenter - presentationModel - withProxy](modelViewPresenter/presentationModel/withProxy) |
| [files](https://github.com/mmasias/game-ticTacToe-domains/blob/master/5.0.files/README.md) | [modelViewPresenter - presentationModel - withoutDAO](modelViewPresenter/presentationModel/withoutDAO) |
| [files](https://github.com/mmasias/game-ticTacToe-domains/blob/master/5.0.files/README.md) | [modelViewPresenter - presentationModel - withDAO](modelViewPresenter/presentationModel/withDAO) |
| [bbdd](https://github.com/mmasias/game-ticTacToe-domains/blob/master/6.0.bbdd/README.md) | [modelViewPresenter - presentationModel - withoutPrototype](modelViewPresenter/presentationModel/withoutPrototype) |
| [bbdd](https://github.com/mmasias/game-ticTacToe-domains/blob/master/6.0.bbdd/README.md) | [modelViewPresenter - presentationModel - withPrototype](modelViewPresenter/presentationModel/withPrototype) |
| [basic](https://github.com/mmasias/game-ticTacToe-domains/blob/master/1.0.basic/README.md) | [modelViewPresenter - passiveView](modelViewPresenter/passiveView) |
| [basic](https://github.com/mmasias/game-ticTacToe-domains/blob/master/1.0.basic/README.md) | [modelViewPresenter - supervisorController](modelViewPresenter/supervisorController) |
| [basic](https://github.com/mmasias/game-ticTacToe-domains/blob/master/1.0.basic/README.md) | [modelViewController](modelViewController) |

![DiagramaSecuencia](/docs/diagrams/out/TicTacToe/TicTacToe.svg)

# Configuration

### ❗ La instalación corresponde al entorno Visual Studio Code.

:one: Realizar la instalacion , abrir el CMD como administrador.
  
:heavy_minus_sign: Primer comando

	@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
	
:heavy_minus_sign: Segundo comando
    
    choco install plantuml

:two: Instalar el plugin de plantUML para Visual Studio Code.

	2.1 En plantUML Ir a extensiones y escribir escribir plantuml.
	
	2.2 Botón derecho sobre la primera (PlantUML Rich PlantUML support) -> Extension Settings
   
  	2.3 Apartado Plantuml: Diagrams Root (Se establece la carpeta donde van a estar localizados los diagramas .png
		Ruta: "docs/diagrams/src"

	2.4 Apartado Plantuml: Export Out Dir (Se establece la carpeta para exportar los diagramas)
		Ruta: "docs/diagrams/out"

	2.5 Apartado Plantuml: Render 
		Cambiar la opción de "Local" a "PlantUMLServer"
	
	2.6 Plantuml: Server (Establecer servidor de PlantUML)
		Escribir la ruta oficial del servidor de Plantuml: "https://www.plantuml.com/plantuml"


:three: Dentro de nuestro proyecto debemos tener una carpeta **docs/** con la siguiente estructura. La carpeta **/out** se va a a generar automaticamente al exportar los diagramas.
	
- :file_folder: Project Folder/
    - :file_folder: docs/  
        - :file_folder:diagrams/  
            - :file_folder:src/  
                - :file_folder:architecture_overview.wsd  
            - :file_folder: out/  
                - :file_folder: architecture_overview/  
                    - :file_folder: architecture_overview.png  
  - :file_folder: rest_of_your_project_folders/  
  

:four: Para generar el diagrama es necesario presionar **Alt+D**, la primera vez, despues se recarga automaticamente.

:five: Exportar un diagrama, **boton derecho "Export current diagram"** se genera el "svg" en la carpeta out/
  + Se genera una carpeta con el nombre del fichero.

:six: Paginación en un diagrama, util para digramas grandes.
  - newpage
  - title: Justo debajo de newPage, para indicar en que se centra el diagrama.


#### :heavy_exclamation_mark: No es necesario instalar el plugin para hacer la documentación. Se pueden exportar los diagramas en svg en plantext y meterlos en la carpeta out/nombrefichero/nombrediagrama.svg  Respetando la estructura del punto
