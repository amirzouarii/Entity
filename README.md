🔶 Entités et attributs
🏢 Gymnase
ID_Gymnase (Identifiant unique)

Nom

Adresse

Téléphone

👤 Membre
ID_Membre (Identifiant unique)

Nom

Prénom

Adresse

Date de naissance

Sexe

Gymnase_FK (appartenance à un gymnase)

🧑‍🏫 Coach
ID_Coach (Identifiant unique)

Nom

Prénom

Âge

Spécialité

🕐 Session
ID_Session (Identifiant unique)

Type de sport

Horaire

Nombre max : 20 membres

🔷 Relations
📌 "Inscription"
Entre Membre et Session

Cardinalité : Un membre peut s'inscrire à plusieurs sessions, une session peut avoir jusqu'à 20 membres

Attributs : Date d’inscription (optionnel)

📌 "Anime"
Entre Coach et Session

Cardinalité : Une session peut être encadrée par jusqu’à 2 coaches, un coach peut animer plusieurs sessions

✅ Diagramme (Représentation textuelle simplifiée)
scss
Copier
Modifier
Gymnase (ID_Gymnase, Nom, Adresse, Téléphone)
    ⬑ 1 - N
Membre (ID_Membre, Nom, Prénom, Adresse, DateNaissance, Sexe, Gymnase_FK)
    ⬌ N - N (max 20) via Inscription
Session (ID_Session, TypeSport, Horaire)
    ⬌ N - N (max 2) via Anime
Coach (ID_Coach, Nom, Prénom, Âge, Spécialité)
