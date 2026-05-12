# WinTriage (fork binario DFIR)

Este repositorio contiene un fork del proyecto original **WinTriage** de Karol Pivo, más un binario precompilado para facilitar su uso en entornos de respuesta a incidentes donde no se dispone de Python instalado.

WinTriage automatiza la ejecución de múltiples comandos nativos de Windows (netstat, wmic, reg query, tasklist, etc.) y la recolección de artefactos clave (event logs, ficheros recientes y modificados, etc.) para ayudar a un analista DFIR a determinar rápidamente si un host Windows puede estar comprometido.

## Características principales

- Recolección rápida de información de red, procesos, servicios, tareas programadas y claves de registro relevantes.  
- Copia de logs de eventos Windows en formato nativo `.evtx`.  
- Opcionalmente, listado de ficheros creados o modificados después de una fecha dada mediante el flag `-d`.  
- Pensado para ejecutarse desde un pendrive o share de red, sin instalación en el sistema víctima.  

## Binario incluido

Este fork incluye un ejecutable generado con:

- Python **2.7** (32 bits).  
- `py2exe` 0.6.9 (build win32 para Python 2.7).  

El binario resultante es de 32 bits, pero funciona sin problemas tanto en:

- Windows 7 / 2008 de **32 bits**.  
- Windows 7 / 2008 y versiones posteriores de **64 bits** (vía WOW64).  

## Uso

1. Copiar el ejecutable `WinTriage_v1.exe` (y los archivos adicionales de la carpeta `dist`, si se distribuyen) a un directorio de trabajo, idealmente en un dispositivo externo (USB).  
2. En el host Windows a analizar, abrir sesión con un usuario con privilegios de **administrador local**.  
3. Ejecutar:

   - GUI/ejecución directa:  
     - Clic derecho sobre `WinTriage_v1.exe` → **Run as administrator**.  
   - CLI con fecha de corte para ficheros recientes:  
     ```cmd
     WinTriage_v1.exe -d 12/12/2015
     ```
     La fecha debe ir en el formato configurado en el sistema (dd/mm/yyyy o mm/dd/yyyy).

4. WinTriage creará un directorio de salida donde almacenará todos los resultados de la colección. Ese directorio puede copiarse después a un equipo de laboratorio para análisis en profundidad.

## Construcción del ejecutable (reproducible)

Si se desea regenerar el binario desde el código fuente:

1. Instalar **Python 2.7 x86** en `C:\Python27`.  
2. Instalar `py2exe` 0.6.9 para Python 2.7 (versión win32).  
3. Clonar este repositorio o descargarlo como ZIP y descomprimirlo.  
4. Desde un `cmd`:

   ```cmd
   cd C:\ruta\al\repositorio\wintriage-master
   python setup.py py2exe
   ```

5. El ejecutable y las DLL necesarias aparecerán en la carpeta `dist\`.  

## Compatibilidad

- **Python**: 2.7 (solo para el proceso de build, no requerido en el host donde se ejecuta el .exe).  
- **Sistemas operativos soportados** (ejecución del binario):  
  - Windows 7 / Windows Server 2008 y versiones posteriores.  
- **Arquitecturas**:  
  - Ejecutable de 32 bits, compatible con sistemas x86 y x64.

## Créditos y licencia

- Proyecto original: [WinTriage de Karol Pivo](https://github.com/karolpivo/wintriage).  
- Este repositorio mantiene el código original y añade instrucciones/artefactos de build para uso interno DFIR.  
- La licencia aplicada es la misma que la del proyecto original (ver `LICENSE` en este repositorio o en el upstream).