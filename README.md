# C-ejercicioUno
#include <iostream>
using namespace std;

class Persona{
    private:

    char nombre[20];
    int edad;
    int numero;
    float altura;
    int dni;
    char letra;
    float sueldo;

    public:
    //#Declaro métodos:
    void setSueldo(float nuevoSueldo);
    void setLetra(char nuevaLetra);
    //void setNombre (char nuevoNombre[20]);
    float getSueldo();
    char getLetra();
};
//#Definir los métodos:
void Persona:: setSueldo(float nuevoSueldo){
   this->sueldo = nuevoSueldo;
}
void Persona::setLetra(char nuevaLetra){
   this->letra = nuevaLetra;
}
//void Persona::setNombre(char nuevoNombre[20]){
    //this->nombre = nuevoNombre;
//}

float Persona::getSueldo(){
    return this->sueldo;
}
char Persona::getLetra(){
    return this->letra;
}



int main() {
    Persona persona1;

    persona1.setSueldo(100);
    cout<<persona1.getSueldo()<<endl;
    persona1.setLetra('a');
    cout<<persona1.getLetra()<<endl;
    return 0;
}
