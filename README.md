#EJERCICIO_1
#!/bin/bash
echo "introduce un numero"
read num;
if [ $num -ge 0 ]; then
    echo "$num es positivo";
    else
        echo "$num no es positivo";
fi;

#EJERCICIO_2
#!/bin/bash
echo "introduce un numero"
read num;
if [ $num -lt 0 ]; then
    echo "$num es negativo";
    else 
        echo "$num no es negativo";
fi;

#EJERCICIO_3
#!/bin/bash
echo "introduce un numero";
read num;
if [ $num -eq 0 ]; then
    echo "el numero introducido es cero";
    else
        echo "el numero introducido no es cero";
fi;

#EJERCICIO_4
#!/bin/bash
echo "introduce un numero";
read num;
if [ $num -eq 0 ]; then
    echo "el numero introducido es un cero";
    elif [ $num -gt 0 ]; then
        echo "el numero introducido es positivo";
        else
            echo "el numero introducido es negativo";
fi;

#EJERCICIO_5
#!/bin/bash
set -- "1" "2" "3" "4";
if [ $# -ne 3 ]; then
    echo "error: no hay tres parametros";
    else
        echo "hay tres parametros";
fi;

#EJERCICIO_6
#!/bin/bash
set -- 6 8 2;
if [ $# -ne 2 ]; then
echo "tienen que ser dos parametros";
else
    let suma=$(($1 + $2));
    echo "$1 + $2 = $suma "
fi;

#EJERCICIO_7
#!/bin/bash
let num1=6;
let num2=8;
let op="x";
if [ $# -ne 3 ]; then
echo "tienen que ser tres parametros";
elif [ $3 -ne "+" ] && [ $3 -ne "-" ] && [ $3 -ne "x" ] && [ $3 -ne "/" ]; then
    echo "las operaciones indicadas por el tercer parametros solo pueden ser "+" "-" "x" "/"";
    elif [ $3 -eq "+"]; then
        let operacion=$(($1 + $2)); 
        echo operacion;
        elif [ $3 -eq "-"]; then
            let operacion=$(($1 - $2)); 
            echo operacion;
            elif [ $3 -eq "x"]; then
                let operacion=$(($1 * $2)); 
                echo operacion;
                elif [ $3 -eq "/"]; then
                    let operacion=$(($1 / $2)); 
                    echo operacion;
fi;


#EJERCICIO_8
#!/bin/bash
if [ fichero.sh -e ]; then
echo "el fichero existe";
else
    echo "el fichero no existe";
fi;

#EJERCICIO_9
#!/bin/bash
if [ fichero.sh -d ]; then
echo "es un directorio";
else
    echo "es un fichero";
fi;

#EJERCICIO_10
#!/bin/bash
if [ fichero.txt -r ]; then
echo "tiene permisos para leer"
else
    echo "no tiene permisos para leer";
fi;

if [ fichero.txt -w ]; then
echo "tiene permisos para escribir"
else
    echo "no tiene permisos para escribir";
fi;
    
if [ fichero.txt -x ]; then
echo "tiene permisos para ejecutar"
else
    echo "no tiene permisos para ejecutar";
fi;

#EJERCICIO_11
#!/bin/bash
for i in {1..50}
do
echo "hola"
done

#EJERCICIO_12
#!/bin/bash
for i in {1..10}
do
echo "introduce una palabra";
read palabra;
echo $palabra;
done

#EJERCICIO_13
#!/bin/bash
let num=6;
for i in $(seq 1 $num)
do
echo "hola"
done

#EJERCICIO_14
#!/bin/bash
let n=6;
for i in $(seq 0 $n)
do
echo $i
done

#EJERCICIO_15
#!/bin/bash
let n=6;
for i in $(seq 1 $n)
do
let suma+=$i;
done
echo "la suma de todos los numeros del 1 hasta $n es $suma";

#EJERCICIO_16
#!/bin/bash
let num1=6;
let num2=8;
echo "el primer numero antes de la transformacion es $num1 y el segundo es $num2";
let temp=$num2;
let num2=$num1;
let num1=$temp;
echo "el primer numero tras la transformacion es $num1 y el segundo es $num2";

#EJERCICIO_17
#!/bin/bash
palabra="";
while [ "$palabra" != ":q" ];
do
read palabra;
done

#EJERCICIO_18
#!/bin/bash
palabra="";
echo "" >> archivo.txt;
while [ "$palabra" != ":q" ];
do
read palabra;
echo $palabra >> archivo.txt;
done

#EJERCICIO_19
#!/bin/bash
palabra="";
echo "" >> archivo2.txt;
while [ "$palabra" != ":q" ]
do
read palabra;
echo $palabra >> archivo2.txt;
done
sort archivo2.txt;

#EJERCICIO_20

