# A2 · Reforç de la configuració d'OpenSSH

**Incidència associada:** #6 · Endurir la configuració del servei SSH

## Nom de la tasca (Què?)
Preparar una proposta segura per a OpenSSH que limite l'accés a usuaris autoritzats, reduïsca els mètodes d'autenticació febles i mantinga un procediment de recuperació.

## Mòdul i RA (Per a què?)
- **Mòdul:** MP05 — Serveis (referència curricular oficial 0227: Serveis en xarxa).
- **RA associat:** RA6 — gestiona mètodes d'accés remot i instal·la els serveis corresponents.

## Modalitat (Com?)
Treball individual simulat en Rol B; la proposta serà revisada per Rol A abans de donar-la per vàlida.

## Producte entregable (Suport)
- `documents/fitxes/A2-reforc-ssh.md`.
- Llista de paràmetres proposats i justificació, sense claus privades ni credencials reals.

## Instruccions pas a pas
1. Revisar els paràmetres actuals d'OpenSSH en una màquina virtual de proves.
2. Proposar que `PermitRootLogin` siga `no` i restringir els comptes que poden entrar.
3. Proposar autenticació amb clau pública; només després de verificar-la, desactivar la contrasenya (`PasswordAuthentication no`).
4. Definir una regla de tallafoc limitada a la xarxa del laboratori i mantindre el servei fora d'Internet.
5. Documentar com comprovar la configuració i com recuperar l'accés si una prova falla.

## Recursos necessaris
- Màquina virtual Debian o Ubuntu, OpenSSH, terminal, manual `sshd_config` i xarxa virtual aïllada.

## Durada i setmana (Quan?)
4 hores · Setmana 4 (01/02/2027–05/02/2027).

## Lloc de realització (On?)
Laboratori d'informàtica amb màquines virtuals pròpies.

## Responsable (Qui?)
- Executa: Rol B.
- Revisa: Rol A (documentació i riscos) i Rol C (restriccions de xarxa).

## Instrument d'avaluació
Rúbrica de la fitxa A2:
- [ ] La proposta elimina l'inici de sessió directe de root (25%).
- [ ] L'autenticació per clau està prevista abans de desactivar contrasenyes (25%).
- [ ] El tallafoc limita l'accés a la xarxa autoritzada (25%).
- [ ] Inclou comprovacions i un mètode de recuperació (25%).
