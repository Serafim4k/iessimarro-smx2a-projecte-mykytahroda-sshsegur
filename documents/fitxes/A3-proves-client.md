# A3 · Proves de connectivitat i accés des del client

**Incidència associada:** #9 · Definir proves d'accés permès, denegat i connectivitat

## Nom de la tasca (Què?)
Definir una matriu de proves per comprovar que el client autoritzat pot connectar-se al servidor SSH i que els accessos no autoritzats es rebutgen de manera esperada.

## Mòdul i RA (Per a què?)
- **Mòdul:** MP02 — Xarxes (referència curricular oficial 0225: Xarxes locals).
- **RA associat:** RA1 — reconeix l'estructura d'una xarxa local i identifica els seus components i el mapa de xarxa.

## Modalitat (Com?)
Treball individual simulat en Rol C, coordinat amb Rol B per conéixer la configuració i amb Rol A per registrar els resultats.

## Producte entregable (Suport)
- `documents/fitxes/A3-proves-client.md`.
- Matriu de proves amb precondicions, acció, resultat esperat i evidència, a completar durant l'execució.

## Instruccions pas a pas
1. Registrar les IP del client i del servidor en la xarxa virtual aïllada.
2. Comprovar la connectivitat IP abans de provar SSH.
3. Definir una prova de connexió correcta amb el compte autoritzat.
4. Definir proves negatives per a un usuari no autoritzat i des d'una adreça fora de l'abast permés, sense atacar sistemes aliens.
5. Indicar quins registres consultar i guardar evidències sense mostrar dades secretes.

## Recursos necessaris
- Client i servidor virtuals, terminal, SSH client, documentació d'adreçament i registre de resultats.

## Durada i setmana (Quan?)
3 hores · Setmana 5 (08/02/2027–12/02/2027).

## Lloc de realització (On?)
Laboratori d'informàtica virtual o ordinador personal amb xarxa host-only.

## Responsable (Qui?)
- Executa: Rol C.
- Revisa: Rol B (servei) i Rol A (evidències i documentació).

## Instrument d'avaluació
Rúbrica de la fitxa A3:
- [ ] La topologia i les IP de prova estan documentades (25%).
- [ ] Es defineixen proves positives i negatives (25%).
- [ ] Els resultats esperats són verificables (25%).
- [ ] Les evidències no exposen credencials i queden vinculades a la incidència (25%).
