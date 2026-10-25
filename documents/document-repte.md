# Document de Repte — Disseny i verificació d'un accés remot segur amb SSH en una xarxa de laboratori

## Títol del projecte
Disseny i verificació d'un accés remot segur amb SSH en una xarxa de laboratori.

## Grup i membres
- **Alumne A — Rol A:** mykytahroda; coordinació, definició de l'abast, inventari de riscos i documentació.
- **Alumne B — Rol B:** mykytahroda (rol simulat); sistema Linux, usuaris, servei OpenSSH i proposta de configuració.
- **Alumne C — Rol C:** mykytahroda (rol simulat); topologia, tallafoc i comprovacions des del client.
- Projecte realitzat individualment per **mykytahroda**, que simula els tres rols de l'equip.

## Centre i curs
IES Lluís Simarro · 2n SMX A · Curs 2026–2027.

## Context i situació inicial
Un petit laboratori informàtic necessita administrar un servidor Linux des d'un equip client sense haver d'accedir físicament al servidor cada vegada. SSH permet l'administració remota xifrada, però una instal·lació amb usuaris excessius, inici de sessió de root, autenticació feble, regles de xarxa massa obertes o registres sense revisar pot augmentar el risc d'accés no autoritzat. Cal establir una configuració coherent, documentada i comprovable abans d'utilitzar-la.

El projecte s'adreça a un entorn de proves educatiu amb màquines virtuals pròpies. No s'analitzaran xarxes alienes, no es provarà cap sistema sense autorització i el servidor no s'exposarà a Internet.

## Repte proposat
Dissenyar i planificar una línia base de seguretat d'OpenSSH en un servidor Debian o Ubuntu de laboratori, definir quins usuaris i mètodes d'autenticació es permeten, restringir l'accés des de la xarxa de proves, establir comprovacions dels registres i preparar proves reproduïbles des d'un client. La pràctica actual acaba en la planificació; les incidències es mantenen obertes fins que el projecte s'execute i es valide.

## Objectiu general
Definir una proposta viable i documentada per a l'administració remota segura d'un servidor Linux mitjançant SSH en una xarxa de laboratori aïllada.

## Objectius específics
1. Identificar els equips, els usuaris, els serveis i els límits de la xarxa de proves.
2. Analitzar els riscos principals de l'accés remot i prioritzar mesures proporcionades.
3. Especificar una configuració d'OpenSSH que limite l'accés a usuaris autoritzats i preferisca claus públiques després de verificar-les.
4. Definir regles de tallafoc que permeten l'accés SSH només des de la xarxa del laboratori.
5. Preparar una matriu de proves per comprovar la connectivitat, l'autenticació, els accessos rebutjats i els registres, sense executar-la en sistemes de tercers.

## Mòduls professionals implicats
La guia de la pràctica utilitza etiquetes internes abreujades `mpXX`. Per evitar confondre-les amb els codis curriculars oficials, s'indica també el codi oficial del mòdul entre parèntesis.

- **MP02 — Xarxes (referència curricular oficial 0225: Xarxes locals).**
- **MP03 — Sistemes (referència curricular oficial 0224: Sistemes operatius en xarxa).**
- **MP05 — Serveis (referència curricular oficial 0227: Serveis en xarxa).**
- **MP06 — Seguretat informàtica (referència curricular oficial 0226: Seguretat informàtica).**

## RA associats per mòdul
- **MP02 / 0225 — RA1:** reconeix l'estructura d'una xarxa local, identifica els seus components i interpreta el mapa de xarxa; s'aplica a la topologia i a la connexió client-servidor del laboratori.
- **MP03 / 0224 — RA2:** gestiona usuaris i grups del sistema operatiu en xarxa; s'aplica a la selecció d'usuaris autoritzats i als permisos d'administració.
- **MP05 / 0227 — RA6:** gestiona mètodes d'accés remot i instal·la els serveis corresponents; s'aplica directament a OpenSSH i a les proves d'administració remota.
- **MP06 / 0226 — RA4:** assegura la privacitat de la informació transmesa en xarxes i inclou mesures com el control del servei i el tallafoc; s'aplica al reforç de SSH i a la restricció de connexions.

## Criteris de qualitat del repte
- **Proximitat/rellevància: Sí.** L'administració remota de sistemes és una necessitat real en laboratoris i petites empreses.
- **Treball en equip: Sí.** Les responsabilitats es divideixen en tres rols amb lliurables i revisions diferenciats, encara que la pràctica es simule individualment.
- **Creativitat: Sí.** Es defineix una matriu pròpia de riscos i proves per a un escenari de laboratori segur i reproduïble.
- **Connexió professional: Sí.** Inclou configuració de serveis, gestió de comptes, protecció de xarxa, diagnòstic i documentació tècnica.

## Requeriments tècnics
- **Hardware:** ordinador existent amb recursos suficients per a dues màquines virtuals; no es requereix comprar equips nous.
- **Programari:** VirtualBox o un altre hipervisor; una màquina virtual Debian/Ubuntu com a servidor; una màquina client Linux o Windows; OpenSSH server/client; tallafoc disponible en la distribució (per exemple, UFW o nftables); Git i GitHub per a documentació i traçabilitat. Wireshark és opcional per a observació de trànsit autoritzada.
- **Xarxa:** xarxa virtual aïllada tipus host-only o equivalent, amb adreçament documentat i sense publicar el port SSH a Internet.

## Limitacions o restriccions
- Durada prevista: cinc setmanes, del 11/01/2027 al 12/02/2027.
- Pressupost addicional: 0 €, aprofitant l'equip i el programari disponibles.
- Només es faran proves en màquines pròpies i amb autorització explícita.
- No es canviaran sistemes productius ni s'utilitzaran credencials reals.
- La desactivació de l'autenticació per contrasenya només es proposarà després d'haver verificat la connexió amb clau pública i disposar d'una via de recuperació.
- L'abast de la pràctica és la planificació: les incidències queden obertes i no es declara executada cap prova.

## Alternatives considerades
1. **Còpies de seguretat xifrades per a una petita empresa:** viable, però menys centrada en xarxes i accés remot.
2. **Xarxa Wi-Fi segmentada per a una associació:** rellevant, però depén més de l'accés a un encaminador i a equips físics.
3. **Accés remot segur amb SSH:** triat perquè es pot planificar i, més endavant, provar amb màquines virtuals pròpies, sense comprar equipament i amb una relació directa entre sistemes, xarxes, serveis i seguretat.

## Validació del professorat
A completar pel professor quan revise el Document de Repte.
