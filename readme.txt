Format d'import/export QCM DIRECT pour Moodle

Installation
Placer le dossier qcm direct sur votre serveur Moodle dans le sous dossier question/format
Bien vérifier que lors du dézippage de l'archive une couche de dossier qcmdirect ne s'est pas rajoutée.
Les fichiers format.php et version.php doivent se trouver dans question/format/qcmdirect et non dans
question/format/qcmdirect/qcmdirect

Usage
L'import et l'export se font comme tous les autres imports/exports de Moodle par les onglets Import et Export
de la banque de questions. 

Export (Moodle -> fichier texte)
Lors de l'Export seules sont prises en considération les questions à choix multiples, les autres sont ignorées.
Toute réponse dont la note est > 0 est considérée comme correcte puisque QCM DIRECT n'implémente pas la notion de
réponse partiellement correcte.
Chaque question peut comporter une ou plusieurs réponse correctes.
Les balises html et les entités sont converties en texte exploitable autant que possible.

Import (Fichier texte -> Moodle)
L'import est possible à la fois à partir de fichier texte générés par les Macros Word de la société Neoptec
(fichiers encodés en UTF-16LE avec CR+LF en fin de ligne) et à partir de fichiers texte générés par la fonction
"Export texte" du logiciel RealQuest version 1.0.0 de la société Neoptec (fichiers encodés en ISO-8859-1
avec CR+LF en fin de ligne).
Comme ces fichiers ne comporte pas de nom pour chaque question, le texte de la question (éventuellement tronqué)
est pris comme nom par défaut.
Les questions ne comportant pas de bonne réponses ou moins de 2 choix ne sont pas importées (limitation de Moodle).

Jean-Michel Védrine
IUT de St etienne Département GEA
vedrine@univ-st-etienne.fr
