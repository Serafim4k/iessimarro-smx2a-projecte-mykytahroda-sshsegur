# Disseny i verificació d'un accés remot segur amb SSH en una xarxa de laboratori

Projecte intermodular de SMX per a planificar una configuració segura d'OpenSSH en un servidor Linux de laboratori. El repte és reduir el risc d'accessos no autoritzats mitjançant autenticació amb claus, restricció d'usuaris, tallafoc, registres i proves des d'un client. Aquesta pràctica arriba fins a la planificació: les incidències es mantenen obertes.

## Autor
- NOMALUMNE: `mykytahroda`
- Usuari GitHub: [@Serafim4k](https://github.com/Serafim4k)

## Rols simulats
- **Rol A — coordinació i documentació:** defineix l'abast, inventaria actius i riscos, i redacta el Document de Repte.
- **Rol B — sistema i servei SSH:** planifica la preparació de Linux, gestiona els usuaris i proposa la configuració d'OpenSSH.
- **Rol C — xarxa i verificació:** documenta la topologia, el tallafoc i les proves des del client.

El projecte es realitza individualment per `mykytahroda`, que simula els tres rols exigits per la pràctica.

## Objectiu i abast
Dissenyar i validar, en una xarxa virtual aïllada i sota autorització, una línia base de seguretat per a l'administració remota amb SSH. No es provarà cap sistema de tercers ni s'exposarà el servei a Internet.

## Contingut del repositori
- `documents/document-repte.md` — Document de Repte (Annex A).
- `documents/fitxes/` — tres fitxes d'activitat (Annex B), vinculades a incidències.
- `configuracio/` — espai per a la futura documentació tècnica i configuracions del laboratori.
- `favorits.md` — quatre eines i tecnologies preferides.

## Planificació
- **M1 — Planificació i inventari:** 11/01/2027–29/01/2027.
- **M2 — Configuració segura i validació:** 30/01/2027–12/02/2027.
- Les incidències romanen obertes fins que el projecte s'execute i es valide.

**Tauler de planificació:** [GitHub Projects](TAULER_URL_PENDENT)

## Entorn i límits de seguretat
Les proves estan limitades a màquines virtuals pròpies en una xarxa host-only o equivalent. Els canvis de configuració es faran només després de comprovar que existeix un mètode de recuperació d'accés, especialment abans de desactivar l'autenticació per contrasenya.
