# Projet de Compilateur - Lexer / Parser / AST

## Description

Ce projet implémente la première partie d'un compilateur avec trois composants principaux :
- **Lexer** (analyseur lexical)
- **Parser** (analyseur syntaxique)
- **AST** (Arbre de Syntaxe Abstraite)

L'objectif est de prendre un code source en entrée, dérivé du langage Python, et de le transformer en un AST.

Un rapport détaillé est disponible dans le fichier [Rapport_PCL.pdf](./docs/Rapport_PCL.pdf), ainsi que le sujet du projet, qui inclut la grammaire en page 4 : [Sujet.pdf](./docs/sujet-Projet-2024-25.pdf).

---

## Prérequis

Avant d'exécuter ce projet, assurez-vous d'avoir les outils suivants installés :

- **Java 8+**
- **Gradle** (optionnel)
- **JRE/JDK**
- **Graphviz** (pour la génération de graphes à partir des fichiers .dot)
  - Si vous n'avez pas **Graphviz** installé, vous pouvez le télécharger et l'installer à partir du site officiel : [Graphviz Download](https://graphviz.gitlab.io/download/).

---

## Installation

1. **Clonez le projet** :
   ```bash
   git clone https://github.com/Drucka1/PCL1.git
   ```
2. **Accédez au répertoire du projet** :
    ```bash
    cd PCL1
    ```
## Utilisation

### Avec JAR

Vous pouvez l'exécuter avec la commande suivante :

    java -jar app/build/libs/app.jar Lexer|Parser FilePath [option]
### Avec Gradle

Vous pouvez l'exécuter avec la commande suivante :

    gradle run --args="Lexer|Parser FilePath [option]"
#### Des fichiers de tests sont disponibles dans le repertoire *app/src/main/resources*

### Options disponibles

    --stack : Affiche la pile des tokens pendant l'analyse lexicale.
    --simplify : Simplifie l'Arbre de Syntaxe Abstraite (AST).


### Visualisation des fichiers .dot

Pour visualiser les fichiers .dot générés, vous pouvez utiliser l'extension Graphviz dans VSCode, ou exécuter la commande suivante pour générer une image PNG :

    dot -Tpng app/src/main/resources/output.dot -o output.png


---

# Compiler Project - Lexer / Parser / AST

## Description

This project implements the first part of a compiler with three main components:
- **Lexer** (lexical analyzer)
- **Parser** (syntax analyzer)
- **AST** (Abstract Syntax Tree)

The goal is to take a source code input, derived from the Python language, and transform it into an AST.

A detailed report is available in the file [Rapport_PCL.pdf](./docs/Rapport_PCL.pdf), as well as the project description, which includes the grammar on page 4  [Sujet.pdf](./docs/sujet-Projet-2024-25.pdf).

---

## Prerequisites

Before running this project, make sure you have the following tools installed:

- **Java 8+**
- **Gradle** (optional)
- **JRE/JDK**
- **Graphviz** (for generating graphs from .dot files)
  - If you don't have **Graphviz** installed, you can download and install it from the official site: [Graphviz Download](https://graphviz.gitlab.io/download/).

---

## Installation

1. **Clone the project**:
   ```bash
   git clone https://github.com/Drucka1/PCL1.git
1. **Navigate to the project directory**:
    ```bash
   cd PCL1
## Usage

### With JAR

You can execute the program with the following command using Java:

    java -jar app/build/libs/app.jar Lexer|Parser FilePath [option]

### With Gradle

Alternatively, you can run the program with the following command using Gradle:

    gradle run --args="Lexer|Parser FilePath [option]"

#### Test files are available in the *app/src/main/resources* directory.

### Available Options

    --stack: Displays the token stack during lexical analysis.
    --simplify: Simplifies the Abstract Syntax Tree (AST).

### Visualizing .dot Files

To visualize the generated .dot files, you can use the Graphviz extension in VSCode, or run the following command to generate a PNG image:

    dot -Tpng app/src/main/resources/output.dot -o output.png
