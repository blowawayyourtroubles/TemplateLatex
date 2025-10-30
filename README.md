# 📐 Template LaTeX para Documentos Matemáticos

[![LaTeX](https://img.shields.io/badge/LaTeX-Template-008080?style=for-the-badge&logo=latex)](https://www.latex-project.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg?style=for-the-badge)](https://github.com/tu-usuario/tu-repo/graphs/commit-activity)

> Template profesional con estilo institucional moderno para crear documentos matemáticos de alta calidad en LaTeX.

## ✨ Características

- 🎨 **Tema oscuro profesional** con paleta de colores institucional
- 📦 **6 tipos de cajas personalizadas** (definición, teorema, ejemplo, nota, advertencia, ejercicio)
- 🔢 **Comandos matemáticos avanzados** para derivadas, integrales, conjuntos numéricos
- 📊 **Soporte completo para gráficas** con TikZ/PGFplots
- 📑 **Encabezados y pies de página** personalizados
- 🔗 **Enlaces clickeables** en el PDF (hyperref)
- 📝 **Tabla de contenidos** automática
- 🎓 **Entornos matemáticos** personalizados (teoremas, lemas, proposiciones)

## 📸 Vista Previa

![Preview](Template.jpg)

## 📋 Requisitos

### Sistema Operativo
- ✅ Windows 10/11
- ✅ macOS
- ✅ Linux

### Distribución LaTeX
Necesitas una de estas distribuciones instaladas:

- **Windows**: [MiKTeX](https://miktex.org/download) (recomendado) o [TeX Live](https://www.tug.org/texlive/)
- **macOS**: [MacTeX](https://www.tug.org/mactex/)
- **Linux**: TeX Live (disponible en repositorios)

```bash
# Ubuntu/Debian
sudo apt-get install texlive-full

# Fedora
sudo dnf install texlive-scheme-full

# Arch Linux
sudo pacman -S texlive-most
```

### Editor LaTeX (Opcional pero recomendado)
- [VSCode](https://code.visualstudio.com/) + [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
- [TeXworks](https://www.tug.org/texworks/) (incluido con MiKTeX)
- [TeXstudio](https://www.texstudio.org/)
- [Overleaf](https://www.overleaf.com/) (online, no requiere instalación)

## 📦 Paquetes LaTeX Necesarios

El template requiere los siguientes paquetes LaTeX:

### Paquetes Esenciales
```latex
babel                 % Idioma español
amsmath              % Matemáticas básicas
amssymb              % Símbolos matemáticos
amsthm               % Teoremas
mathtools            % Herramientas matemáticas avanzadas
xcolor               % Colores
geometry             % Márgenes de página
graphicx             % Imágenes
booktabs             % Tablas profesionales
array                % Tablas avanzadas
tabularx             % Tablas con ancho ajustable
multicol             % Múltiples columnas
enumitem             % Listas personalizadas
fancyhdr             % Encabezados y pies de página
titlesec             % Formato de títulos
```

### Paquetes Críticos (Gráficos y Cajas)
```latex
tcolorbox            % Cajas de color ⭐ IMPORTANTE
tikz                 % Gráficos vectoriales ⭐ IMPORTANTE
pgfplots             % Gráficas matemáticas ⭐ IMPORTANTE
```

### Paquetes Adicionales
```latex
lm                   % Fuentes Latin Modern
hyperref             % Enlaces clickeables en PDF
```

## ⚙️ Configuración de Paquetes

### En MiKTeX (Windows)

**Instalación automática** (recomendado):
1. Abre **MiKTeX Console**
2. Ve a **Settings** → **General**
3. En **"Install missing packages on-the-fly"** selecciona: `Always`
4. Los paquetes se instalarán automáticamente al compilar

**Instalación manual**:
1. Abre **MiKTeX Console**
2. Ve a **Packages**
3. Busca cada paquete de la lista
4. Clic derecho → **Install**

### En TeX Live (Linux/macOS)

La mayoría de los paquetes vienen con `texlive-full`. Si falta alguno:

```bash
# Ubuntu/Debian
sudo apt-get install texlive-latex-extra texlive-science

# Para pgfplots y tikz
sudo apt-get install texlive-pictures
```

### En Overleaf

✅ **No requiere instalación** - Overleaf tiene todos los paquetes preinstalados.

## 📝 Uso Básico

### 1. Personaliza la información del documento

Edita las líneas 224-237 del archivo `.tex`:

```latex
\title{
	\textcolor{accent}{\Huge\textbf{Tu Título Aquí}}\\
	\vspace{5pt}
	\textcolor{highlight}{\Large Tu Subtítulo}
}
\author{
	\textcolor{white}{\Large Tu Nombre}\\
	\textcolor{accent}{Tu Institución}\\
	\textcolor{highlight}{\texttt{tu-correo@institucion.edu}}
}
```

### 2. Usa las cajas personalizadas

```latex
% Definición
\begin{definicion}{Límite}
Contenido de la definición...
\end{definicion}

% Teorema
\begin{teorema}{Teorema Fundamental del Cálculo}
Contenido del teorema...
\end{teorema}

% Ejemplo
\begin{ejemplo}{Derivada de una función}
Paso a paso del ejemplo...
\end{ejemplo}

% Nota
\begin{nota}{Observación importante}
Contenido de la nota...
\end{nota}

% Advertencia
\begin{advertencia}{Error común}
Advertencia sobre errores frecuentes...
\end{advertencia}

% Ejercicio
\begin{ejercicio}{Para practicar}
Enunciado del ejercicio...
\end{ejercicio}
```

### 3. Comandos matemáticos personalizados

```latex
% Conjuntos numéricos
\N   % Naturales
\Z   % Enteros
\Q   % Racionales
\R   % Reales
\C   % Complejos

% Derivadas
\dv{y}{x}           % dy/dx
\dvn{y}{x}{3}       % d³y/dx³
\pdv{f}{x}          % ∂f/∂x

% Integrales
\inte{a}{b}         % Integral de a a b
\intinf             % Integral de -∞ a ∞

% Otros
\abs{x}             % Valor absoluto
\norm{v}            % Norma
\vect{v}            % Vector en negrita
```

### 4. Separadores visuales

```latex
\separator          % Línea separadora gruesa
\thinline          % Línea separadora delgada
```

### 5. Destacar texto

```latex
\highlight{texto}   % Texto en azul (resaltado)
\important{texto}   % Texto en naranja (importante)
\critical{texto}    % Texto en rojo (crítico)
```

### 6. Fórmula destacada

```latex
\mainformula{E = mc^2}
```

## 🔨 Compilación

### Con VSCode + LaTeX Workshop

1. Abre el archivo `.tex` en VSCode
2. Guarda el archivo (`Ctrl+S`) - compila automáticamente
3. O presiona `Ctrl+Alt+B` para compilar manualmente
4. El PDF se abrirá automáticamente

### Con TeXworks

1. Abre el archivo `.tex`
2. Selecciona **pdfLaTeX** en el menú desplegable
3. Presiona el botón verde de compilar (o `Ctrl+T`)

### Línea de comandos

```bash
pdflatex nombre-archivo.tex
pdflatex nombre-archivo.tex  # Compilar dos veces para referencias
```

## 🎨 Personalización de Colores

Puedes cambiar la paleta de colores editando las líneas 37-46:

```latex
\definecolor{primary}{HTML}{0077b6}      % Azul institucional
\definecolor{secondary}{HTML}{023e8a}    % Azul oscuro
\definecolor{accent}{HTML}{48cae4}       % Azul claro/cyan
\definecolor{highlight}{HTML}{90e0ef}    % Azul muy claro
\definecolor{success}{HTML}{06a77d}      % Verde
\definecolor{warning}{HTML}{f77f00}      % Naranja
\definecolor{danger}{HTML}{d62828}       % Rojo
\definecolor{dark}{HTML}{293133}         % Gris oscuro (fondo)
```

### Paletas alternativas sugeridas:

**Paleta Verde:**
```latex
\definecolor{primary}{HTML}{2d6a4f}
\definecolor{accent}{HTML}{52b788}
\definecolor{highlight}{HTML}{95d5b2}
```

**Paleta Púrpura:**
```latex
\definecolor{primary}{HTML}{5a189a}
\definecolor{accent}{HTML}{9d4edd}
\definecolor{highlight}{HTML}{c77dff}
```

**Paleta Roja:**
```latex
\definecolor{primary}{HTML}{9d0208}
\definecolor{accent}{HTML}{dc2f02}
\definecolor{highlight}{HTML}{f48c06}
```

## 📚 Estructura de Archivos

```
latex-math-template/
│
├── template.tex              # Template principal
├── README.md                 # Este archivo
├── preview.png              # Vista previa del documento
├── LICENSE                   # Licencia MIT
│
└── examples/                 # (Opcional) Ejemplos de uso
    ├── derivadas.tex
    ├── integrales.tex
    └── algebra-lineal.tex
```

## 🐛 Solución de Problemas

### Error: "File X.sty not found"
**Solución**: Instala el paquete `X` usando MiKTeX Console o tu gestor de paquetes.

### Error con tcolorbox
**Solución**: Instala también los paquetes: `pgf`, `etoolbox`, `environ`, `xparse`

### Error: "Undefined control sequence"
**Solución**: Asegúrate de que todos los paquetes estén instalados y compilar dos veces.

### Las gráficas no aparecen
**Solución**: Verifica que `pgfplots` versión 1.18+ esté instalado. Usa `\pgfplotsset{compat=1.18}`

### Caracteres especiales no se muestran
**Solución**: Asegúrate de guardar el archivo con codificación UTF-8.

**: Octubre 2025
