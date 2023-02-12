# Sammlung von Competency Questions zum Entwurf von Datenmodellen für Ortsdaten und biographischen Daten in DigiKAR

Die Auswahl an allgemeinen und für die Modellierung von Ortsdaten und biographischen Daten relevanten Competency Questions wird in Beschreibungslisten präsentiert:

- Im ersten Eintrag ist die ursprüngliche User Story aus der Anforderungsanalyse wiedergegeben.
- Im zweiten Eintrag sind die von der User Story abgeleitete Competency Questions aufgelistet.

Eine User Story beschreibt in strukturierter Form Anforderungen an die Datenmodellierung bzw. an das Datenmodell. Eine User Story wird aus Anwenderperspektive formuliert, d.h. aus Sicht einer Historikerin oder eines Historikers, einer Forschungsdatenmanagerin oder eines Forschungsdatenmanagers, einer Kartographin oder eines Kartographen usw.

Die Struktur einer User Story ist wie folgt aufgebaut:

Als **Rolle** möchte ich **Ziel/Wunsch**, um **Nutzen**.

Anders gesagt beantwortet eine User Story die Frage: **wer** will **was** und **warum**?

Competency Questions werden aus einer User Story abgeleitet. Eine Competency Questions ist im Prinzip eine in natürlicher Sprache formulierte Datenbankabfrage. Eine Competency Question beschreibt somit die Anforderungen an die Datenbank bzw. das Datenmodell, d.h. sie formuliert, was eine Datenbankabfrage an Ergebnissen liefern muss, um schließlich die in der zugehörigen User Story formulierte Anforderung zu erfüllen.

## Competency Questions zu allgemeinen Anforderungen

### Forschungsdatenmanagement

<dl>
<dt>User Story</dt>
<dd>[Als Forschungsdatenmanager möchte ich einen Überblick über Forschungsdaten, die aktuell aus historischen Quellen gewonnen werden abfragen, um den Fortschritt der Datenaufbereitung und die Datenqualität einzusehen bzw. zu überwachen.](https://gitlab.rlp.net/digikar/user-stories/-/issues/1)</dd>
<dt>Competency Questions</dt>
<dd>
<ol>
<li>Welche Datensätze gibt es?</li>
<li>Was ist die Quellengrundlage eines Datensatzes?</li>
<li>Aus welchen Dateien besteht ein Datensatz?</li>
<li>In welchen Dateiformaten gibt es die Dateien eines Datensatzes?</li>
<li>Gemäß welchem Datenmodell oder Standard wurden die Daten modelliert?</li>
<ol>
</dd>
</dl>

### Datenbankentwurf und Datenkuration

<dl>
<dt>User Story</dt>
<dd>[Als Historiker will ich eine Datenbank erstellen, die offen bleiben muss, um neue Orte, neue Attribute, neue Zuordnungen zu Attributen ergänzen zu können.](https://gitlab.rlp.net/digikar/user-stories/-/issues/2)</dd>
<dt>Competency Questions</dt>
<dd>
<ol>
<li>Welche Orte befinden sich bereits in der Datenbank?</li>
<li>Welche Klassen und Eigenschaften gibt es in der Datenbank?</li>
<ol>
</dd>
</dl>

<dl>
<dt>User Story</dt>
<dd>[Als Historiker will ich vage Datums- und Zeitangaben modellieren, um relative Datierung zu unterstützen.](https://gitlab.rlp.net/digikar/user-stories/-/issues/9)</dd>
<dt>Competency Questions</dt>
<dd>
<ol>
<li>Was ist der Zeitpunkt nach dem das Ereignis geschehen sein muss (<em>terminus post quem</em>)?</li>
<li>Was ist der Zeitpunkt vor dem das Ereignis geschehen sein muss (<em>terminus ante quem</em>)?</li>
<li>Was ist der frühest mögliche Zeitpunkt (<em>terminus a quo</em>) des Ereignisses?</li>
<li>Was ist der spätest mögliche Zeitpunkt (<em>terminus ad quem</em>) des Ereignisses?</li>
<ol>
</dd>
</dl>

### Datenvalidierung

<dl>
<dt>User Story</dt>
<dd>[Als Historiker oder Informationswissenschaftler will ich Daten automatisch validieren können, um die Datenqualität (Vollständigkeit und Konsistenz der Angaben) zu sichern.](https://gitlab.rlp.net/digikar/user-stories/-/issues/21)</dd>
<dt>Competency Questions</dt>
<dd>
<ol>
<li>Welche Daten sind unvollständig?</li>
<li>Welche Daten sind inkonsistent (verwenden z.B. nicht die vorgesehenen kontrollierten Vokabulare oder verwenden abweichende Datentypen)?</li>
<ol>
</dd>
</dl>

## Competency Questions zu Anforderungen der Modellierung von Ortsdaten

<dl>
<dt>User Story</dt>
<dd>[Als Historiker will ich Daten aus seriellen Quellen erfassen, um Information über raumkonstituierende Eigenschaften von Orten zu sammeln.](https://gitlab.rlp.net/digikar/user-stories/-/issues/3)</dd>
<dt>Competency Questions</dt>
<dd>
<ol>
<li>Aus welcher Quelle stammen die Daten?</li>
<li>Auf welche Zeitspanne beziehen (zeitlicher Bezug) sich die Daten?</li>
<li>Welchen räumlichen Bezug haben die Daten?</li>
<li>Welche Information gibt es über einen bestimmten Ort?</li>
<li>Welche raumkonstitutierenden Eigenschaften wurden erfasst?</li>
<li>Für welche Zeitschnitte gibt es Daten mit den selben, d.h. konsistent erfaßten, raumkonstituierenden Eigenschaften?</li>
<ol>
</dd>
</dl>

<dl>
<dt>User Story</dt>
<dd>[Als Informationswissenschaftler will ich Geodaten zu einem Ort aus verschieden Quellen bzw. Datenbeständen integrieren, um sie für weiterführende Analysen und Visualisierungen abrufbar zu machen.](https://gitlab.rlp.net/digikar/user-stories/-/issues/5)</dd>
<dt>Competency Questions</dt>
<dd>
<ol>
<li>Welche Geodaten gibt es zu einem Territorium?</li>
<li>Gibt es Geodaten zu Territorium X im WKT-Format?</li>
<li>Aus welcher Quellen stammen die Geodaten?</li>
<li>Zu welchen Territorien gibt es mehrere Geodaten aus verschiedenen Quellen?</li>
<ol>
</dd>
</dl>

<dl>
<dt>User Story</dt>
<dd>[Als Historiker will ich einen Ort typisieren bzw. klassifizieren, um ihn entsprechend visualisieren zu können..](https://gitlab.rlp.net/digikar/user-stories/-/issues/8)</dd>
<dt>Competency Questions</dt>
<dd>
<ol>
<li>Welche Art von Entität/Ding ist ein Ort?</li>
<li>Welche Orte sind Siedlungen?</li>
<li>Welche Arten von Siedlungen gibt es unter den Orten?</li>
<li>Welche Orte sind Verwaltungsgebiete/verweltungsgebiete?</li>
<li>Welche Arten von Verwaltungseinheiten (geistlich/weltlich) gibt es unter den Orten?</li>
<ol>
</dd>
</dl>

<dl>
<dt>User Story</dt>
<dd>[Als Historiker will ich die multiple Zugehörigkeiten von Orten erfassen, um diese Information für Visualisierungen zu nutzen.](https://gitlab.rlp.net/digikar/user-stories/-/issues/15)</dd>
<dt>Competency Questions</dt>
<dd>
<ol>
<li>Welche Orte liegen in einem geistlichen Territorium?</li>
<li>Welche Orte liegen in einem weltlichem Territorium?</li>
<li>Welche Orte gehören zu einem geistlichen Territorium?</li>
<li>Welche Orte gehören zu einem weltlichem Territorium?</li>
<li>Welche Ortstypen sind am häufigsten in weltlichen und welche in geistlichen Territorien?</li>
<li>Welche Orte liegen im Gebiet eines Reichsstands (<em>in territorio</em>)?</li>
<li>Welche Orte sind der Gerichtsbarkeit bzw. Landeshoheit eines Reichsstands unterworfen (<em>de territorio</em>)?</li>
<ol>
</dd>
</dl>

<dl>
<dt>User Story</dt>
<dd>[Als Informationswissenschaftler will ich aus historischen Quellen zeitlich begrenzt verwendeten Ortsnamen im Datenmodell erfassen können, um ein historisches Ortsnamensverzeichnis mit entsprechender Information aufzubauen.](https://gitlab.rlp.net/digikar/user-stories/-/issues/17)</dd>
<dt>Competency Questions</dt>
<dd>
<ol>
<li>Seit wann ist der Ortsname in Gebrauch?</li>
<li>Von wann bis wann war der Ortsname in Gebrauch?</li>
<li>Vom wem wurde der Ortsname eingeführt?</li>
<li>Wo oder vom wem war der Ortsname in Gebrauch?</li>
<ol>
</dd>
</dl>

<dl>
<dt>User Story</dt>
<dd>[Als Kartographin will ich grundlegende Geoinformation bzw. ortsbasierte Information zu allen erfassten Orten visualisieren, um dadurch einen Überblick über den Raum zu bekommen.](https://gitlab.rlp.net/digikar/user-stories/-/issues/22)</dd>
<dt>Competency Questions</dt>
<dd>
<ol>
<li>Zu welchen Orten liegen Punktkoordinaten vor?</li>
<li>Zu welchen Orten liegen Geodaten (Polygone etc.) vor?</li>
<li>Zu welchen weltlichen oder geistlichen Verwaltungseinheiten gehören die Orte?</li>
<li>Welche Ortsnamen sind zu den Orten erfasst?</li>
<ol>
</dd>
</dl>

## Competency Questions zu Anforderungen der Modellierung von biographischen Daten

<dl>
<dt>User Story</dt>
<dd>[Als Historiker will ich Verwandschaftsbeziehungen und soziale Beziehungen zwischen Personen erfassen erfassen und in den Daten abbilden, um etwa die Karriereverläufe von Amtsträgern aufgrund ihrer Herkunft und persönlichen bzw. beruflichen Netzwerke zu analysieren.](https://gitlab.rlp.net/digikar/user-stories/-/issues/4)</dd>
<dt>Competency Questions</dt>
<dd>
<ol>
<li>Welche Rolle spielte eine Person in einer sozialen Beziehung?</li>
<li>Welche Rolle spielte eine Person in einer beruflichen Tätigkeit?</li>
<ol>
</dd>
</dl>

<dl>
<dt>User Story</dt>
<dd>[Als Historiker möchte ich die Vernetzung von Personen darstellen, um die Lebenswege der in verschiedenen sozialen Beziehungen stehenden Personen zu analysieren.](https://gitlab.rlp.net/digikar/user-stories/-/issues/20)</dd>
<dt>Competency Questions</dt>
<dd>
<ol>
<li>Welche unterschiedliche Arten von Vernetzungen (familiäre, Eltern-Kind, Eltern-Schwiegerkind, Enkel-Großvater) können unterscheiden werden?</li>
<li>Welche Personen stehen dabei im Fokus ('Person of Interest' (PoI))?</li>
<li>Welche Lebenswege (Karrierestationen, konkrete Aufenthalts- wie auch Bezugsorte/Dienstherren und Ämter) haben die Söhne, Schwiegersöhne, Väter und Großeltern zurückgelegt?</li>
<li>Wen heirateten die Töchter?</li>
<li>Wie viele unterschiedliche Wirkungsorte/Bezugsorte hatte eine poi (= Wie relevant ist Mobilität im Lebensverlauf gewesen)?</li>
<li>Zu welchen Orten steht eine Person aufgrund einer bestimmten sozialen Beziehung (Verwandtschaft, Bekanntschaft, frühere Kollegenschaft) zu einem bestimmten Zeitpunkt in Beziehung (betrifft die dann zum Zeitpunkt aktuellen Orte der Beziehungspersonen)?</li>
<ol>
</dd>
</dl>

