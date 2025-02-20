# Analyse Lexicale, Syntaxique et Sémantique d'Expressions Mathématiques

## Description du Projet
Ce projet implémente un analyseur lexical, syntaxique et sémantique permettant d'évaluer des expressions mathématiques composées de nombres, d'opérateurs arithmétiques et de parenthèses.

## Fonctionnalités
1. **Analyse Lexicale (Lexer)** : 
   - Identifie et extrait les différents composants d'une expression mathématique.
   - Gère les constantes numériques, les opérateurs `+`, `-`, `*`, `/` et les délimiteurs `(`, `)`.
   - Ignore les espaces blancs.

2. **Analyse Syntaxique (Parser)** : 
   - Vérifie la syntaxe de l'expression en appliquant des règles de grammaire.
   - Identifie les erreurs telles que des parenthèses mal appariées ou des opérateurs sans opérandes.

3. **Analyse Sémantique** :
   - Détecte des erreurs logiques, comme la division par zéro.
   - Assure la validité du résultat final.

## Structure du Code
- `MathLexer` : Classe responsable de l'analyse lexicale.
- `MathParser` : Classe gérant l'analyse syntaxique et l'évaluation des expressions.
- `MathSemanticAnalyzer` : Classe effectuant des vérifications sémantiques.
- `Evaluator` : Classe permettant l'évaluation finale de l'expression.

## Installation
Prérequis : Python 3.x

1. Clonez le dépôt :
   ```sh
   git clone https://github.com/votre-repo/analyse-math.git
   cd analyse-math
   ```

2. Installez les dépendances :
   ```sh
   pip install -r requirements.txt
   ```

3. Exécutez le script principal :
   ```sh
   python main.py
   ```

## Utilisation
1. Entrez une expression mathématique (ex: `3 + 5 * (2 - 1)`).
2. L'analyseur lexical génère une liste de tokens.
3. L'analyseur syntaxique valide et évalue l'expression.
4. L'analyse sémantique vérifie la cohérence logique du résultat.
5. L'évaluateur calcule le résultat final.

## Exemples
```python
lexer = MathLexer()
tokens = lexer.tokenize("3 + 5 * (2 - 1)")
parser = MathParser(tokens)
ast = parser.parse()
semantic_analyzer = MathSemanticAnalyzer(ast)
semantic_analyzer.analyze()
evaluator = Evaluator(ast)
final_result = evaluator.evaluate()
print(final_result)  # Affiche le résultat de l'expression
```



