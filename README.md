CLASE CUENTA:
public class Cuenta {
	
	//#1 ATRIBUTOS:
    private String titular;
    private double cantidad;
    
    
    //#2 CONSTRUCTORES:
    public Cuenta (String titular) {
        this (titular, 0); 
    }
 
    public Cuenta (String titular, double cantidad) {
        this.titular = titular;
        
     // - Si la cantidad es menor que cero, lo ponemos a cero
        if (cantidad < 0) {
            this.cantidad = 0;
        } else {
            this.cantidad = cantidad;
        }
    }
    
    //#3 METODOS:
    public String getTitular() {
        return titular;
    }
 
    public void setTitular (String titular) {
        this.titular = titular;
    }
 
    public double getCantidad() {
        return cantidad;
    }
 
    public void setCantidad (double cantidad) {
        this.cantidad = cantidad;
    }


    //#4 METODOS ESPECIALES:
     // - Ingresar
    public void ingresar (double cantidad) {
        if(cantidad > 0){
        }
    }
    
     // - Retirar
    public void retirar (double cantidad) {
        if (this.cantidad - cantidad < 0) {
            this.cantidad = 0;
        } else {
            this.cantidad -= cantidad;
        }
    }
    
     // - Return
    public String toString() {
        return "El titular " + titular + " tiene " + cantidad + " euros en la cuenta";
    }
    
    //


    
}

CLASE PERSONA:
public class Persona {
	
	//PUNTO #5
	 //1 - Atributos
	 private String nombre;
	 private char sexo;
	 private int edad;
	 private int dni;
	 private double peso;
	 private double altura;
	
	 //2 - Constructores:
	  //Constructor por defecto
	  public Persona(){
        
      }
	  
	  //Constructor con nombre, etc
	  public Persona (Persona persona){
		  
          this.nombre = persona.nombre;
          this.sexo = persona.sexo;
          this.edad = persona.edad;
          this.dni = persona.dni;
          this.peso = persona.peso;
          this.altura = persona.altura;
             
      }
	  
	  //Constructor con todos los atributos como parámetro
	  public Persona(String nom, char sexo, int edad, int dni, double peso, double altura){
		  
          this.nombre = nom;       
          this.sexo = sexo;
          this.edad = edad;
          this.dni = dni;
          this.peso = peso;
          this.altura = altura;
                    
      }
	  
	 //3 - Metodos
	  //El metodo uno esta en la clase CalcularImc ->
	  
	  //Metodo dos
	  public void mayorEdad(int edad){
          if (edad > 18)
        	  
                  System.out.println("Es mayor de edad");
          else
                  System.out.println("Es menor de edad");
      }
	  //Metodos tres
	     
      public void genero(char sexo) {
     
      if (sexo=='h'){
          System.out.println("Eres hombre");
      }
      else if (sexo=='m'){
          System.out.println("Eres mujer");
      }
     
      }
      
    
	  
	
}

CLASE CALCULARIMC:
//PUNTO #5 - Numero 3 METODO UNO
import java.util.Scanner;

public class CalcularImc {

    public static void main(String[] args) {

        Scanner teclado = new Scanner(System.in);
     
        double peso, altura, imc;

        System.out.println("Cual es su peso ");
        peso = teclado.nextDouble();
        altura = teclado.nextDouble();

        imc = peso/(altura*altura);
        System.out.println("SU IMC ES: " + imc);
    
        if (imc < 20.00) {
            System.out.println("-1");

        } else if (imc >= 20.01 && imc <= 25.00) {
            System.out.println("0");

        } else if (imc >= 25.00) {
            System.out.println("1");

        }

    }

 

}
