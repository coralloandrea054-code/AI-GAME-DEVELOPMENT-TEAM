Progetto gioco incrementale «L'Ammasso» - Resoconto della sessione
Resoconto della sessione di lavoro tra l'utente e Claude (Anthropic) sul videogioco incrementale ambientato nel periodo fascista italiano. Data della sessione: 15 novembre 2026. Lingua di lavoro: italiano. In fondo al documento trovi tutto il codice usato.
Legenda degli stati
• CONFERMATO: l'utente ha detto che funziona o ha eseguito il passo.
• FORNITO: Claude ha dato codice o istruzioni, senza un esito riportato dall'utente.
• PROPOSTO: è solo un'idea o un piano, non ancora realizzato.
1. OBIETTIVO
L'utente vuole creare un videogioco incrementale a tema storico-satirico, ispirato a «Potato Please» (si sbucciano patate nell'epoca comunista), ma ambientato nel periodo fascista italiano. Requisiti emersi:
• Sviluppo gratuito, con strumenti gratuiti.
• L'utente è alle prime armi e vuole essere guidato passo passo, con indicazioni precise su cosa cliccare.
• Il gioco deve essere in prima persona: non un incrementale fatto di soli numeri e non a vista dall'alto.
• Pubblicazione futura su Steam, con alternative gratuite (sito proprio, itch.io, GitHub Pages) se Steam costa troppo.
• Stile grafico scelto: illustrato, stile manifesto anni '30.
• Tono scelto: satira comica (burocrazia assurda).
• Peso del gioco: equilibrio tra lavoro a mano, gestione/automazione e trucco del grano dichiarato.
• Ultima richiesta: il gioco deve procedere a un ritmo più lento a livello di sviluppo.
Giochi di riferimento citati dall'utente: Potato Please, Leaf It Alone, Moon Sweepers, Unharvest, One Million Coins.
2. LAVORO SVOLTO
2.1 Stima dei tempi (completato)
Stima generale: prototipo giocabile in poche ore; gioco piccolo e curato in 1-3 settimane part-time; gioco completo in 1-3 mesi. Percorso gratuito: HTML, CSS e JavaScript, con hosting su GitHub Pages, Netlify o itch.io.
2.2 Primo prototipo «La Battaglia del Grano» (completato e pubblicato)
Incrementale classico a numeri, in un solo file, ambientato 1925-1943. Pubblicato come artifact: https://claude.ai/artifact/HbSEJkhUHFPw7GsD2wfnj4. Il sorgente /mnt/user-data/outputs/battaglia-del-grano.html esiste solo nell'ambiente di Claude, non sul computer dell'utente.
• Pulsante di click per raccogliere grano.
• 6 generatori: Bracciante, Trattore Fordson, Bonifica Pontina, Altoparlanti in piazza, Cinegiornale LUCE, Gerarca provinciale (costo crescente ×1.15).
• 5 miglioramenti: falce, discorso dal balcone, tessera del partito, sabato fascista, statistiche ritoccate.
• Frasi satiriche a rotazione, salvataggio con localStorage (chiave bdg_save_v1), progressi offline fino a 8 ore.
• Evento finale a 10 milioni di quintali: schermata sul 25 luglio 1943.
Questa direzione è stata poi scartata dall'utente, che voleva un gioco in cui ci si muove.
2.3 Concept «Mussolinia: la Battaglia del Grano» (proposto, poi superato)
Contadino nelle paludi di Terralba/Mussolinia (oggi Arborea, Sardegna) dal 1928 al 1943, con grano dichiarato contro grano reale, un indice di sospetto, tre epoche (1928-35, 1935-39, 1940-43). Il nome è stato poi sostituito da «L'Ammasso». I dettagli storici non sono stati verificati con fonti.
2.4 Connettori e Steam (completato)
• Ricerca nel registro dei connettori per GitHub/git/repository/code: nessun connettore rilevante. Claude non può accedere né al computer dell'utente né a GitHub e lavora scrivendo codice che l'utente copia a mano. Claude Code (app desktop) è stato citato solo come strada futura (proposto).
• Ricerca web su Steam: quota di 100 dollari per ogni nuova app, recuperabile dopo 1.000 dollari di ricavi lordi rettificati; Valve trattiene il 30% sulle prime vendite fino a 10 milioni. Un gioco web si impacchetta con Electron e si carica con Steamworks (SDK, SteamPipe). Le cifre possono cambiare: da ricontrollare alla pubblicazione.
2.5 Ricerca sui giochi di riferimento (completato)
Esito da fonti di stampa e store, non verificato di persona:
• Potato Please: simulazione in prima persona, si parte da coltello e secchio e si passa all'automazione.
• Leaf it Alone: simulazione «cozy» di pulizia di un cortile pieno di foglie.
• Moon Sweepers: pulizia cooperativa della Luna, si parte con uno spazzolino e poi si automatizza; team di due persone.
• Unharvest: informazioni scarse e incerte (sembra un idle con piaghe che si diffondono su un campo di grano).
• One Million Coins: incrementale minerario in prima persona, circa 2 ore, albero abilità con oltre 250 nodi.
Formula comune individuata: prima persona, lavoro fisico, compito ridicolmente grande, scatto di scala dal manuale all'automatico, idea unica, durata breve.
2.6 Ambiente sul computer dell'utente, Windows (confermato)
• Node.js installato: v26.13.1.
• Git installato: git init ha risposto Initialized empty Git repository in C:/Users/Utente/Documents/mussolinia/.git/. Il risultato di git --version non è stato riportato.
• VS Code aperto sulla cartella mussolinia.
• Live Server (autore Ritwick Dey) installato.
• Primo index.html di prova: l'utente ha scritto «vedo la pagina».
2.7 Scheletro multi-file (fornito, problema, abbandonato)
Struttura index.html, css/style.css, js/data.js, js/game.js, js/ui.js, js/main.js (incrementale a numeri con moduli ES). L'utente ha riferito che cliccando il pulsante non succedeva nulla e che non voleva comunque quel tipo di gioco. Causa non diagnosticata con certezza (ipotesi non confermata: pagina aperta senza Live Server, dove i moduli ES non funzionano).
2.8 Prototipo 2D dall'alto con Phaser (confermato funzionante, poi scartato)
Un solo file che ha sostituito il contenuto di index.html, con Phaser 3.80.1 da cdn.jsdelivr.net: contadino con WASD/click, 6 campi da seminare e raccogliere, Ammasso e Consorzio, braccianti automatici. L'utente ha chiesto come usare «Open with Live Server», poi ha detto che andava, ma ha chiarito di volere la prima persona.
2.9 Concept «L'Ammasso» in prima persona (confermato: «si mi piace»)
Sei un contadino sull'aia di un podere nel 1928. Il regime impone di consegnare il grano all'ammasso. All'inizio batti il grano a mano con il correggiato (flagello), riempi i sacchi e li porti alla pesa; poi compri attrezzi, braccianti, trebbiatrice e camion. Alla pesa decidi quanto dichiarare, anche più del vero. Finale al 25 luglio 1943 con statistiche vere contro dichiarate (non ancora implementato).
2.10 Prototipo in prima persona ammasso.html con Three.js (confermato)
Creato come nuovo file ammasso.html (il vecchio index.html lasciato come copia di sicurezza). Libreria: Three.js r128 da https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js. Versione 1: aia, covoni, correggiato, sacco, pesa, Consorzio con 3 acquisti, braccianti. Valutazione dell'utente: «per essere un prototipo va bene».
2.11 Fix del blocco puntatore (confermato risolto)
Vedi sezione 5.
2.12 Meccanica del grano dichiarato (confermato funzionante)
ammasso.html riscritto per intero con quota giornaliera, dichiarazione alla pesa, indice di sospetto, ispettore, fine giornata. L'utente ha poi chiesto di migliorare la grafica e ha detto che il giorno a 120 secondi andava bene per il prototipo.
2.13 Blocco grafico intermedio (fornito, superato)
Blocco da sostituire tra // Scena e // Messaggi: cielo sfumato, ombre, texture, campi di grano con InstancedMesh, cipressi, colline, casale, persone con braccia e gambe, covoni più dettagliati. Superato dalla versione completa v3.
2.14 Domande di design e versione completa v3 (fornita, parzialmente confermata)
Claude ha posto 3 domande a scelta. Risposte dell'utente:
• Stile grafico: Illustrato stile manifesto anni '30.
• Tono: Satira comica (burocrazia assurda).
• Peso: Un equilibrio di tutto.
Claude ha poi fornito l'intero ammasso.html v3 (sezione 3). Commento dell'utente: la grafica va ok ma andrà rivista, e il gioco va troppo veloce.
2.15 Analisi del ritmo e piano di sviluppo (proposto)
Ultimo intervento di Claude: analisi delle cause della velocità eccessiva, piano per fasi A-G e cinque ritocchi provvisori (sezioni 3 e 7). L'utente non ha ancora risposto né confermato di averli applicati.
3. MODIFICHE
3.1 Struttura delle cartelle sul computer dell'utente
Percorso: C:\Users\Utente\Documents\mussolinia. Stato basato sulle istruzioni date, non verificato direttamente (Claude non ha accesso ai file).
mussolinia/
├── .git/               repository locale vuoto (confermato)
├── index.html          prova -> scheletro -> Phaser 2D (non più usato)
├── css/
│   └── style.css       dello scheletro multi-file (non usato)
├── js/
│   ├── data.js         dello scheletro (non usato)
│   ├── game.js         dello scheletro (non usato)
│   ├── ui.js           dello scheletro (non usato)
│   └── main.js         dello scheletro (non usato)
└── ammasso.html        FILE DI LAVORO ATTUALE (Three.js, prima persona)
Le cartelle css/ e js/ e i loro file sono probabilmente creati ma non confermati. Claude ha detto di ignorarli.
3.2 Evoluzione di ammasso.html
1.  v1: WASD, mouse-look con pointer lock, correggiato animato, 7 covoni, aia, Pesa (destra, x=13) e Consorzio (sinistra, x=-13), 3 acquisti (correggiato, sacco, bracciante), lire come unica valuta.
2.  v1.1: fix del blocco puntatore e frecce per guardarsi attorno.
3.  v2 (dichiarazione alla pesa): giorno (DAY=120), quota, sospetto, ispettore, fine giornata.
4.  v3 (versione completa attuale): grafica manifesto, circolari, nascondiglio, registro.
3.3 Contenuto tecnico della v3
• Stack: file singolo HTML con <script> inline, Three.js r128 da cdnjs, nessun salvataggio.
• Rendering: MeshToonMaterial con gradientMap a 3 toni; contorni neri con la tecnica «inverted hull» (funzione ink); nebbia; cielo a fasce su sfera con sole rosso; overlay CSS con vignettatura e grana della carta (SVG feTurbulence); font di sistema Impact/Arial Narrow; interfaccia in crema #f1e3bd, rosso #b3261e, nero #1a1209.
• Mondo: aia circolare (raggio 14), 4 campi di grano con InstancedMesh, cipressi, colline, casale col tetto, 4 cartelloni satirici, Pesa e Consorzio con etichette sprite, 7 covoni (hp 5, ricrescita 6 s).
• Stato (S): lire, sacco, cap(10), danno(1), brac, nasc, c{danno:20, cap:30, brac:60, nasc:80}, giorno, t, dichG, sosp, gap, totD, totR, ispT, circT, quotaX, marcia.
• Comandi: WASD, mouse (o frecce), clic sinistro per battere, E/R/T alla pesa (fattori 1, 1.3, 1.8), 1-4 al Consorzio, Tab per il registro.
• Formule: quota = round((20 + giorno*15) * quotaX); il sospetto sale di falsi*1.5/(1+0.3*nasc) e scende di 0.25/s; ispezione ogni 25-50 s con probabilità di scoperta sosp/100; multa = 40% delle lire + gap*2; a fine giorno premio 20*giorno se la quota è raggiunta, altrimenti multa del 30% delle lire; sacco pieno rallenta del 40%; aumenti di prezzo per acquisto: correggiato ×1.8, sacco ×1.7, bracciante ×1.35, nascondiglio ×1.9; ogni colpo dà min(2*danno, spazio nel sacco).
• Circolari satiriche (6, ogni 35-65 s, la prima a 25 s): marcia dei braccianti, visita del podestà (quota +20% e +15 lire), triplice copia (sospetto -15), nessun dubbio (sospetto +20), sacco dichiarato pieno, pioggia «dichiarata sereno» (+30 s).
• Effetti: particelle di chicchi, leggero dondolio camminando.
3.3b Cinque ritocchi provvisori proposti per rallentare (non applicati)
1.  const DAY=120; diventa const DAY=300;
2.  Nella quota, (20+S.giorno*15) diventa (120+S.giorno*60).
3.  const gu=Math.min(2*S.danno,S.cap-S.sacco) diventa const gu=Math.min(S.danno,S.cap-S.sacco).
4.  c:{danno:20,cap:30,brac:60,nasc:80} diventa c:{danno:200,cap:300,brac:900,nasc:1200}.
5.  La riga const pr=S.brac... diventa const pr=S.brac*.15*(S.marcia>0?2:1)*dt;S.lire+=pr;S.dichG+=pr;S.totD+=pr;S.totR+=pr;if(S.marcia>0)S.marcia-=dt}. Inoltre i moltiplicatori di prezzo S.c.danno*=1.8, S.c.cap*=1.7, S.c.brac*=1.35 diventano 2.5, 2.2, 1.3.
3.4 File nell'ambiente di Claude
Solo /mnt/user-data/outputs/battaglia-del-grano.html (primo prototipo, pubblicato come artifact). Tutto il codice successivo è stato dato solo in chat: la copia sul computer dell'utente è l'unica versione reale.
4. DECISIONI
Decisione
Motivazione
Passare da incrementale a numeri a gioco in prima persona
Richiesta esplicita dell'utente, in linea con i giochi di riferimento.
Usare Three.js (web) e non un motore come Godot
Si continua con VS Code e Live Server, Claude scrive il codice direttamente, è gratuito, pubblicabile sul web e impacchettabile con Electron per Steam.
Niente fisica realistica, grafica a forme semplici
Il 3D con modelli complessi e fisica è molto più difficile; fattibilità per principianti.
Tenere index.html come copia di sicurezza e lavorare su ammasso.html
Evitare di rompere versioni funzionanti.
Dare sempre il file completo quando le modifiche sono molte
L'utente è principiante e sbaglia con i copia-incolla a pezzi.
Meccanica centrale: grano dichiarato contro grano reale con sospetto e ispezioni
È l'elemento distintivo rispetto agli altri incrementali.
Tono satirico, non celebrativo
Scelta dell'utente; si ride della propaganda e non si esalta il regime.
Giorno a 120 s per il prototipo
L'utente ha detto che va bene per ora; da allungare dopo.
Pubblicare prima su GitHub Pages o itch.io, Steam solo se il gioco funziona
Steam costa 100 dollari a gioco.
Durata obiettivo 2-3 ore (3 epoche da circa 40 minuti)
Modello: One Million Coins. Non ancora confermata dall'utente.
5. PROBLEMI
Problema
Esito
Scheletro multi-file: cliccando non succede nulla
Non diagnosticato con certezza; strada abbandonata. Ipotesi non verificata: file aperto senza Live Server.
Errore in Console: WrongDocumentError: The root document of this element is not valid for pointer lock
Risolto: il blocco del puntatore ora è richiesto su document.documentElement con gestione dell'errore; se il browser lo rifiuta il gioco parte lo stesso e si guarda con le frecce. Dopo il fix la Console non mostrava errori.
Avvisi Tracking Prevention blocked access to storage (Edge) per cdnjs
Innocui: la libreria si carica comunque.
favicon.ico 404
Innocuo: manca l'icona della scheda.
Utente alle prime armi su terminale, Live Server, Console (F12)
Risolto con istruzioni dettagliate; suggeriti screenshot e copia della riga rossa della Console.
Gioco troppo veloce (acquisti subito, costi bassi, tutto sbloccato dall'inizio)
IRRISOLTO: piano e ritocchi provvisori proposti, non confermati.
Grafica da rivedere (giudizio dell'utente)
IRRISOLTO: pianificato come Fase F.
Possibile incongruenza nella produzione dei braccianti nella v3 (lettura del codice, non testata): S.brac*.5*(S.marcia>0?2:0.5*2/2) dà 0.25 kg/s per bracciante normalmente e 1.0 durante la «marcia», cioè ×4 e non ×2
Irrisolto, da verificare.
Anno mostrato incoerente: «Anno IV E.F.» nel primo prototipo, «Anno VI E.F.» nei successivi
Irrisolto, da uniformare.
Il blocco grafico intermedio e la v3 non sono stati testati da Claude
Il feedback dell'utente («va ok la grafica») suggerisce che la v3 gira, ma non sono stati riportati dettagli su prestazioni o difetti visivi.
6. STATO ATTUALE
• Funziona (secondo l'utente): ammasso.html in prima persona, con grafica stile manifesto, quota, dichiarazione alla pesa, sospetto, ispettore, circolari, registro, nascondiglio.
• Si gioca solo su computer con tastiera e mouse; serve la connessione internet (Three.js da CDN); nessun salvataggio (F5 azzera tutto); nessun suono; nessun supporto touch.
• Ritmo: troppo veloce (giudizio dell'utente). Non ancora corretto.
• Git: repository locale inizializzato. Claude ha dato i comandi per git config e un primo commit (git add . e git commit -m "Prototipo 1: aia in prima persona"), ma l'utente non ha confermato di averli eseguiti. Nessun account GitHub confermato, nessun remoto.
• Pubblicazione: nulla di pubblicato oltre al primo prototipo come artifact di Claude.
• Contenuti storici: solo spunti satirici; nessuna epoca implementata, nessuna scheda «Lo sapevi?», nessun finale del 25 luglio 1943 in ammasso.html.
7. PROSSIMI PASSI
Subito, in attesa dell'utente:
1.  Chiedere se la durata totale di 2-3 ore è giusta.
2.  Applicare il rallentamento, con i cinque ritocchi della sezione 3.3b o con la Fase A.
Piano per fasi (proposto):
• Fase A: bilanciamento con tutti i numeri in un blocco di configurazione in cima al file, giorno a 300 s, seconda valuta Favore del Partito (guadagnata barando senza essere scoperti, spesa per permessi).
• Fase B: sblocchi per giorno (per esempio trebbiatrice dal giorno 6, camion dal 12) e primi 5 minuti solo a mano.
• Fase C: salvataggio con localStorage e progressi offline.
• Fase D: tre epoche (giorni 1-8 Battaglia del Grano; 9-16 Autarchia e Impero; 17-24 Guerra con braccianti richiamati e requisizioni), con quota che dal giorno 4 supera la produzione onesta.
• Fase E: altri eventi satirici, schede «Lo sapevi?», finale del 25 luglio 1943 con statistiche vere contro dichiarate.
• Fase F: grafica e suono (manifesti, icone, eventualmente Krita).
• Fase G: test con altri giocatori, pubblicazione su GitHub Pages o itch.io, poi valutazione di Steam con Electron e Steamworks (verificare la quota di 100 dollari e le regole sui simboli storici).
Da fare lato utente: salvare il commit Git, creare un account GitHub quando serve, installare Krita solo più avanti.
8. NOTE PER CHATGPT
Profilo dell'utente
• Scrive in italiano informale; vive a Oristano (Sardegna); usa Windows (nome utente Utente); è alle prime armi: serve guidarlo passo passo con indicazioni precise su cosa cliccare (per esempio «tasto destro dentro il file, Open with Live Server»).
• Preferisce che gli si facciano domande prima di costruire le parti importanti e che gli si dia il codice completo del file invece di modifiche a pezzi.
• Quando qualcosa non funziona, conviene chiedergli la riga rossa della Console del browser (F12) o uno screenshot.
Ambiente tecnico
• Cartella progetto: C:\Users\Utente\Documents\mussolinia. Editor VS Code con estensione Live Server (indirizzo tipico 127.0.0.1:5500). Node.js v26.13.1, Git installato.
• File di lavoro: ammasso.html (singolo file, Three.js r128 da cdnjs). index.html e le cartelle css/ e js/ sono residui di prototipi precedenti, non usati.
• Claude non aveva accesso ai file dell'utente né a GitHub. La versione reale di ammasso.html è sul PC dell'utente: prima di modificarlo conviene chiedergli di incollare il file attuale, perché potrebbe differire da quanto descritto qui.
Direzione del progetto (decisa)
• Prima persona, 3D semplice, stile manifesto anni '30, tono di satira comica sulla burocrazia, equilibrio tra lavoro manuale, automazione e trucco della pesa. Nessun uso celebrativo del regime.
Cose da non dare per scontate
• I dettagli storici (Mussolinia/Arborea, date di Battaglia del Grano e ammassi, anno E.F.) non sono stati verificati con fonti.
• Le informazioni sui giochi di riferimento e sui costi di Steam vengono da ricerche web della sessione e vanno riverificate.
• Il commit Git e l'account GitHub non sono confermati.
Priorità immediata
1.  Rallentare il ritmo (richiesta esplicita dell'utente) e creare un blocco di configurazione unico per i numeri.
2.  Attendere la risposta dell'utente sulla durata totale desiderata.
3.  Poi procedere con le fasi B-G, ricordando che la grafica va rivista e che il salvataggio non è ancora implementato.
9. CODICE USATO
Le sezioni seguenti riportano il codice fornito nella sessione. Le versioni v1, v1.1, v2 e il blocco grafico intermedio di ammasso.html sono interamente superati dalla v3, che ne contiene tutte le funzioni, e quindi non sono riportati separatamente. Il fix del blocco puntatore è già integrato nella v3.
9.1 ammasso.html (v3, versione attuale, file di lavoro)
Cartella: C:\Users\Utente\Documents\mussolinia. Si apre con Live Server (tasto destro, Open with Live Server). Il giorno dura DAY=120 secondi.
<!DOCTYPE html>
<html lang="it"><head><meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1"><title>L’Ammasso</title>
<style>
:root{--c:#f1e3bd;--r:#b3261e;--k:#1a1209}
body{margin:0;overflow:hidden;background:#000;font-family:Impact,"Arial Narrow",Oswald,sans-serif;text-transform:uppercase;letter-spacing:.04em}
canvas{display:block}
.box{position:fixed;background:var(--c);color:var(--k);border:3px solid var(--k);box-shadow:5px 5px 0 var(--r);padding:8px 12px}
#hud{top:12px;left:12px;font-size:17px;line-height:1.45}#hud b{color:var(--r)}
#circ{top:12px;left:50%;transform:translateX(-50%);width:min(440px,60vw);text-align:center;display:none;background:var(--r);color:var(--c);box-shadow:5px 5px 0 var(--k);font-size:15px}
#hint{bottom:36px;left:50%;transform:translateX(-50%);display:none;text-align:center;max-width:90%;font-size:18px;background:var(--r);color:var(--c);box-shadow:5px 5px 0 var(--k)}
#reg{top:12px;right:12px;display:none;font-size:15px;line-height:1.5}
#mira{position:fixed;top:50%;left:50%;width:8px;height:8px;margin:-4px;border:2px solid var(--c);border-radius:50%;box-shadow:0 0 0 1px var(--k)}
#fx{position:fixed;inset:0;pointer-events:none;background:radial-gradient(transparent 55%,rgba(40,20,5,.5))}
#grain{position:fixed;inset:0;pointer-events:none;opacity:.18;mix-blend-mode:multiply;background:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='160' height='160'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='2'/%3E%3C/filter%3E%3Crect width='160' height='160' filter='url(%23n)'/%3E%3C/svg%3E")}
#start{position:fixed;inset:0;background:rgba(26,18,9,.8);display:flex;align-items:center;justify-content:center;cursor:pointer}
#card{position:static;max-width:520px;text-align:center;box-shadow:8px 8px 0 var(--r);padding:18px 26px}
#card h1{font-size:56px;color:var(--r);margin:0;line-height:1}#card h2{margin:4px 0 12px;font-size:20px}
#card p{font-family:Georgia,serif;text-transform:none;letter-spacing:0;font-size:15px;margin:8px 0}
.go{background:var(--r);color:var(--c);display:inline-block;padding:6px 16px;font-size:20px}
</style>
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script></head>
<body>
<div id="hud" class="box"></div><div id="circ" class="box"></div><div id="hint" class="box"></div><div id="reg" class="box"></div>
<div id="mira"></div><div id="fx"></div><div id="grain"></div>
<div id="start"><div id="card" class="box"><h1>L’Ammasso</h1><h2>Anno VI dell’Era Fascista</h2>
<p>Il podestà pretende il suo grano ogni giorno. Battilo, pesalo e dichiaralo… magari un po’ più abbondante del vero. L’ispettore, però, passa quando meno te l’aspetti.</p>
<span class="go">▶ Clicca per iniziare</span>
<p><b>WASD</b> muoviti · <b>Mouse</b> (o frecce) guarda · <b>Clic</b> batti il grano<br><b>Pesa:</b> E onesto, R +30%, T +80% · <b>Consorzio:</b> 1, 2, 3, 4 · <b>Tab:</b> registro</p></div></div>
<script>
const DAY=120;
const S={lire:0,sacco:0,cap:10,danno:1,brac:0,nasc:0,c:{danno:20,cap:30,brac:60,nasc:80},giorno:1,t:DAY,dichG:0,sosp:0,gap:0,totD:0,totR:0,ispT:30,circT:25,quotaX:1,marcia:0};
const $=i=>document.getElementById(i),quota=()=>Math.round((20+S.giorno*15)*S.quotaX);

// Scena e stile manifesto
const scene=new THREE.Scene();scene.fog=new THREE.Fog(0xf0d9a4,45,150);
const camera=new THREE.PerspectiveCamera(70,innerWidth/innerHeight,.1,400);camera.rotation.order="YXZ";camera.position.set(0,1.7,3);scene.add(camera);
const renderer=new THREE.WebGLRenderer({antialias:true});renderer.setSize(innerWidth,innerHeight);renderer.setPixelRatio(Math.min(devicePixelRatio,2));document.body.appendChild(renderer.domElement);
addEventListener("resize",()=>{camera.aspect=innerWidth/innerHeight;camera.updateProjectionMatrix();renderer.setSize(innerWidth,innerHeight)});
scene.add(new THREE.HemisphereLight(0xfff1d0,0x9a8050,.9));const sole=new THREE.DirectionalLight(0xfff0cc,.8);sole.position.set(18,30,10);scene.add(sole);
const grad=new THREE.DataTexture(new Uint8Array([110,180,255]),3,1,THREE.LuminanceFormat);grad.minFilter=grad.magFilter=THREE.NearestFilter;grad.needsUpdate=true;
const mat=c=>new THREE.MeshToonMaterial({color:c,gradientMap:grad});
const inkM=new THREE.MeshBasicMaterial({color:0x1a1209,side:THREE.BackSide});
function ink(o,s=1.06){const l=[];o.traverse(m=>{if(m.isMesh&&m.material!==inkM)l.push(m)});l.forEach(m=>{const k=new THREE.Mesh(m.geometry,inkM);k.scale.setScalar(s);m.add(k)});return o}
function box(w,h,d,c,x,y,z){const m=new THREE.Mesh(new THREE.BoxGeometry(w,h,d),mat(c));m.position.set(x,y,z);scene.add(ink(m));return m}
function etichetta(t,x,y,z){const c=document.createElement("canvas");c.width=256;c.height=64;const g=c.getContext("2d");g.fillStyle="#f1e3bd";g.fillRect(0,0,256,64);g.strokeStyle="#1a1209";g.lineWidth=5;g.strokeRect(2,2,252,60);g.fillStyle="#b3261e";g.font="34px Impact,Arial";g.textAlign="center";g.fillText(t,128,45);
const s=new THREE.Sprite(new THREE.SpriteMaterial({map:new THREE.CanvasTexture(c)}));s.scale.set(4,1,1);s.position.set(x,y,z);scene.add(s)}
function rumore(base,spec,rep){const c=document.createElement("canvas");c.width=c.height=128;const g=c.getContext("2d");g.fillStyle=base;g.fillRect(0,0,128,128);for(let i=0;i<700;i++){g.fillStyle=spec[i%spec.length];g.fillRect(Math.random()*128,Math.random()*128,3,3)}const t=new THREE.CanvasTexture(c);t.wrapS=t.wrapT=THREE.RepeatWrapping;t.repeat.set(rep,rep);return t}

// Cielo a fasce con sole rosso
(()=>{const c=document.createElement("canvas");c.width=1024;c.height=512;const g=c.getContext("2d");
["#4f86b0","#78a9c4","#a9c9c0","#dcd3a0","#f0c878"].forEach((k,i)=>{g.fillStyle=k;g.fillRect(0,i*52,1024,53)});g.fillStyle="#f0c878";g.fillRect(0,256,1024,256);
g.save();g.translate(700,170);for(let i=0;i<14;i++){g.beginPath();g.moveTo(0,0);g.arc(0,0,300,i*.45,i*.45+.14);g.closePath();g.fillStyle="rgba(255,238,180,.4)";g.fill()}
g.beginPath();g.arc(0,0,44,0,7);g.fillStyle="#c8321f";g.fill();g.restore();
scene.add(new THREE.Mesh(new THREE.SphereGeometry(300,24,16),new THREE.MeshBasicMaterial({map:new THREE.CanvasTexture(c),side:THREE.BackSide,fog:false})))})();

// Terreno, aia, campi
const terreno=new THREE.Mesh(new THREE.PlaneGeometry(400,400),new THREE.MeshToonMaterial({map:rumore("#7f9a48",["#6f8d3c","#8fab55"],70),gradientMap:grad}));terreno.rotation.x=-Math.PI/2;scene.add(terreno);
const aia=new THREE.Mesh(new THREE.CircleGeometry(14,48),new THREE.MeshToonMaterial({map:rumore("#d2b074",["#c19c5e","#e0c488"],6),gradientMap:grad}));aia.rotation.x=-Math.PI/2;aia.position.y=.02;scene.add(aia);
function campo(cx,cz,w,d,col){const n=Math.floor(w*d*2);const im=new THREE.InstancedMesh(new THREE.BoxGeometry(.12,1,.12),mat(col),n),m=new THREE.Matrix4();
for(let i=0;i<n;i++){const h=.7+Math.random()*.5;m.makeScale(1,h,1);m.setPosition(cx+(Math.random()-.5)*w,h/2,cz+(Math.random()-.5)*d);im.setMatrixAt(i,m)}scene.add(im)}
campo(-38,-38,30,30,0xe0a82e);campo(38,-42,30,25,0xd49a28);campo(-42,32,25,25,0xdcb03a);campo(40,36,30,30,0xe3b242);

// Cipressi, colline, casale
function cipresso(x,z,s){const g=new THREE.Group();const t=new THREE.Mesh(new THREE.CylinderGeometry(.15,.2,1,6),mat(0x4a3320));t.position.y=.5;const c=new THREE.Mesh(new THREE.ConeGeometry(.9,5,8),mat(0x2f5a2f));c.position.y=3.5;g.add(t,c);g.position.set(x,0,z);g.scale.setScalar(s);scene.add(ink(g))}
for(let i=0;i<10;i++)cipresso(-22+i*4.8,-19,1+Math.random()*.4);for(let i=0;i<5;i++){cipresso(-30,12+i*5,1.1);cipresso(30,12+i*5,1.1)}
for(let i=0;i<9;i++){const h=new THREE.Mesh(new THREE.SphereGeometry(30,12,8),mat(i%2?0x8aa860:0x7d9a58));h.scale.y=.35;h.position.set(-120+i*30,-2,-110-Math.random()*20);scene.add(h)}
box(11,5,6,0xefdcb0,0,2.5,-26);const tt=new THREE.Mesh(new THREE.ConeGeometry(8.2,3,4),mat(0xb5532f));tt.rotation.y=Math.PI/4;tt.scale.z=.62;tt.position.set(0,6.5,-26);scene.add(ink(tt));
box(1.4,2.4,.1,0x5a3a1a,0,1.2,-22.95);box(1,1,.1,0x2b3a4a,-3.5,3,-22.95);box(1,1,.1,0x2b3a4a,3.5,3,-22.95);

// Manifesti satirici
function cartellone(righe,x,z,ry){const c=document.createElement("canvas");c.width=256;c.height=340;const g=c.getContext("2d");
g.fillStyle="#b3261e";g.fillRect(0,0,256,340);g.fillStyle="#f1e3bd";g.fillRect(10,10,236,320);g.fillStyle="#e0a82e";g.beginPath();g.arc(128,90,50,0,7);g.fill();
g.strokeStyle="#1a1209";g.lineWidth=4;g.stroke();g.fillStyle="#b3261e";g.font="27px Impact,Arial";g.textAlign="center";righe.forEach((t,i)=>g.fillText(t,128,175+i*36));
const m=new THREE.Mesh(new THREE.PlaneGeometry(3,4),new THREE.MeshBasicMaterial({map:new THREE.CanvasTexture(c)}));m.position.set(x,2.6,z);m.rotation.y=ry;scene.add(m);
box(.15,3,.15,0x5a3a1a,x-1.4*Math.cos(ry),1.5,z+1.4*Math.sin(ry)*-1);box(.15,3,.15,0x5a3a1a,x+1.4*Math.cos(ry),1.5,z-1.4*Math.sin(ry)*-1)}
cartellone(["IL GRANO","È VITTORIA","(SE DICHIARATO)"],-7,-11,0);cartellone(["PIÙ GRANO,","MENO","DOMANDE"],8,-11,0);
cartellone(["TIMBRA","PRIMA DI","RACCOGLIERE"],22,6,-Math.PI/2);cartellone(["DICHIARARE","È PATRIOTTICO"],-22,6,Math.PI/2);

// Pesa e Consorzio
box(4,.2,4,0x777777,13,.1,0);box(2.4,2.6,2.4,0xefdcb0,15.8,1.3,-1.8);box(3.2,.3,3.2,0xb3261e,15.8,2.75,-1.8);box(.9,.9,.1,0x2b3a4a,14.55,1.7,-1.8);etichetta("PESA",14,4,-1);
box(4,1.1,1.5,0x8a5a2b,-13,.55,0);box(.2,2.6,.2,0x5a3a1a,-14.8,1.3,-.7);box(.2,2.6,.2,0x5a3a1a,-11.2,1.3,-.7);
for(let i=0;i<6;i++){const s=box(.67,.12,2.2,i%2?0xf1e3bd:0xb3261e,-14.67+i*.67,2.65,-.2);s.rotation.x=.2}
box(.6,.4,.4,0xd8c08a,-13.8,1.3,0);box(.5,.35,.4,0xd8c08a,-12.4,1.28,.1);etichetta("CONSORZIO",-13,4,0);

// Persone
function persona(cc,hc,alto){const g=new THREE.Group();const p=(geo,col,x,y)=>{const m=new THREE.Mesh(geo,mat(col));m.position.set(x,y,0);g.add(m)};
p(new THREE.CylinderGeometry(.1,.1,.6,8),0x3a2a1a,-.13,.3);p(new THREE.CylinderGeometry(.1,.1,.6,8),0x3a2a1a,.13,.3);p(new THREE.CylinderGeometry(.28,.34,1,10),cc,0,1.1);
p(new THREE.CylinderGeometry(.07,.07,.8,8),cc,-.38,1.1);p(new THREE.CylinderGeometry(.07,.07,.8,8),cc,.38,1.1);p(new THREE.SphereGeometry(.22,10,8),0xe0b890,0,1.8);
p(new THREE.CylinderGeometry(.42,.42,.04,14),hc,0,1.98);p(new THREE.CylinderGeometry(.2,.2,alto,10),hc,0,1.98+alto/2);g.scale.setScalar(.85);return ink(g)}
const ispettore=persona(0x1a1a1a,0x111111,.3);ispettore.position.set(11,0,3);ispettore.visible=false;scene.add(ispettore);
const braccianti=[];function nuovoBracciante(){const g=persona(0xe8e0c8,0xe0c060,.2);scene.add(g);braccianti.push({g,o:Math.random()*6.28})}

// Covoni e correggiato
const covoni=[];for(let i=0;i<7;i++){const a=i/7*Math.PI*2,m=new THREE.Group();
const f=new THREE.Mesh(new THREE.CylinderGeometry(.55,.75,1.1,10),mat(0xe0a82e));f.position.y=.55;const c=new THREE.Mesh(new THREE.ConeGeometry(.75,.9,10),mat(0xd49a28));c.position.y=1.55;
const l=new THREE.Mesh(new THREE.CylinderGeometry(.66,.66,.08,10),mat(0x8a5a2b));l.position.y=.65;m.add(f,c,l);m.position.set(Math.cos(a)*3.2,0,-4+Math.sin(a)*3.2);scene.add(ink(m));covoni.push({m,hp:5,max:5,back:0})}
const flail=new THREE.Group();const asta=new THREE.Mesh(new THREE.BoxGeometry(.06,.06,.9),mat(0x5a3a1a));asta.position.z=-.45;
const testa=new THREE.Mesh(new THREE.BoxGeometry(.08,.08,.5),mat(0x3a2410));testa.position.z=-1.1;flail.add(asta,testa);flail.position.set(.35,-.35,-.5);flail.rotation.x=.9;camera.add(flail);

// Chicchi che schizzano
const pz=[];for(let i=0;i<14;i++){const m=new THREE.Mesh(new THREE.BoxGeometry(.08,.08,.08),new THREE.MeshBasicMaterial({color:0xe0a82e}));m.visible=false;scene.add(m);pz.push({m,v:new THREE.Vector3(),l:0})}
function spruzza(p){let n=0;for(const q of pz)if(q.l<=0&&n<7){q.l=.7;q.m.visible=true;q.m.position.copy(p);q.v.set((Math.random()-.5)*3,2+Math.random()*2,(Math.random()-.5)*3);n++}}

// Circolari satiriche
const CIRC=[
["Circolare 47: marciare è obbligatorio. I braccianti lavorano a passo di marcia (x2 per 25 s).",()=>S.marcia=25],
["Circolare 12: il podestà visita l’aia. Quota di oggi +20%, ma c’è un premio per gli applausi (+15 lire).",()=>{S.quotaX=1.2;S.lire+=15}],
["Circolare 88: il grano va timbrato in triplice copia. Il sospetto cala di 15.",()=>S.sosp=Math.max(0,S.sosp-15)],
["Circolare 3: è vietato avere dubbi sul raccolto. Gli ispettori sono più zelanti (+20 sospetto).",()=>S.sosp=Math.min(100,S.sosp+20)],
["Circolare 66: per il morale, i sacchi sono dichiarati pieni. Il tuo sacco si riempie!",()=>S.sacco=S.cap],
["Circolare 101: il tempo è stato dichiarato sereno. Piove. Si lavora lo stesso (+30 s).",()=>S.t+=30]];
let yaw=0,pitch=0,bloccato=false,swing=0,colpito=false,msg="",msgT=0,ispVisT=0,circVis=0,walk=0;const tasti={};
function avviso(t,d){msg=t;msgT=d||2.5}
function stazioneVicina(){const p=camera.position;if(Math.hypot(p.x-13,p.z)<5)return"pesa";if(Math.hypot(p.x+13,p.z)<5)return"cons";return null}
function compra(tipo){if(stazioneVicina()!=="cons")return;const costo=Math.ceil(S.c[tipo]);if(S.lire<costo){avviso("Non hai abbastanza lire.");return}S.lire-=costo;
if(tipo==="danno"){S.danno++;S.c.danno*=1.8;avviso("Correggiato più pesante!")}
if(tipo==="cap"){S.cap+=5;S.c.cap*=1.7;avviso("Sacco più grande!")}
if(tipo==="brac"){S.brac++;S.c.brac*=1.35;nuovoBracciante();avviso("Un bracciante lavora per te (paga: un applauso).")}
if(tipo==="nasc"){S.nasc++;S.c.nasc*=1.9;avviso("Nascondiglio sotto il fienile: i falsi destano meno sospetti.")}}
function consegna(f){if(stazioneVicina()!=="pesa")return;if(S.sacco<=0){avviso("Il sacco è vuoto. Anche la burocrazia ha bisogno di grano.");return}
const reale=S.sacco,dich=Math.round(reale*f),falso=dich-reale;S.lire+=dich;S.dichG+=dich;S.totD+=dich;S.totR+=reale;S.gap+=falso;S.sosp=Math.min(100,S.sosp+falso*1.5/(1+.3*S.nasc));S.sacco=0;
avviso(falso>0?`Pesati ${reale} kg, dichiarati ${dich}. Il funzionario annota con un sorriso… (+${falso} falsi)`:`Consegnati ${reale} kg onesti. Il funzionario è sospettosamente deluso.`)}
function colpisci(){const fx=-Math.sin(yaw),fz=-Math.cos(yaw);let me=null,md=99;
for(const b of covoni){if(b.hp<=0)continue;const dx=b.m.position.x-camera.position.x,dz=b.m.position.z-camera.position.z,d=Math.hypot(dx,dz);if(d<3.4&&(dx*fx+dz*fz)/d>.4&&d<md){md=d;me=b}}
if(!me)return;const gu=Math.min(2*S.danno,S.cap-S.sacco);if(gu<=0){avviso("Sacco pieno! Portalo alla pesa.");return}
S.sacco+=gu;me.hp-=S.danno;me.m.scale.y=Math.max(.2,me.hp/me.max);spruzza(me.m.position.clone().setY(1.2));if(me.hp<=0){me.m.visible=false;me.back=6}}
function ispezione(){ispettore.visible=true;ispVisT=6;
if(S.gap<=0){avviso("L’ispettore conta il grano con aria severa: tutto in regola. Se ne va deluso.",5);S.sosp=Math.max(0,S.sosp-10);return}
if(Math.random()<S.sosp/100){const mu=Math.floor(S.lire*.4)+S.gap*2;S.lire=Math.max(0,S.lire-mu);S.dichG=Math.max(0,S.dichG-S.gap);S.totD-=S.gap;
avviso(`SCOPERTO! ${S.gap} kg dichiarati ma inesistenti. Multa: ${mu} lire e un lungo verbale.`,6);S.gap=0;S.sosp=20}
else{avviso("L’ispettore conta… sbaglia a contare e si fida. Per ora.",5);S.sosp=Math.max(0,S.sosp-10)}}
function fineGiorno(){const q=quota();
if(S.dichG>=q){const pr=20*S.giorno;S.lire+=pr;avviso(`Giorno ${S.giorno}: quota di ${q} kg raggiunta! Premio e medaglia di latta: ${pr} lire.`,6)}
else{const mu=Math.floor(S.lire*.3);S.lire-=mu;avviso(`Giorno ${S.giorno}: quota mancata (${Math.floor(S.dichG)}/${q}). Multa: ${mu} lire e una paternale.`,6)}
S.giorno++;S.dichG=0;S.quotaX=1;S.t=DAY}

// Comandi
addEventListener("keydown",e=>{tasti[e.code]=true;if(e.code==="Tab"){e.preventDefault();$("reg").style.display=$("reg").style.display==="block"?"none":"block"}
if(!bloccato)return;if(e.code==="KeyE")consegna(1);if(e.code==="KeyR")consegna(1.3);if(e.code==="KeyT")consegna(1.8);
if(e.code==="Digit1")compra("danno");if(e.code==="Digit2")compra("cap");if(e.code==="Digit3")compra("brac");if(e.code==="Digit4")compra("nasc")});
addEventListener("keyup",e=>{tasti[e.code]=false});
addEventListener("mousemove",e=>{if(!bloccato)return;yaw-=e.movementX*.0022;pitch=Math.max(-1.3,Math.min(1.3,pitch-e.movementY*.0022))});
addEventListener("mousedown",e=>{if(bloccato&&e.button===0&&swing===0){swing=.001;colpito=false}});
let senzaBlocco=false;function attivaSenzaBlocco(){senzaBlocco=true;bloccato=true;$("start").style.display="none"}
$("start").onclick=()=>{try{const r=document.documentElement.requestPointerLock();if(r&&r.catch)r.catch(attivaSenzaBlocco)}catch(e){attivaSenzaBlocco()}};
document.addEventListener("pointerlockchange",()=>{bloccato=document.pointerLockElement!==null||senzaBlocco;$("start").style.display=bloccato?"none":"flex"});
document.addEventListener("pointerlockerror",attivaSenzaBlocco);

// Ciclo
const orologio=new THREE.Clock();
function ciclo(){requestAnimationFrame(ciclo);const dt=Math.min(orologio.getDelta(),.05),t=orologio.elapsedTime;
if(bloccato){const v=4*(1-.4*(S.sacco/S.cap))*dt;let ax=0,az=0;if(tasti.KeyW)az--;if(tasti.KeyS)az++;if(tasti.KeyA)ax--;if(tasti.KeyD)ax++;
if(ax||az){const l=Math.hypot(ax,az);ax/=l;az/=l;camera.position.x+=(ax*Math.cos(yaw)+az*Math.sin(yaw))*v;camera.position.z+=(-ax*Math.sin(yaw)+az*Math.cos(yaw))*v;
camera.position.x=Math.max(-45,Math.min(45,camera.position.x));camera.position.z=Math.max(-45,Math.min(45,camera.position.z));walk+=dt*9}
camera.position.y=1.7+Math.sin(walk)*.04;
if(tasti.ArrowLeft)yaw+=1.8*dt;if(tasti.ArrowRight)yaw-=1.8*dt;if(tasti.ArrowUp)pitch=Math.min(1.3,pitch+1.2*dt);if(tasti.ArrowDown)pitch=Math.max(-1.3,pitch-1.2*dt);
camera.rotation.y=yaw;camera.rotation.x=pitch;
S.t-=dt;if(S.t<=0)fineGiorno();S.sosp=Math.max(0,S.sosp-.25*dt);
S.ispT-=dt;if(S.ispT<=0){S.ispT=25+Math.random()*25;ispezione()}
S.circT-=dt;if(S.circT<=0){S.circT=35+Math.random()*30;const c=CIRC[Math.floor(Math.random()*CIRC.length)];c[1]();$("circ").textContent=c[0];$("circ").style.display="block";circVis=8}
const pr=S.brac*.5*(S.marcia>0?2:0.5*2/2)*dt;S.lire+=pr;S.dichG+=pr;S.totD+=pr;S.totR+=pr;if(S.marcia>0)S.marcia-=dt}
if(circVis>0){circVis-=dt;if(circVis<=0)$("circ").style.display="none"}
if(swing>0){swing+=dt*4;flail.rotation.x=.9-1.5*Math.sin(Math.min(swing,1)*Math.PI);if(!colpito&&swing>.5){colpito=true;colpisci()}if(swing>=1){swing=0;flail.rotation.x=.9}}
for(const b of covoni)if(b.hp<=0){b.back-=dt;if(b.back<=0){b.hp=b.max;b.m.visible=true;b.m.scale.set(1,1,1)}}
for(const q of pz)if(q.l>0){q.l-=dt;q.v.y-=9*dt;q.m.position.addScaledVector(q.v,dt);if(q.l<=0)q.m.visible=false}
braccianti.forEach(b=>{const a=t*(S.marcia>0?.8:.4)+b.o;b.g.position.set(Math.cos(a)*6,0,-4+Math.sin(a)*6);b.g.rotation.y=-a});
if(ispVisT>0){ispVisT-=dt;if(ispVisT<=0)ispettore.visible=false}
const q=quota(),sc=S.sosp<30?"#2e7d32":S.sosp<65?"#b8860b":"#b3261e";
$("hud").innerHTML=`Giorno ${S.giorno} · ${Math.max(0,Math.ceil(S.t))}s<br>Quota: ${Math.floor(S.dichG)} / ${q} kg<br>Lire: ${Math.floor(S.lire)} · Sacco: ${S.sacco}/${S.cap} · Braccianti: ${S.brac}<br>Sospetto: <b style="color:${sc}">${Math.floor(S.sosp)}%</b>`;
if($("reg").style.display==="block")$("reg").innerHTML=`<b>REGISTRO DEL PODESTÀ</b><br>Grano reale: ${Math.floor(S.totR)} kg<br>Grano dichiarato: ${Math.floor(S.totD)} kg<br>Falsi da nascondere: ${Math.floor(S.gap)} kg<br>Nascondigli: ${S.nasc}`;
msgT-=dt;const st=stazioneVicina();let hint="";
if(msgT>0)hint=msg;else if(st==="pesa")hint=`E: onesto (${S.sacco} kg) · R: dichiara ${Math.round(S.sacco*1.3)} · T: dichiara ${Math.round(S.sacco*1.8)}`;
else if(st==="cons")hint=`1: Correggiato (${Math.ceil(S.c.danno)}) · 2: Sacco (${Math.ceil(S.c.cap)}) · 3: Bracciante (${Math.ceil(S.c.brac)}) · 4: Nascondiglio (${Math.ceil(S.c.nasc)})`;
$("hint").textContent=hint;$("hint").style.display=hint?"block":"none";
renderer.render(scene,camera)}
ciclo();
</script></body></html>
9.2 battaglia-del-grano.html (primo prototipo a numeri, pubblicato come artifact, scartato)
File singolo, salvataggio in localStorage con chiave bdg_save_v1. Esiste solo nell'ambiente di Claude (/mnt/user-data/outputs/battaglia-del-grano.html).
<!DOCTYPE html>
<html lang="it">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>La Battaglia del Grano</title>
<style>
:root{--bg:#f1e8d4;--card:#e6d9bd;--ink:#2b2418;--mut:#6d614a;--acc:#8a1c1c;--line:#bfae86;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#1c1812;--card:#2a241a;--ink:#eadfc6;--mut:#a59a80;--acc:#d9534f;--line:#4a402c}}
:root[data-theme="dark"]{--bg:#1c1812;--card:#2a241a;--ink:#eadfc6;--mut:#a59a80;--acc:#d9534f;--line:#4a402c}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--ink);font-family:Georgia,"Times New Roman",serif;line-height:1.4}
main{max-width:640px;margin:0 auto;padding:16px}
h1{font-size:1.5rem;margin:0;color:var(--acc);letter-spacing:.04em;text-transform:uppercase}
.sub{color:var(--mut);font-size:.85rem;margin:2px 0 12px}
.stat{text-align:center;margin:10px 0}
.stat b{font-size:2.2rem;display:block}
.stat span{color:var(--mut);font-size:.9rem}
#click{display:block;width:100%;padding:18px;font:inherit;font-size:1.2rem;font-weight:bold;background:var(--acc);color:#fff;border:0;border-radius:10px;cursor:pointer}
#click:active{transform:scale(.98)}
.ticker{min-height:3em;margin:12px 0;padding:10px;border-left:4px solid var(--acc);background:var(--card);font-style:italic;font-size:.92rem}
h2{font-size:1rem;margin:18px 0 6px;border-bottom:1px solid var(--line);padding-bottom:4px;text-transform:uppercase;letter-spacing:.05em}
.item{display:flex;justify-content:space-between;align-items:center;gap:10px;width:100%;text-align:left;font:inherit;color:var(--ink);background:var(--card);border:1px solid var(--line);border-radius:8px;padding:10px;margin-bottom:6px;cursor:pointer}
.item:disabled{opacity:.5;cursor:not-allowed}
.item small{display:block;color:var(--mut)}
.item .r{text-align:right;white-space:nowrap}
.foot{margin-top:20px;font-size:.75rem;color:var(--mut);text-align:center}
.foot button{font:inherit;font-size:.75rem;background:none;border:1px solid var(--line);color:var(--mut);border-radius:6px;padding:4px 8px;cursor:pointer}
#end{display:none;position:fixed;inset:0;background:rgba(0,0,0,.8);align-items:center;justify-content:center;padding:20px;z-index:20}
#end div{background:var(--bg);max-width:460px;padding:22px;border-radius:12px;border:2px solid var(--acc)}
#end h3{margin:0 0 8px;color:var(--acc)}
#end button{margin-top:10px;font:inherit;padding:10px 16px;border:0;border-radius:8px;background:var(--acc);color:#fff;cursor:pointer}
</style>
</head>
<body>
<main>
<h1>La Battaglia del Grano</h1>
<p class="sub">Anno IV E.F. · «Il pane è sacro. Il grano è vittoria.»</p>
<div class="stat"><b id="grain">0</b><span>quintali di grano (<span id="rate">0</span>/s)</span></div>
<button id="click">🌾 Trebbia il grano</button>
<div class="ticker" id="ticker">Il Duce ha dichiarato la Battaglia del Grano. Si comincia con le tue mani.</div>
<h2>Miglioramenti</h2><div id="upgs"></div>
<h2>Forze produttive</h2><div id="gens"></div>
<div class="foot">Salvataggio automatico · <button id="reset">Azzera la partita</button></div>
</main>
<div id="end"><div>
<h3>25 luglio 1943</h3>
<p>Hai raggiunto la «produzione record». Ma i numeri erano gonfiati, i granai vuoti e il pane razionato. Quella notte il Gran Consiglio sfiducia Mussolini: vent’anni di propaganda crollano in poche ore.</p>
<p>Puoi continuare a giocare, ma ormai sai come finisce.</p>
<button id="close">Continua</button>
</div></div>
<script>
const GENS=[
 {id:"brac",n:"Bracciante",d:"Paga: una pacca sulla spalla",c:15,r:0.5},
 {id:"trat",n:"Trattore Fordson",d:"Importato, ma chiamiamolo autarchico",c:110,r:3},
 {id:"bon",n:"Bonifica Pontina",d:"Paludi diventano campi (e città di fondazione)",c:1200,r:22},
 {id:"rad",n:"Altoparlanti in piazza",d:"Il raccolto è ottimo, lo dice la radio",c:13000,r:130},
 {id:"luce",n:"Cinegiornale LUCE",d:"Spighe dorate, sorrisi e orchestrine",c:140000,r:750},
 {id:"ger",n:"Gerarca provinciale",d:"Moltiplica i dati, non il grano",c:1500000,r:4500}
];
const UPG=[
 {id:"falce",n:"Falce nuova",d:"Click ×2",c:100,t:"click",m:2},
 {id:"disc",n:"Discorso dal balcone",d:"Click ×2",c:1200,t:"click",m:2},
 {id:"tess",n:"Tessera del partito",d:"Produzione ×1,5",c:8000,t:"all",m:1.5},
 {id:"sab",n:"Sabato fascista",d:"Click ×2",c:60000,t:"click",m:2},
 {id:"stat",n:"Statistiche ritoccate",d:"Produzione ×2",c:500000,t:"all",m:2}
];
const MSG=[
 "«Vincere!» Intanto, vinci un altro sacco di grano.",
 "Il podestà annuncia che il raccolto è il più grande della storia. Non ha ancora contato.",
 "Un ispettore passa a controllare: tutto in regola, soprattutto i suoi appunti.",
 "Il manifesto dice «Il pane non si spreca». Il pane, però, non si vede.",
 "Arriva una circolare: da domani si lavora con più entusiasmo.",
 "Il federale loda la tua dedizione. Ti chiede un contributo volontario.",
 "Sul giornale locale la tua trebbiatura è un trionfo nazionale.",
 "Il parroco benedice il grano. Il gerarca lo requisisce."
];
const KEY="bdg_save_v1",TOT=1e7;
let S={g:0,t:0,own:{},up:{},last:Date.now(),done:false};
try{const x=JSON.parse(localStorage.getItem(KEY));if(x)S=Object.assign(S,x)}catch(e){}
const $=id=>document.getElementById(id);
function fmt(n){if(n<1e3)return n<10?n.toFixed(1).replace(".",","):Math.floor(n).toString();
 const u=["","k","M","Md","B"];let i=0;while(n>=1e3&&i<4){n/=1e3;i++}return n.toFixed(2).replace(".",",")+u[i]}
const cost=(g)=>Math.ceil(g.c*Math.pow(1.15,S.own[g.id]||0));
function mult(t){return UPG.filter(u=>S.up[u.id]&&u.t===t).reduce((a,u)=>a*u.m,1)}
const clickVal=()=>mult("click");
function rate(){return GENS.reduce((a,g)=>a+(S.own[g.id]||0)*g.r,0)*mult("all")}
function build(){
 $("gens").innerHTML="";$("upgs").innerHTML="";
 GENS.forEach(g=>{const b=document.createElement("button");b.className="item";b.id="g_"+g.id;
  b.onclick=()=>{const c=cost(g);if(S.g>=c){S.g-=c;S.own[g.id]=(S.own[g.id]||0)+1;ui()}};
  $("gens").appendChild(b)});
 UPG.forEach(u=>{const b=document.createElement("button");b.className="item";b.id="u_"+u.id;
  b.onclick=()=>{if(!S.up[u.id]&&S.g>=u.c){S.g-=u.c;S.up[u.id]=1;ui()}};
  $("upgs").appendChild(b)})}
function ui(){
 $("grain").textContent=fmt(S.g);$("rate").textContent=fmt(rate());
 GENS.forEach(g=>{const b=$("g_"+g.id),c=cost(g);
  b.disabled=S.g<c;
  b.innerHTML=`<span>${g.n}<small>${g.d}</small></span><span class="r">${fmt(c)}<small>posseduti: ${S.own[g.id]||0}</small></span>`});
 UPG.forEach(u=>{const b=$("u_"+u.id);
  b.style.display=S.up[u.id]?"none":"flex";b.disabled=S.g<u.c;
  b.innerHTML=`<span>${u.n}<small>${u.d}</small></span><span class="r">${fmt(u.c)}</span>`})}
function add(x){S.g+=x;S.t+=x;
 if(!S.done&&S.t>=TOT){S.done=true;$("end").style.display="flex"}}
$("click").onclick=()=>{add(clickVal());ui()};
$("close").onclick=()=>$("end").style.display="none";
$("reset").onclick=()=>{if(confirm("Vuoi davvero ricominciare da zero?")){try{localStorage.removeItem(KEY)}catch(e){}location.reload()}};
function save(){S.last=Date.now();try{localStorage.setItem(KEY,JSON.stringify(S))}catch(e){}}
const off=(Date.now()-S.last)/1000;
if(off>10){const gain=rate()*Math.min(off,28800);if(gain>0){add(gain);$("ticker").textContent="Mentre eri via il grano è aumentato di "+fmt(gain)+" quintali (secondo il federale)."}}
build();ui();
let prev=Date.now();
setInterval(()=>{const n=Date.now(),dt=(n-prev)/1000;prev=n;add(rate()*dt);ui()},250);
setInterval(save,5000);
setInterval(()=>{$("ticker").textContent=MSG[Math.floor(Math.random()*MSG.length)]},14000);
addEventListener("beforeunload",save);
</script>
</body>
</html>
9.3 index.html di prova (primo file creato sul PC)
<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="utf-8">
  <title>Mussolinia</title>
</head>
<body>
  <h1>Mussolinia: la Battaglia del Grano</h1>
  <p>Il progetto è partito.</p>
</body>
</html>
9.4 Scheletro multi-file (abbandonato)
Incrementale a numeri con moduli ES. L'utente ha riferito che il pulsante non rispondeva; causa non diagnosticata.
index.html
<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Mussolinia</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <main>
    <h1>Mussolinia</h1>
    <p class="sottotitolo">La Battaglia del Grano · Anno VI E.F.</p>
    <div class="grano"><b id="grano">0</b> quintali (<span id="produzione">0</span>/s)</div>
    <button id="btn-raccogli">🌾 Raccogli il grano</button>
    <h2>Forze produttive</h2>
    <div id="elenco"></div>
  </main>
  <script type="module" src="js/main.js"></script>
</body>
</html>
css/style.css
body { margin: 0; background: #f1e8d4; color: #2b2418; font-family: Georgia, serif; }
main { max-width: 600px; margin: 0 auto; padding: 16px; }
h1 { color: #8a1c1c; text-transform: uppercase; margin-bottom: 0; }
.sottotitolo { color: #6d614a; margin-top: 4px; }
.grano { text-align: center; margin: 16px 0; }
.grano b { font-size: 2.4rem; display: block; }
#btn-raccogli { width: 100%; padding: 18px; font-size: 1.2rem; font-weight: bold;
  background: #8a1c1c; color: white; border: 0; border-radius: 10px; cursor: pointer; }
.voce { display: flex; justify-content: space-between; width: 100%; margin-top: 8px;
  padding: 10px; font: inherit; text-align: left; background: #e6d9bd;
  border: 1px solid #bfae86; border-radius: 8px; cursor: pointer; }
.voce:disabled { opacity: 0.5; cursor: not-allowed; }
js/data.js
export const GENERATORI = [
  { id: "bracciante", nome: "Bracciante", desc: "Paga: una pacca sulla spalla", costo: 15, produzione: 0.5 },
  { id: "trattore", nome: "Trattore Fordson", desc: "Importato, ma chiamiamolo autarchico", costo: 110, produzione: 3 },
  { id: "bonifica", nome: "Bonifica", desc: "Le paludi diventano campi", costo: 1200, produzione: 22 },
];
js/game.js
import { GENERATORI } from "./data.js";

const CHIAVE_SALVATAGGIO = "mussolinia_salvataggio_v1";

export const stato = { grano: 0, posseduti: {} };

export function costo(g) {
  return Math.ceil(g.costo * Math.pow(1.15, stato.posseduti[g.id] || 0));
}

export function produzioneAlSecondo() {
  let totale = 0;
  for (const g of GENERATORI) {
    totale += (stato.posseduti[g.id] || 0) * g.produzione;
  }
  return totale;
}

export function raccogli() {
  stato.grano += 1;
}

export function compra(id) {
  const g = GENERATORI.find((x) => x.id === id);
  const prezzo = costo(g);
  if (stato.grano >= prezzo) {
    stato.grano -= prezzo;
    stato.posseduti[id] = (stato.posseduti[id] || 0) + 1;
  }
}

export function passaTempo(secondi) {
  stato.grano += produzioneAlSecondo() * secondi;
}

export function salva() {
  localStorage.setItem(CHIAVE_SALVATAGGIO, JSON.stringify(stato));
}

export function carica() {
  const testo = localStorage.getItem(CHIAVE_SALVATAGGIO);
  if (testo) Object.assign(stato, JSON.parse(testo));
}
js/ui.js
import { GENERATORI } from "./data.js";
import { stato, costo, produzioneAlSecondo, compra } from "./game.js";

const elGrano = document.getElementById("grano");
const elProduzione = document.getElementById("produzione");
const elElenco = document.getElementById("elenco");
const bottoni = {};

function formatta(n) {
  return n < 10 ? n.toFixed(1).replace(".", ",") : Math.floor(n).toLocaleString("it-IT");
}

export function costruisci() {
  for (const g of GENERATORI) {
    const b = document.createElement("button");
    b.className = "voce";
    b.onclick = () => { compra(g.id); aggiorna(); };
    elElenco.appendChild(b);
    bottoni[g.id] = b;
  }
}

export function aggiorna() {
  elGrano.textContent = formatta(stato.grano);
  elProduzione.textContent = formatta(produzioneAlSecondo());
  for (const g of GENERATORI) {
    const b = bottoni[g.id];
    const prezzo = costo(g);
    b.disabled = stato.grano < prezzo;
    b.innerHTML = `<span>${g.nome}<br><small>${g.desc}</small></span>` +
      `<span>${formatta(prezzo)}<br><small>posseduti: ${stato.posseduti[g.id] || 0}</small></span>`;
  }
}
js/main.js
import { raccogli, passaTempo, salva, carica } from "./game.js";
import { costruisci, aggiorna } from "./ui.js";

carica();
costruisci();
aggiorna();

document.getElementById("btn-raccogli").onclick = () => { raccogli(); aggiorna(); };

let ultimo = Date.now();
setInterval(() => {
  const adesso = Date.now();
  passaTempo((adesso - ultimo) / 1000);
  ultimo = adesso;
  aggiorna();
}, 250);

setInterval(salva, 5000);
9.5 Prototipo 2D con Phaser (sostituiva index.html, scartato)
Vista dall'alto: campi da seminare e raccogliere, Ammasso e Consorzio, braccianti. Libreria Phaser 3.80.1 da cdn.jsdelivr.net. L'utente ha confermato che funzionava, ma voleva la prima persona.
<!DOCTYPE html>
<html lang="it">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Mussolinia</title>
<style>body{margin:0;background:#1c1812;display:flex;justify-content:center}</style>
<script src="https://cdn.jsdelivr.net/npm/phaser@3.80.1/dist/phaser.min.js"></script>
</head>
<body>
<script>
const S = { grano: 0, porto: 0, cap: 5, brac: 0, costoBrac: 20, costoSacco: 30 };

class Gioco extends Phaser.Scene {
  create() {
    this.add.rectangle(400, 300, 800, 600, 0xc9b98a);
    this.oggetti = [];

    // Campi (6)
    for (let i = 0; i < 6; i++) {
      const x = 330 + (i % 3) * 120, y = 220 + Math.floor(i / 3) * 120;
      const r = this.add.rectangle(x, y, 100, 100, 0x6b4a2b).setStrokeStyle(2, 0x3d2a17);
      this.oggetti.push({ tipo: "campo", x, y, r, stato: 0, t: 0 });
    }
    // Ammasso e Consorzio
    this.add.rectangle(90, 250, 110, 130, 0x8a1c1c).setStrokeStyle(3, 0x4a0e0e);
    this.add.text(90, 250, "AMMASSO", { fontSize: "16px", color: "#fff" }).setOrigin(0.5);
    this.oggetti.push({ tipo: "ammasso", x: 90, y: 250 });
    this.add.rectangle(90, 440, 110, 110, 0x4a6a3a).setStrokeStyle(3, 0x24361c);
    this.add.text(90, 440, "CONSORZIO", { fontSize: "15px", color: "#fff" }).setOrigin(0.5);
    this.oggetti.push({ tipo: "consorzio", x: 90, y: 440 });

    // Giocatore: corpo + cappello
    this.pl = this.add.container(400, 520, [
      this.add.circle(0, 0, 14, 0x2b2b2b),
      this.add.rectangle(0, -12, 26, 6, 0xe0c060),
    ]);

    // Scritte
    this.hud = this.add.text(12, 10, "", { fontSize: "18px", color: "#2b2418", backgroundColor: "#f1e8d4" });
    this.hint = this.add.text(400, 575, "", { fontSize: "18px", color: "#fff", backgroundColor: "#8a1c1c" }).setOrigin(0.5);

    // Comandi
    this.cur = this.input.keyboard.createCursorKeys();
    this.keys = this.input.keyboard.addKeys("W,A,S,D,SPACE,ONE,TWO");
    this.input.on("pointerdown", (p) => { this.meta = { x: p.worldX, y: p.worldY }; });
  }

  nuovoBracciante() {
    const c = this.add.circle(Phaser.Math.Between(250, 700), Phaser.Math.Between(150, 450), 9, 0x7a5a2a);
    this.tweens.add({
      targets: c, x: Phaser.Math.Between(250, 700), y: Phaser.Math.Between(150, 450),
      duration: Phaser.Math.Between(2000, 4000), yoyo: true, repeat: -1, ease: "Sine.easeInOut",
    });
  }

  update(t, dt) {
    const k = this.keys, c = this.cur, p = this.pl, v = 180 * dt / 1000;
    let vx = 0, vy = 0;
    if (k.A.isDown || c.left.isDown) vx = -1;
    if (k.D.isDown || c.right.isDown) vx = 1;
    if (k.W.isDown || c.up.isDown) vy = -1;
    if (k.S.isDown || c.down.isDown) vy = 1;
    if (vx || vy) {
      this.meta = null;
      const l = Math.hypot(vx, vy);
      p.x += (vx / l) * v; p.y += (vy / l) * v;
    } else if (this.meta) {
      const dx = this.meta.x - p.x, dy = this.meta.y - p.y, d = Math.hypot(dx, dy);
      if (d < 4) this.meta = null; else { p.x += (dx / d) * v; p.y += (dy / d) * v; }
    }
    p.x = Phaser.Math.Clamp(p.x, 20, 780);
    p.y = Phaser.Math.Clamp(p.y, 60, 580);

    // Crescita campi
    for (const o of this.oggetti) {
      if (o.tipo === "campo" && o.stato === 1) {
        o.t -= dt;
        if (o.t <= 0) { o.stato = 2; o.r.setFillStyle(0xd9a82a); }
      }
    }
    // Braccianti producono da soli
    S.grano += S.brac * 0.5 * dt / 1000;

    // Oggetto vicino
    let vic = null, best = 80;
    for (const o of this.oggetti) {
      const d = Phaser.Math.Distance.Between(p.x, p.y, o.x, o.y);
      if (d < best) { best = d; vic = o; }
    }
    let testo = "";
    if (vic) {
      if (vic.tipo === "campo") {
        testo = vic.stato === 0 ? "SPAZIO: semina" : vic.stato === 1 ? "Sta crescendo..." : "SPAZIO: raccogli";
        if (Phaser.Input.Keyboard.JustDown(k.SPACE)) {
          if (vic.stato === 0) { vic.stato = 1; vic.t = 4000; vic.r.setFillStyle(0x4a7a2a); }
          else if (vic.stato === 2 && S.porto < S.cap) { S.porto++; vic.stato = 0; vic.r.setFillStyle(0x6b4a2b); }
        }
      } else if (vic.tipo === "ammasso") {
        testo = "SPAZIO: consegna il grano";
        if (Phaser.Input.Keyboard.JustDown(k.SPACE)) { S.grano += S.porto; S.porto = 0; }
      } else {
        testo = `1: Bracciante (${S.costoBrac})   2: Sacco +5 (${S.costoSacco})`;
        if (Phaser.Input.Keyboard.JustDown(k.ONE) && S.grano >= S.costoBrac) {
          S.grano -= S.costoBrac; S.brac++; S.costoBrac = Math.ceil(S.costoBrac * 1.4); this.nuovoBracciante();
        }
        if (Phaser.Input.Keyboard.JustDown(k.TWO) && S.grano >= S.costoSacco) {
          S.grano -= S.costoSacco; S.cap += 5; S.costoSacco = Math.ceil(S.costoSacco * 1.6);
        }
      }
    }
    this.hint.setText(testo).setVisible(testo !== "");
    this.hud.setText(`Grano: ${Math.floor(S.grano)}   Sacco: ${S.porto}/${S.cap}   Braccianti: ${S.brac}`);
  }
}

new Phaser.Game({
  type: Phaser.AUTO, width: 800, height: 600,
  scale: { mode: Phaser.Scale.FIT, autoCenter: Phaser.Scale.CENTER_BOTH },
  scene: Gioco,
});
</script>
</body>
</html>
9.6 Comandi usati nel terminale e in Git
Eseguiti con esito confermato dall'utente:
node -v
git init
Forniti a Claude, ma senza conferma dell'esecuzione da parte dell'utente:
git --version
cd Documents
mkdir mussolinia
cd mussolinia
code .
git config --global user.name "Il Tuo Nome"
git config --global user.email "tua@email.it"
git add .
git commit -m "Prototipo 1: aia in prima persona"
9.7 Fix del blocco puntatore (già integrato nella v3)
Causa dell'errore WrongDocumentError: il browser rifiutava il blocco del mouse sull'elemento canvas. Soluzione adottata: richiesta su document.documentElement con gestione dell'errore e modalità di riserva con le frecce.
let senzaBlocco = false;
function attivaSenzaBlocco() {
  senzaBlocco = true;
  bloccato = true;
  $("start").style.display = "none";
}
function avvia() {
  try {
    const r = document.documentElement.requestPointerLock();
    if (r && r.catch) r.catch(attivaSenzaBlocco);
  } catch (e) { attivaSenzaBlocco(); }
}
$("start").onclick = avvia;
document.addEventListener("pointerlockchange", () => {
  bloccato = document.pointerLockElement !== null || senzaBlocco;
  $("start").style.display = bloccato ? "none" : "flex";
});
document.addEventListener("pointerlockerror", attivaSenzaBlocco);
Nelle versioni successive alla v1 sono state aggiunte anche le frecce per guardarsi attorno (nel ciclo di gioco, dentro if(bloccato): ArrowLeft/ArrowRight cambiano yaw, ArrowUp/ArrowDown cambiano pitch, poi si aggiornano camera.rotation).
