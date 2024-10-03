# Progetto Angular - Santuccione Diego Con l'aiuto nella risoluzione dei problrmi da parte di
## Luca Renzetti & Ignacio E. Pezzana 
###  Progetto di Angular per la gestione di una tabella tramite crud

Questo progetto Angular include implementazioni avanzate progettate per migliorare la sicurezza, l'usabilità e l'efficienza dell'applicazione. Di seguito sono descritte le principali funzionalità implementate.

## 1. Autenticazione con Tentativi di Accesso Limitati

**Funzionalità**:
- L'accesso è limitato a **5 tentativi falliti**, dopo i quali l'utente deve attendere **1,67 minuti** prima di riprovare.
- Durante il periodo di attesa, le credenziali risultano non valide, impedendo ulteriori tentativi.
- Questo sistema protegge contro attacchi di forza bruta.

**Implementazione**:
- La logica è gestita in `login.component.ts` per controllare i tentativi falliti e il timer di attesa.

## 2. Protezione delle Tabelle dei Dati

**Funzionalità**:
- Le tabelle che gestiscono dati sensibili sono protette da tentativi di manipolazione non autorizzati.
- Prevenzione di **injection attacks** e modifiche non autorizzate.

**Implementazione**:
- Validazione rigorosa degli input e controlli di sicurezza a livello di client.

## 3. Validazione Stringente per la Gestione degli Utenti

**Funzionalità**:
- Durante l'aggiunta di nuove persone, tutti i campi obbligatori devono essere correttamente compilati.
- I dati accettati devono rispettare regole specifiche per campi come nome, età, email e codice fiscale.

**Implementazione**:
- Validazione lato componente che impedisce l'invio di dati incompleti o non conformi.

## 4. Opzione di Eliminazione Estesa

**Funzionalità**:
- Ogni utente, inclusi quelli esistenti, può essere eliminato. 
- Una conferma mostra il nome e cognome della persona prima di procedere.

**Implementazione**:
- Aggiunta dell'opzione di eliminazione per ogni utente nella tabella, con una richiesta di conferma.

## 5. Monitoraggio delle Vulnerabilità

**Funzionalità**:
- Il progetto è monitorato per rilevare vulnerabilità di sicurezza tramite il comando `npm audit`.
- Attualmente, non ci sono vulnerabilità conosciute.

**Implementazione**:
- Utilizzo di `npm audit` per mantenere le dipendenze aggiornate e sicure.

## 6. Integrazione con `json-server`

**Funzionalità**:
- Il progetto utilizza `json-server` per simulare un backend durante lo sviluppo.
- Le operazioni CRUD vengono gestite senza la necessità di un server reale.

**Implementazione**:
- Il file `db.json` agisce come un database temporaneo per testare le operazioni sui dati.

## 7. Gestione Sicura del Codice con GitHub

**Funzionalità**:
- Il progetto è ospitato in un repository privato su GitHub, garantendo controllo versione sicuro e riservato.

## Conclusioni

Queste funzionalità offrono un sistema solido, sicuro e user-friendly. La combinazione di controlli avanzati e usabilità garantisce un'esperienza sicura e piacevole per l'utente, proteggendo i dati da possibili attacchi e mantenendo una gestione efficiente delle operazioni.
