PRACTICA DE COLORPICKER Y DATE PICKER

Captura del código
![](https://i.ibb.co/MSw0rnT/2.png)

Lineas de codigo

	import javafx.application.Application;
	import javafx.geometry.Insets;
	import javafx.geometry.Pos;
	import javafx.scene.Scene;
	import javafx.scene.control.Button;
	import javafx.scene.control.ColorPicker;
	import javafx.scene.control.DatePicker;
	import javafx.scene.control.Label;
	import javafx.scene.layout.VBox;
	import javafx.stage.Stage;

	public class FechaYColorGUI extends Application {

	 @Override
    public void start(Stage primaryStage) {
        // Crear controles
        Label fechaLabel = new Label("Selecciona una fecha:");
        DatePicker datePicker = new DatePicker();
        Label colorLabel = new Label("Selecciona un color:");
        ColorPicker colorPicker = new ColorPicker();
        Button botonConfirmar = new Button("Confirmar");
        Label resultadoLabel = new Label("Resultado:");

        // Crear layout vertical (VBox)
        VBox root = new VBox(10);
        root.setPadding(new Insets(10));
        root.setAlignment(Pos.CENTER);

        // Agregar controles al layout
        root.getChildren().addAll(fechaLabel, datePicker, colorLabel, colorPicker, botonConfirmar, resultadoLabel);

        // Acción al presionar el botón
        botonConfirmar.setOnAction(e -> {
            String fechaSeleccionada = datePicker.getValue().toString();
            String colorSeleccionado = colorPicker.getValue().toString();
            resultadoLabel.setText("Fecha seleccionada: " + fechaSeleccionada + "\nColor seleccionado: " + colorSeleccionado);
            System.out.println("Fecha seleccionada: " + fechaSeleccionada + ", Color seleccionado: " + colorSeleccionado);
        });

        // Crear escena y mostrarla
        Scene scene = new Scene(root, 300, 250);
        primaryStage.setTitle("Fecha y Color GUI");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
	}

####Explicación del codigo
- **Paquete y Clases**
El código está en el paquete application y la clase principal es Main, que extiende la clase Application de JavaFX.

- **Método start**
Creación de Controles: Se crean varios controles de la interfaz, incluyendo etiquetas (Label), un selector de fechas (DatePicker), un selector de colores (ColorPicker), un botón (Button), y una etiqueta para mostrar resultados.

Diseño del Layout: Se utiliza un VBox (layout vertical) para organizar los controles con un espacio de 10 píxeles entre ellos y con un padding de 10 píxeles.

Acción del Botón: Se define una acción para el botón "Confirmar", que recoge las selecciones del DatePicker y ColorPicker y las muestra en la etiqueta de resultado. También imprime estas selecciones en la consola.

- **Escena y  Ventana**
Se crea una escena (Scene) con el VBox como raíz y se establece en el primaryStage.
El título de la ventana se establece como "Fecha y Color GUI" y se muestra la ventana.

-**Método main**
Inicia la aplicación JavaFX llamando a launch(args).


Datepicker y Colorpicker

Datepicker
Es un componente de interfaz de usuario que permite a los usuarios seleccionar una fecha desde un calendario gráfico. Este componente se utiliza comúnmente en formularios web y aplicaciones para facilitar la entrada de fechas, evitando errores en el formato y mejorando la experiencia del usuario.

Colorpicker
Es un componente de interfaz de usuario que permite a los usuarios seleccionar un color. Este componente es comúnmente utilizado en aplicaciones gráficas, editores de texto, diseño web y cualquier aplicación que requiera la elección de colores. El colorpicker facilita la selección precisa de colores mediante una interfaz gráfica que puede incluir una paleta de colores, un selector de tonos, y a veces un campo para ingresar códigos de color directamente.

###Conclusión del código
Este código implementa una aplicación JavaFX básica que permite a los usuarios seleccionar una fecha y un color. La selección se muestra tanto en una etiqueta dentro de la interfaz como en la consola. El uso de controles básicos de JavaFX y un layout sencillo hace que la aplicación sea fácil de entender y extender.


