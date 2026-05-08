[Philosophen_Konzepte_6.html](https://github.com/user-attachments/files/27512910/Philosophen_Konzepte_6.html)
<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Philosophen & ihre Konzepte</title>
<style>
* { box-sizing: border-box; margin: 0; padding: 0; }
body { font-family: Arial, sans-serif; background: #f0f4f8; padding: 20px; }
h1 { text-align: center; color: #1F3864; font-size: 24px; margin-bottom: 6px; }
.subtitle { text-align: center; color: #666; font-size: 13px; margin-bottom: 20px; }
.tabs { display: flex; flex-wrap: wrap; gap: 8px; justify-content: center; margin-bottom: 24px; }
button.tab { padding: 9px 20px; border-radius: 24px; border: 3px solid transparent; cursor: pointer; font-size: 13px; font-weight: 700; color: #fff; }
button.tab.active { border-color: #fff; box-shadow: 0 0 0 3px rgba(0,0,0,0.3); }
.grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(310px, 1fr)); gap: 16px; }
.card { background: #fff; border-radius: 12px; box-shadow: 0 2px 8px rgba(0,0,0,0.1); overflow: hidden; }
.card.hidden { display: none; }
.card-head { padding: 14px 16px; }
.card-dates { font-size: 11px; color: rgba(255,255,255,0.7); margin-bottom: 3px; }
.card-name { font-size: 16px; font-weight: 800; color: #fff; }
.card-pos { font-size: 11px; color: rgba(255,255,255,0.85); margin-top: 2px; }
.card-body { padding: 14px 16px; }
.tags { margin-bottom: 10px; }
.tag { display: inline-block; background: #eef3fb; color: #1F3864; border: 1px solid #c8d8f0; border-radius: 12px; padding: 3px 9px; font-size: 10px; font-weight: 700; margin: 2px; }
.blk { margin-bottom: 11px; }
.blk-label { font-size: 10px; font-weight: 800; color: #999; text-transform: uppercase; letter-spacing: 0.7px; margin-bottom: 4px; }
.core { background: #fffbe6; border-left: 4px solid #f0c040; padding: 8px 11px; border-radius: 0 8px 8px 0; font-size: 12px; color: #4a3800; line-height: 1.6; }
ul.clist { list-style: none; }
ul.clist li { font-size: 12px; color: #333; padding: 4px 0; border-bottom: 1px solid #f5f5f5; line-height: 1.5; }
ul.clist li:last-child { border-bottom: none; }
ul.clist li::before { content: "-> "; color: #aaa; font-weight: bold; }
.memo { background: #e8f5ef; border-left: 4px solid #2E7D5E; padding: 8px 11px; border-radius: 0 8px 8px 0; font-size: 12px; color: #1a4a33; font-style: italic; line-height: 1.6; }
.conns { display: flex; flex-wrap: wrap; gap: 5px; }
.conn { background: #eef2fb; color: #2E5EA8; border: 1px solid #c0ccee; border-radius: 12px; padding: 3px 10px; font-size: 11px; cursor: pointer; transition: all 0.15s; }
.conn:hover { background: #2E5EA8; color: #fff; }
.card.highlight { outline: 3px solid #f0c040; outline-offset: 4px; }
</style>
</head>
<body>

<h1>Philosophen &amp; ihre Konzepte</h1>
<p class="subtitle">Philosophieunterricht S6-S7 | Klicke auf ein Themenfeld zum Filtern</p>

<div class="tabs">
  <button class="tab active" data-filter="all" style="background:#555">Alle</button>
  <button class="tab" data-filter="ET" style="background:#1F3864">Erkenntnistheorie</button>
  <button class="tab" data-filter="Ethik" style="background:#7B2D8B">Ethik</button>
  <button class="tab" data-filter="Staat" style="background:#B8520A">Staatsphilosophie</button>
  <button class="tab" data-filter="Anthro" style="background:#1a6e4a">Anthropologie</button>
</div>

<div class="grid" id="grid"></div>

<script>
var data = [
  {name:"Sextus Empiricus",dates:"ca. 160-210 n. Chr.",field:"ET",color:"#2c5f9e",pos:"Skeptizismus",tags:["Skepsis","Epoche","Ataraxie"],core:"Sicheres Wissen ist unerreichbar. Urteil zurückhalten (Epoche) führt zur Seelenruhe (Ataraxie).",concepts:["Skepsis: systematischer Zweifel an allen Erkenntnisansprüchen","Epoche: Urteilsenthaltung - weder Ja noch Nein","Ataraxie: innere Ruhe durch Nicht-Urteilen","Sinne und Vernunft sind beide fehlbar"],memo:"Da der Skeptiker weder bejahen noch verneinen will, lebt er ohne feste Meinungen.",conns:["Descartes (methodischer Zweifel)","Hume (radikale Skepsis)"]},
  {name:"Platon",dates:"427-347 v. Chr.",field:"ET",color:"#1a5276",pos:"Ideenlehre / Rationalismus",tags:["Ideen","Höhlengleichnis","Anamnesis","Doxa / Episteme"],core:"Hinter den vergänglichen Dingen liegen ewige Ideen. Wahres Wissen = Erkenntnis der Ideen durch Vernunft, nicht durch Sinne.",concepts:["Doxa (Meinung) vs. Episteme (Wissen): nur Episteme trifft die Ideen","Ideenlehre: ewige, unveränderliche Urbilder hinter sinnlichen Dingen","Höhlengleichnis: Aufstieg von Schatten zur Ideenschau","Anamnesis: Lernen = Wiedererinnern","Vier Stufen: Einbildung - Meinen - Denken - Ideenschau"],memo:"Vernunft, nicht Sinne, führt zur Wahrheit. Die meisten leben in einer Welt der Schatten.",conns:["Descartes (Rationalismus)","Kant (Idealismus)"]},
  {name:"Rene Descartes",dates:"1596-1650",field:"ET",color:"#154360",pos:"Rationalismus / methodischer Zweifel",tags:["Cogito ergo sum","Methodischer Zweifel","Angeborene Ideen","Böser Dämon"],core:"Zweifle an allem - was bleibt, ist unbezweifelbar. Im Zweifel selbst liegt die erste Gewissheit: Ich denke, also bin ich.",concepts:["Methodischer Zweifel: alles infrage stellen, um Gewissheit zu finden","Böser Dämon: hypothetische Instanz, die uns in allem täuscht","Cogito ergo sum: das Denken selbst ist unbezweifelbar","Angeborene Ideen: Vernunftwahrheiten unabhängig von Erfahrung","Dualismus: Geist (res cogitans) vs. Körper (res extensa)"],memo:"Cogito ergo sum - Im Zweifeln selbst liegt die erste und einzige Gewissheit.",conns:["Platon (Rationalismus)","Locke & Hume (Gegenantwort)"]},
  {name:"John Locke (ET)",dates:"1632-1704",field:"ET",color:"#1a5276",pos:"Empirismus / Tabula rasa",tags:["Tabula rasa","Sensation","Reflexion","Primär-/Sekundärqualitäten"],core:"Der Geist ist bei Geburt leer (Tabula rasa). Alles Wissen kommt aus Erfahrung - keine angeborenen Ideen.",concepts:["Tabula rasa: Geist als unbeschriebenes Blatt bei der Geburt","Sensation: aeußere Sinneserfahrung als Erkenntnisquelle","Reflexion: innere Beobachtung eigener Geistestätigkeiten","Primärqualitäten: objektiv (Ausdehnung, Gestalt)","Sekundärqualitäten: subjektiv (Farbe, Geschmack, Geruch)"],memo:"Nichts ist im Verstand, was nicht vorher in den Sinnen war. Kein angeborenes Wissen.",conns:["Descartes (Gegensatz)","Hume (Radikalisierung)","Kant (Synthese)"]},
  {name:"David Hume",dates:"1711-1776",field:"ET",color:"#154360",pos:"Radikaler Empirismus / Skepsis",tags:["Impressions & Ideas","Induktionsproblem","Kausalität als Gewohnheit"],core:"Alles Denken stammt aus Sinneseindrücken. Kausalität ist keine Vernunftwahrheit, sondern bloss Gewohnheit.",concepts:["Impressions: lebhafte Sinneseindrücke (Primärquelle)","Ideas: abgeschwächte Kopien der Eindrücke","Induktionsproblem: Vergangenheit garantiert nie die Zukunft","Kausalität als Gewohnheit: wir sehen nur Abfolge, nie Notwendigkeit","Skepsis gegenüber Metaphysik: Gott, Seele nicht aus Erfahrung ableitbar"],memo:"Wir sehen nie Kausalität - nur gewohnte Abfolge. Kausalität ist eine Erwartung, kein Naturgesetz.",conns:["Locke (Empirismus)","Kant (Antwort auf Hume)","Popper (Induktionsproblem)"]},
  {name:"Immanuel Kant (ET)",dates:"1724-1804",field:"ET",color:"#1f4e79",pos:"Kritizismus / Transzendentalphilosophie",tags:["Kopernikanische Wende","A priori","Ding an sich","Kategorien"],core:"Nicht Erkenntnis richtet sich nach Dingen - Dinge erscheinen uns so, wie unser Verstand sie ordnet.",concepts:["Kopernikanische Wende: das Subjekt formt die Erkenntnis","A priori: Raum & Zeit als Anschauungsformen vor aller Erfahrung","Kategorien: Kausalität, Substanz etc. als Verstandesformen","Ding an sich: Wirklichkeit jenseits unserer Wahrnehmung (unerkennbar)","Synthetische Urteile a priori: notwendig UND erkenntniserweiternd"],memo:"Anschauungen ohne Begriffe sind blind, Begriffe ohne Anschauungen sind leer.",conns:["Hume (Anlass der Synthese)","Locke (Empirismus aufgenommen)"]},
  {name:"Karl Popper",dates:"1902-1994",field:"ET",color:"#1a3a6e",pos:"Falsifikationismus",tags:["Falsifikation","Bewährung","Kritischer Rationalismus","Pseudowissenschaft"],core:"Eine Theorie ist nur dann wissenschaftlich, wenn sie grundsätzlich widerlegbar ist. Wissen bleibt immer vorläufig.",concepts:["Falsifikationsprinzip: Wissenschaft definiert sich durch Widerlegbarkeit","Bewährung: Theorien sind nie bewiesen - nur vorläufig nicht widerlegt","Kritischer Rationalismus: Fortschritt durch Fehlersuche","Abgrenzungsproblem: Wissenschaft vs. Pseudowissenschaft","Ablehnung der Induktion: viele Beobachtungen beweisen nichts"],memo:"Die Wissenschaft baut nicht auf Felsengrund - sie steht auf Sumpf. Alles Wissen ist vorläufig.",conns:["Hume (Induktionsproblem)","Kuhn (Kontroverse)","Feyerabend (Kritik)"]},
  {name:"Thomas Kuhn",dates:"1922-1996",field:"ET",color:"#215484",pos:"Paradigmentheorie",tags:["Paradigma","Normalwissenschaft","Paradigmenwechsel","Inkommensurabilität"],core:"Wissenschaft arbeitet in Paradigmen. Fortschritt geschieht nicht graduell, sondern durch Revolutionen.",concepts:["Paradigma: gemeinsamer Denkrahmen einer Wissenschaftsgemeinschaft","Normalwissenschaft: Rätsellösen innerhalb des bestehenden Paradigmas","Anomalie: Befund, den das Paradigma nicht erklären kann","Krise: Häufung von Anomalien erschüttert das Paradigma","Inkommensurabilität: alte und neue Paradigmen nicht direkt vergleichbar"],memo:"Wissenschaftlicher Fortschritt ist Revolution, keine ruhige Evolution.",conns:["Popper (Kritik)","Feyerabend (Relativismus)"]},
  {name:"Paul Feyerabend",dates:"1924-1994",field:"ET",color:"#1c3d6b",pos:"Methodenpluralismus",tags:["Anything goes","Methodenpluralismus","Wissenschaftskritik"],core:"Es gibt keine einheitliche Methode der Wissenschaft. Grosse Fortschritte entstanden durch Regelbruch.",concepts:["'Anything goes': keine Methode darf absolut gesetzt werden","Methodenpluralismus: verschiedene Methoden sind nötig","Wissenschaft als Ideologie: geniesst zu viel unkritische Autorität","Inkommensurabilität: Theorien oft nicht miteinander vergleichbar","Pluralismus der Wissensformen: andere Kulturen haben legitime Erkenntnisse"],memo:"Galilei selbst brach Regeln. Grosser Fortschritt entstand nie durch Gehorsam.",conns:["Kuhn (Paradigmen)","Popper (Kritik am Falsifikationismus)"]},
  {name:"Aristoteles (Ethik)",dates:"384-322 v. Chr.",field:"Ethik",color:"#6b2580",pos:"Tugendethik / Eudaimonia",tags:["Eudaimonia","Tugend (Arete)","Mesoteslehre","Zoon politikon"],core:"Das Ziel des Menschen ist Glückseligkeit (Eudaimonia) durch Tugend und vernünftiges Leben in der Gemeinschaft.",concepts:["Eudaimonia: Glückseligkeit als höchstes Ziel des Lebens","Tugend (Arete): Mitte zwischen zwei Extremen (Mesoteslehre)","Dianoetische Tugenden: Verstandestugenden (lernbar)","Ethische Tugenden: Charaktertugenden (durch Uebung)","Zoon politikon: Mensch von Natur auf Gemeinschaft angewiesen"],memo:"Tugend ist die Mitte: Tapferkeit liegt zwischen Feigheit und Tollkühnheit.",conns:["Kant (Pflicht vs. Tugend)","Epikur (Glück als Ziel)"]},
  {name:"Epikur",dates:"341-270 v. Chr.",field:"Ethik",color:"#7B2D8B",pos:"Hedonismus",tags:["Hedone","Ataraxie","Aponia","Tetrapharmakos"],core:"Lust ist das höchste Gut. Aber wahre Lust ist ruhig - frei von Schmerz und Angst, nicht wilder Genuss.",concepts:["Hedone: Lust als Grundprinzip des guten Lebens","Ataraxie: Seelenruhe als höchste Lust","Aponia: Schmerzfreiheit des Körpers","Kinetische vs. katastematische Lust: Bewegungs- vs. Ruhezustand","Tetrapharmakos: Götter & Tod nicht fürchten"],memo:"Nicht Ausschweifung, sondern Nüchternheit und Freundschaft führen zum wahren Glück.",conns:["Aristoteles (Glück)","Utilitarismus (Lust als Massstab)"]},
  {name:"Die Stoa",dates:"ca. 300 v. Chr. - 200 n. Chr.",field:"Ethik",color:"#5a1e7a",pos:"Stoizismus / Vernunftethik",tags:["Logos","Apatheia","Dichotomie der Kontrolle","Kosmopolitismus"],core:"Nur Tugend ist wirklich gut. Was nicht in meiner Macht steht, soll mich nicht erschüttern.",concepts:["Logos: universelle Vernunft, die alles ordnet","Apatheia: Freiheit von Leidenschaften (nicht: Gleichgültigkeit)","Dichotomie der Kontrolle: nur eigene Gedanken & Handlungen in unserer Macht","Kosmopolitismus: alle Menschen Bürger der Weltgemeinschaft","Vertreter: Zenon, Epiktet, Marc Aurel, Seneca"],memo:"Manche Dinge sind in unserer Macht, andere nicht. (Epiktet)",conns:["Epikur (Ataraxie)","Kant (Pflicht aus Vernunft)"]},
  {name:"Bentham & Mill",dates:"1748-1832 / 1806-1873",field:"Ethik",color:"#8e2494",pos:"Utilitarismus",tags:["Nützlichkeitsprinzip","Konsequentialismus","Hedonic Calculus","Qualität (Mill)"],core:"Eine Handlung ist gut, wenn sie das groeßte Glück der groeßten Zahl bewirkt. Nur Folgen zählen.",concepts:["Utilitaristischer Imperativ: Glück für die groeßte Zahl maximieren","Bentham: quantitativer Utilitarismus - Lust ist messbar","Mill: höhere Lüste (Geist) > niedere Lüste (Körper)","Singer: Präferenzutilitarismus - alle empfindenden Wesen zählen","Konsequentialismus: nur Folgen sind moralisch relevant"],memo:"Es ist besser, ein unzufriedener Sokrates als ein zufriedenes Schwein. (Mill)",conns:["Kant (Gegensatz: Absicht, nicht Folge)","Aristoteles (Glück)"]},
  {name:"Kant (Pflichtethik)",dates:"1724-1804",field:"Ethik",color:"#6a1a90",pos:"Deontologische Ethik",tags:["Kategorischer Imperativ","Pflicht","Guter Wille","Autonomie","Würde"],core:"Handle nur nach der Maxime, die du als allgemeines Gesetz wollen könntest. Pflicht aus Vernunft, nicht Neigung.",concepts:["Kategorischer Imperativ (F1): Universalgesetz - verallgemeinerbar?","Kategorischer Imperativ (F2): Menschheit nie bloss als Mittel behandeln","Guter Wille: einziges unbedingt Gutes","Pflicht: Handeln aus Vernunft, nicht aus Gefühl oder Nutzen","Autonomie: selbst gegebenes Gesetz der Vernunft"],memo:"Handle so, dass du die Menschheit jederzeit zugleich als Zweck, niemals bloss als Mittel brauchst.",conns:["Utilitarismus (Gegensatz)","Aristoteles (Tugend vs. Pflicht)"]},
  {name:"Hans Jonas",dates:"1903-1993",field:"Ethik",color:"#7a2080",pos:"Verantwortungsethik",tags:["Prinzip Verantwortung","Heuristik der Furcht","Zukunftsverantwortung"],core:"Im technologischen Zeitalter trägt der Mensch Verantwortung für zukünftige Generationen. Im Zweifel: Vorsicht.",concepts:["Prinzip Verantwortung: neue Ethik für das technologische Zeitalter","Heuristik der Furcht: beim schlimmsten Szenario ansetzen","Zukunftsverantwortung: auch Ungeborene haben moralische Ansprüche","Kritik am Utilitarismus: Langzeitfolgen nie vollständig berechenbar","Technik verändert den moralischen Rahmen grundlegend"],memo:"Handle so, dass die Wirkungen deiner Handlungen verträglich sind mit der Permanenz echten menschlichen Lebens.",conns:["Kant (Pflicht)","Aristoteles (Verantwortung in Gemeinschaft)"]},
  {name:"Thomas Hobbes",dates:"1588-1679",field:"Staat",color:"#a04000",pos:"Staatsvertrag / Absolutismus",tags:["Leviathan","Naturzustand","bellum omnium","Absolutismus"],core:"Im Naturzustand herrscht Krieg aller gegen alle. Nur ein starker, absoluter Staat sichert dauerhaften Frieden.",concepts:["Naturzustand: bellum omnium contra omnes","Menschen: egoistisch und machtgierig von Natur","Gesellschaftsvertrag: Abgabe aller Rechte an den Souverän","Leviathan: absoluter Staat als starker kuenstlicher Mensch","Souverän steht ueber dem Vertrag - absolute Macht"],memo:"Der Mensch ist dem Menschen ein Wolf - solange kein starker Staat existiert.",conns:["Locke (Widerstandsrecht)","Rousseau (Gegenbild: guter Mensch)"]},
  {name:"John Locke (Staat)",dates:"1632-1704",field:"Staat",color:"#8a3500",pos:"Liberaler Gesellschaftsvertrag",tags:["Naturrechte","Treuheanderschaft","Widerstandsrecht","Gewaltenteilung"],core:"Menschen haben unveraеusserliche Naturrechte. Der Staat ist Treuhаender - verletzt er seine Pflicht, darf man Widerstand leisten.",concepts:["Naturzustand: friedlich, aber unsicher","Naturrechte: Leben, Freiheit, Eigentum - unveraеusserlich","Gesellschaftsvertrag: Staat als Treuhаender, kein absoluter Herrscher","Widerstandsrecht: bei Tyrannei darf das Volk Widerstand leisten","Gewaltenteilung: Legislative und Exekutive getrennt"],memo:"Der Staat dient dem Volk - nicht umgekehrt. Tyrannei berechtigt zum Widerstand.",conns:["Hobbes (Kontrast: Absolutismus)","Rousseau (Gemeinwille)"]},
  {name:"Jean-Jacques Rousseau",dates:"1712-1778",field:"Staat",color:"#B8520A",pos:"Volonte generale",tags:["Volonte generale","Naturmensch","Zivilisation als Verderb","Volkssouveränität"],core:"Der Mensch ist von Natur gut - Gesellschaft verdirbt ihn. Der wahre Staat folgt dem Gemeinwillen.",concepts:["Naturmensch: ursprünglich gut, frei und glücklich","Zivilisation als Verderb: Ungleichheit durch Eigentum entstanden","Volonte generale: Gemeinwille ungleich bloss Mehrheit","Gesellschaftsvertrag: echte Freiheit durch Unterwerfung unter Gemeinwille","Volkssouveränität: kann nicht uebertragen werden"],memo:"Der Mensch wird frei geboren, und ueberall liegt er in Ketten.",conns:["Hobbes (Naturzustand: Gegenbild)","Locke (Liberalismus)"]},
  {name:"Machiavelli / Arendt / Weber",dates:"16.-20. Jh.",field:"Staat",color:"#9e4208",pos:"Machtbegriffe",tags:["Macht als Herrschaft","Macht als Handeln","Legitimität","Gewalt vs. Macht"],core:"Drei grundverschiedene Machtbegriffe: Herrschaft (Machiavelli), kollektives Handeln (Arendt), soziale Relation (Weber).",concepts:["Machiavelli: Macht als Herrschaftsinstrument - pragmatisch","Arendt: Macht = kollektives, gewaltfreies Handeln von Menschen","Weber: Macht = Chance, eigenen Willen auch gegen Widerstand durchzusetzen","Weber: Legitimität - traditionell / charismatisch / legal-rational","Arendt: Gewalt ist das Gegenteil von Macht, nicht ihre Steigerung"],memo:"Arendt: Macht entsteht durch Zusammenhandeln - Gewalt zerstört Macht, ersetzt sie nicht.",conns:["Hobbes (Souverän und Macht)","Locke (Widerstandsrecht)"]},
  {name:"Arnold Gehlen",dates:"1904-1976",field:"Anthro",color:"#1a6e4a",pos:"Mängelwesen",tags:["Mängelwesen","Instinktunsicherheit","Weltoffenheit","Technik als Kompensation"],core:"Der Mensch ist biologisch ein Mängelwesen. Technik ist keine Option, sondern Ueberlebensbedingung.",concepts:["Mängelwesen: kein Instinktsystem, keine biologische Spezialisierung","Instinktunsicherheit: Mensch auf bewusste Entscheidungen angewiesen","Weltoffenheit: muss sich aktiv mit der Welt auseinandersetzen","Technik als Kompensation: ersetzt fehlende Instinkte","Institutionen: stabilisieren die unsichere menschliche Existenz"],memo:"Der Mensch ist das Mängelwesen - erst Technik und Institutionen machen ihn lebensfähig.",conns:["Marx (Arbeit schafft den Menschen)","Jonas (Verantwortung für Technik)"]},
  {name:"Karl Marx",dates:"1818-1883",field:"Anthro",color:"#0e5c3a",pos:"Arbeit & Entfremdung",tags:["Arbeit als Selbsterschaffung","Entfremdung","Species-Wesen","Kapitalismuskritik"],core:"Arbeit ist das Wesen des Menschen. Doch im Kapitalismus entfremdet Lohnarbeit den Menschen von sich selbst.",concepts:["Species-Wesen: Mensch erschafft sich selbst durch bewusste Arbeit","Vier Entfremdungsformen: vom Produkt, Prozess, anderen, sich selbst","Arbeit als Selbsterschaffung: Mensch verwirklicht sich in freier Arbeit","Kapitalismuskritik: Lohnarbeit verhindert freie Selbstentfaltung","Historischer Materialismus: materielle Verhältnisse formen Bewusstsein"],memo:"Im Kapitalismus arbeitet der Mensch nicht für sich - sondern gegen sich selbst.",conns:["Gehlen (Arbeit & Mensch)","Arendt (Arbeit/Herstellen/Handeln)"]},
  {name:"Hannah Arendt (Anthro)",dates:"1906-1975",field:"Anthro",color:"#1a5e3a",pos:"Vita activa",tags:["Arbeit","Herstellen","Handeln","Natalität","Oeffentlicher Raum"],core:"Drei Grundformen: Arbeit (biologisch), Herstellen (dauerhaft), Handeln (politisch frei).",concepts:["Arbeit: biologischer Kreislauf, vergänglich","Herstellen: schafft dauerhafte Gegenstände (Homo faber)","Handeln: einzigartig menschlich - frei, unvorhersehbar, politisch","Natalität: Fähigkeit, etwas Neues in der Welt zu beginnen","Oeffentlicher Raum: notwendige Bedingung für echtes Handeln"],memo:"Nur Handeln ist wirklich frei - es bringt Neues in die Welt, das noch nie dagewesen ist.",conns:["Marx (Arbeit)","Aristoteles (Zoon politikon)"]},
  {name:"Naturrecht vs. Positives Recht",dates:"Antike bis Gegenwart",field:"Staat",color:"#6b3000",pos:"Rechtsphilosophie / Rechts- und Gerechtigkeit",tags:["Naturrecht","Positives Recht","Legalität","Legitimität","Radbruchsche Formel"],core:"Reicht es aus, dass ein Gesetz gueltig ist - oder muss es auch gerecht sein? Naturrecht und positives Recht geben gegensätzliche Antworten.",concepts:["Positives Recht: vom Staat gesetztes, formal gueltiges Recht - gilt weil erlassen","Naturrecht: überzeitliche, universelle Rechte die dem Menschen von Natur zukommen","Legalität: ein Gesetz ist legal, wenn es ordnungsgemaeß erlassen wurde","Legitimität: ein Gesetz ist legitim, wenn es moralisch gerechtfertigt ist","Radbruchsche Formel (Radbruch): positives Recht gilt nicht, wenn es 'unerträglich ungerecht' ist","Rechtspositivismus: Recht gilt unabhängig von Moral - Ziel ist Rechtssicherheit","Thoreau: Pflicht zum zivilen Ungehorsam bei ungerechten Gesetzen","Ziviler Ungehorsam: bewusster, gewaltfreier Gesetzesbruch um auf Unrecht hinzuweisen"],memo:"Es gibt Gesetze, die legal aber unmoralisch sind (z.B. NS-Recht). Es gibt Handlungen, die illegal aber moralisch legitim sind (z.B. Gandhi, Rosa Parks).",conns:["Locke (Widerstandsrecht)","Hobbes (Rechtsgehorsam)","Kant (Moral als Massstab)"]},
  {name:"Sartre & de Beauvoir",dates:"1905-1980 / 1908-1986",field:"Anthro",color:"#0d5030",pos:"Existentialismus",tags:["Existenz vor Essenz","Radikale Freiheit","Mauvaise foi","Genderkonstruktion"],core:"Es gibt keine vorgegebene Natur des Menschen. Freiheit ist unausweichlich - und damit volle Verantwortung.",concepts:["Existenz vor Essenz: kein Wesen ist dem Menschen vorgeschrieben","Radikale Freiheit: immer Wahlmöglichkeit, keine Ausreden","Mauvaise foi: Freiheit durch Rollenspiele verleugnen","de Beauvoir: Man wird nicht als Frau geboren - man wird dazu gemacht","Genderkonstruktion: Rollen kulturell geformt, nicht biologisch"],memo:"Man wird nicht als Frau geboren, man wird dazu gemacht. (Simone de Beauvoir)",conns:["Gehlen (Essentialismus als Gegensatz)","Arendt (Freiheit & Handeln)"]}
];

function buildGrid() {
  var grid = document.getElementById("grid");
  data.forEach(function(ph) {
    var card = document.createElement("div");
    card.className = "card";
    card.setAttribute("data-field", ph.field);
    var tagsHtml = ph.tags.map(function(t){return '<span class="tag">'+t+'</span>';}).join("");
    var conceptsHtml = ph.concepts.map(function(c){return '<li>'+c+'</li>';}).join("");
    var connsHtml = ph.conns.map(function(c){
    return '<span class="conn" onclick="scrollToCard(\'' + c.replace(/'/g, '') + '\')">' + c + '</span>';
  }).join("");
    card.innerHTML =
      '<div class="card-head" style="background:'+ph.color+'">'+
        '<div class="card-dates">'+ph.dates+'</div>'+
        '<div class="card-name">'+ph.name+'</div>'+
        '<div class="card-pos">'+ph.pos+'</div>'+
      '</div>'+
      '<div class="card-body">'+
        '<div class="tags blk">'+tagsHtml+'</div>'+
        '<div class="blk"><div class="blk-label">Kernidee</div><div class="core">'+ph.core+'</div></div>'+
        '<div class="blk"><div class="blk-label">Zentrale Konzepte</div><ul class="clist">'+conceptsHtml+'</ul></div>'+
        '<div class="blk"><div class="blk-label">Merksatz</div><div class="memo">'+ph.memo+'</div></div>'+
        '<div class="blk"><div class="blk-label">Querverbindungen</div><div class="conns">'+connsHtml+'</div></div>'+
      '</div>';
    grid.appendChild(card);
  });
}


function scrollToCard(connText) {
  // Extract name before the first '('
  var targetName = connText.split('(')[0].trim().toLowerCase();
  var cards = document.querySelectorAll('.card');
  var found = null;
  for (var i = 0; i < cards.length; i++) {
    var cardName = cards[i].querySelector('.card-name');
    if (cardName && cardName.textContent.toLowerCase().indexOf(targetName) !== -1) {
      found = cards[i];
      break;
    }
  }
  if (found) {
    // Make sure the card is visible (remove hidden if filtered)
    var wasHidden = found.classList.contains('hidden');
    if (wasHidden) {
      // Switch to "all" filter first
      var allBtn = document.querySelector('button[data-filter="all"]');
      if (allBtn) allBtn.click();
    }
    found.scrollIntoView({ behavior: 'smooth', block: 'center' });
    found.classList.add('highlight');
    setTimeout(function() { found.classList.remove('highlight'); }, 2000);
  }
}

function setupTabs() {
  var tabs = document.querySelectorAll("button.tab");
  for (var i = 0; i < tabs.length; i++) {
    tabs[i].addEventListener("click", function() {
      for (var j = 0; j < tabs.length; j++) { tabs[j].classList.remove("active"); }
      this.classList.add("active");
      var filter = this.getAttribute("data-filter");
      var cards = document.querySelectorAll(".card");
      for (var k = 0; k < cards.length; k++) {
        if (filter === "all" || cards[k].getAttribute("data-field") === filter) {
          cards[k].classList.remove("hidden");
        } else {
          cards[k].classList.add("hidden");
        }
      }
    });
  }
}

buildGrid();
setupTabs();
</script>
</body>
</html>
