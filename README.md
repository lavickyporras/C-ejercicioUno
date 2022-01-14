#include <iostream>
using namespace std;

class Persona{
    private:
    
    char nombre[20];
    int edad;
    float altura;
    int dni;
    char letra;
    float sueldo;
    
    public:
    //#Declaro métodos:
    void setSueldo(float nuevoSueldo);
    void setLetra(char nuevaLetra);
    void setNombre (char nuevoNombre[20]);
    float getSueldo();
    char getLetra();
    char* getNombre();
};
//#Definir los métodos:
void Persona:: setSueldo(float nuevoSueldo){
   this->sueldo = nuevoSueldo; 
}
void Persona::setLetra(char nuevaLetra){
   this->letra = nuevaLetra;
}
void Persona::setNombre(char nuevoNombre[10]){
    for (int i = 0; i<20; i++){
        this->nombre[i]=nuevoNombre[i];
    }
}

float Persona::getSueldo(){
    return this->sueldo;
}
char Persona::getLetra(){
    return this->letra;
}
char* Persona::getNombre(){
    return this->nombre;
}



int main() {
    Persona persona1;
    
    persona1.setSueldo(100);
    cout<<persona1.getSueldo()<<endl;
    persona1.setLetra('a');
    cout<<persona1.getLetra()<<endl;

    char nombre[20]="Vicky";
    persona1.setNombre(nombre);
    cout<<persona1.getNombre()<<endl;

    char pal1[20]="zanahoria";
    char pal2[20];
    for (int i=0 ; i<20;i++){
        pal2[i]=pal1[i];
    }
    cout<< pal2;

    string palabra1 = "patata";
    string palabra2;
    string palabra2 = palabra1;
    cout<< palabra2<<endl;
    return 0;
}
