**Chris Garbers**
  [vor 3 Tagen](https://dst-csp.slack.com/archives/C99LGLS2H/p1682342153501429)
Frage an POs und Scrum Master in der Softwareentwicklung: macht ihr “Bug-Fixing Sprints”, kurz vor einem pending Release (werden nicht geplant, Bugs adhoc behoben)? Wenn ja, warum? Wenn nicht, warum nicht? (Wir machen das nicht, versuchen Bugs zu planen wie Stories, habe das aber mal in 1-2 anderen Firmen gesehen)




6 Antworten


![](T9ACL5Y22-UB63W01H7-124a3d0666a3-72.jpg)

**Viktoria Heep**
  [vor 3 Tagen](https://dst-csp.slack.com/archives/C99LGLS2H/p1682344278690169?thread_ts=1682342153.501429&cid=C99LGLS2H)
Wenn bei uns ein Bug auftaucht - fliegt er direkt im Sprint ins Backlog und wird mit der Argumentation "Defects gehen vor" auch direkt mit abgearbeitet.
Zum Teil deshalb weil es bei uns kritische Arbeitsstruktur ist zum anderen auch um eine Anwachsen weiterer Bugs aus diesem zu verhindern.




![](T9ACL5Y22-U049CKA6MRD-3dfa6ec9683e-72.jpg)

**Adrian Wildermuth**
  [vor 3 Tagen](https://dst-csp.slack.com/archives/C99LGLS2H/p1682353461992869?thread_ts=1682342153.501429&cid=C99LGLS2H)
Bugs werden bei uns wie Stories behandelt und kommen in's Backlog. Der/die PO priorisiert diese dann wie Stories ein. Mit dem Ziel keine grössere Bugwelle entstehen zu lassen.




![](T9ACL5Y22-U027S2NP4M7-15bf9bca7c0f-72.jpg)

**Domenica 'Nica' Krebs**
  [vor 2 Tagen](https://dst-csp.slack.com/archives/C99LGLS2H/p1682409221843579?thread_ts=1682342153.501429&cid=C99LGLS2H)
Bei uns werden Bugs als Tickets aufgenommen und analysiert, aber nicht geschätzt. Der PO bestimmt durch Prio im Backlog, wie wichtig ihr/ihm der Fix ist. Für gewöhnlich landen ca. 2 Bugfix-Tickets in einem Sprint.




![](T9ACL5Y22-U05306KD8GZ-gc3c07592d59-72.png)

**Chris Garbers**
  [vor 2 Tagen](https://dst-csp.slack.com/archives/C99LGLS2H/p1682409296144309?thread_ts=1682342153.501429&cid=C99LGLS2H)
Vielen Dank für euer Feedback




![](T9ACL5Y22-U04R1DLMTN1-455dd8f6afd7-72.jpg)

**Philipp Drescher**
  [vor 2 Tagen](https://dst-csp.slack.com/archives/C99LGLS2H/p1682414504682749?thread_ts=1682342153.501429&cid=C99LGLS2H)
Also normalerweise werden bei uns bugs wenn sie aufkommen sofort gefixed. Natürlich gibt es unbedeutendere Fehler, die man gerne nach hinten schiebt, vor allem wenn man gerade kurz vor einem großen Featurerelease steht.
Bei mir kam es sehr gut an, sich 2-3 Tage für diese Fehler Zeit zu nehmen (Haben an Tag 1 uns alle getroffen und zusammen Pizza gegessen, um nochmal alle Bugs durchzugehen, danach wurde sich ans fixen gemacht 

![](1f609@2x.png)

 )
Pizza hilft immer (bearbeitet) 

![](T9ACL5Y22-UD8GTFS95-fdc61eaaf4ae-72.jpg)

**Frank Sattler**
  [vor 24 Stunden](https://dst-csp.slack.com/archives/C99LGLS2H/p1682519359521299?thread_ts=1682342153.501429&cid=C99LGLS2H)
Ich habe es noch nie gesehen, dass reine „Bug Fixing“ Sprints gemacht werden. Bugs wurden in bis dato allen meinen Projekten im entsprechenden Tool (z.B. JIRA, VersionOne, Azure DevOps) entsprechend aufgenommen.
Wenn es sich um einen Bug der Kategorie „Showstopper / schwer / rot“ gehandelt hat, haben wir das Thema spätestens im nächsten Daily kurz thematisiert und von da aus die nächsten Schritte initiiert.
Da ich bis dato fast nur in mittleren bis großen Projekten mit Drei-Wochen-Sprints gearbeitet habe, haben wir dann in den beiden wöchentlichen Refinements die Bugs der anderen Kategorien kurz angerissen und eingestuft. Das haben wir als Prozeß fortlaufend gemacht, um hier die bereits zitierte Bugwelle zu vermeiden. Wird der Ruf nach „Bug Fixing Sprints“ laut, wäre das für mich ein Zeichen, dass es ein Problem mit dem Qualitätsverständnis und / oder der „Definition of Done“ gibt. Hat das Testen einen entsprechenden Stellenwert? Wie stellt ihr Code Qualität sicher? Und und und…