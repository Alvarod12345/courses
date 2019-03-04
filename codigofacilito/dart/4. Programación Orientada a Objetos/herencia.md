# Herencia
La herencia es una de las propiedades principales de la Programación Orientada a Objetos.
Ejemplo:
```
class Persona {
  String nombre;
  int edad;
}

class Hombre extends Persona {}

main() {
  var juan = new Hombre();
  juan.nombre = "Juan";
  print(juan.nombre);
}
```
En este caso, al decir que 'Hombre' es una clase que extiende de 'Persona' adquiere las propiedades y además los métodos.
> Todo lo que está dentro de 'Persona' también lo tiene 'Hombre'.

# Sobre escribir métodos
Los métodos que son heredados tiene un comportamiento predeterminado en su clase principal. Para sobreescribir éstos utilizamos @override
Agregamos un método a Persona:
```
class Persona {
  String nombre;
  int edad;

  void sumarEdad() {
    this.edad = 20;
    print(this.edad);
  }
}

class Hombre extends Persona {
  // Sobreescribimos el método
  @override
  void sumarEdad() {
    // Sobreescribimos la variable
    this.edad = 30;
    print(this.edad);
  }
}

main() {
  var juan = new Hombre();
  juan.sumarEdad(); // 30
}
```
# Constructor
Cuando la clase de la que heramos tiene un constructor, necesitamos definir por lo menos el mismo constructor si es que no queremos personalizarlo.
```
class Persona {
  String nombre;
  int edad;

  Persona(this.nombre, this.edad)
}

class Hombre extends Persona {
  Hombre(String nombre, int edad):super(nombre, edad);
}
```
El construtor de 'Hombre' se va a comportar en este caso igual que el de 'Persona'  .