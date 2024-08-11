# NLP Analyst Recommendation Project
Dieses Projekt analysiert den Einfluss der Unternehmenskommunikation auf das Verhalten von Finanzanalysten unter Verwendung von NLP-Techniken wie Sentimentanalyse und Topic Modeling. Die Fallstudie konzentriert sich auf Pressemitteilungen der Siemens AG und die dazugehörigen Analystenempfehlungen.  
Ziel dieses Projekts ist es, zu untersuchen, wie von Unternehmen kommunizierte Themen von Analysten aufgegriffen werden und welchen Einfluss diese Themen auf das Sentiment der Analysten haben. Die gewonnenen Erkenntnisse können genutzt werden, um zukünftige Kommunikationsstrategien von Unternehmen zu verbessern.  

## Vorgehensweise
1. **Datenbeschaffung**  
   Zuerst wurden die benötigten Daten mithilfe eines Web-Crawlers (der Begriff wird hier synonym zu <u>Web-Scraper</u> verwendet) gesammelt. Der Crawler (`Crawler.ipynb`) wurde verwendet, um Analystenempfehlungen von einer Webseite zu extrahieren. Die gesammelten Daten wurden in der Datei `Analystenempfehlungen.xlsx` gespeichert. Eine Vorstufe des Crawling-Prozesses, bei der nur die Links zu den Analystenempfehlungen gesammelt wurden, ist in der Datei `Analystenempfehlungen_Links.xlsx` dokumentiert.

2. **Datenvorverarbeitung**  
   Nach der Datenerfassung wurden die Analystenempfehlungen aufbereitet. Dazu gehörte die Konvertierung von Zeitstempeln, die Bereinigung von Texten sowie das Entfernen von Stoppwörtern. Für das Topic Modeling der Analystenempfehlungen (Iteration 2) wurde zusätzlich eine benutzerdefinierte Stoppwortliste erstellt und in der Datei `Stoppwörter` abgelegt.

3. **Sentimentanalyse**  
   In diesem Schritt wurde das Sentiment der Analystenempfehlungen mithilfe des German FinBERT-Modells analysiert. Der Code zur Durchführung der Sentimentanalyse befindet sich im Notebook `Analysten_Sentimentanalyse_TopicModelling.ipynb`.

4. **Topic Modeling**  
   Parallel zur Sentimentanalyse wurde ein Topic Modeling durchgeführt, um die Hauptthemen in den Analystenempfehlungen und der Pressemitteilung zu identifizieren. Der Prozess wurde in zwei Teilen ausgeführt:  
   - `Analysten_Sentimentanalyse_TopicModelling.ipynb`: Enthält das Topic Modeling der Analystenempfehlungen.
   - `Pressemitteilung_TopicModelling.ipynb`: Beinhaltet das Topic Modeling der Pressemitteilung der Siemens AG.

5. **Ergebnisse und Interpretation**  
   Die Ergebnisse aus der Sentimentanalyse und dem Topic Modeling wurden analysiert und interpretiert, um zu verstehen, wie die Kommunikationsthemen der Siemens AG von Analysten aufgenommen wurden und welchen Einfluss sie auf das Sentiment hatten. Die Ergebnisse können verwendet werden, um die zukünftige Kommunikationsstrategie von Unternehmen zu verbessern.

## Übersicht
**/ :**  
< └── **Ergebnis Crawler :** beinhaltet das Ergebnis des Web-Crawlers (die gecrawlten Analystenempfehlungen).  
 < < ├── **Analystenempfehlungen.xlsx :** Die gecrawlten Analystenempfehlungen mit Zeitstempeln.  
  < < ├── **Analystenempfehlungen_Links.xlsx :** Links zu den gecrawlten Analystenempfehlungen (Vorstufe im Crawling-Prozess).  
< └── **Pressemitteilung :** beinhaltet die Pressemitteilung der Siemens AG vom 16.11.2023.   
< ├── **Stoppwörter :** beinhaltet die benutzerdefinierten Stoppwörter für Iteration 2 des Topic Modelings der Analystenempfehlungen.    
< ├── **Analysten_Sentimentanalyse_TopicModeling.ipynb :** Sentimentanalyse und Topic Modeling der Analystenempfehlungen.  
< ├── **Crawler.ipynb :** Crawler für die Analystenempfehlungen.   
< └── **Pressemitteilung_TopicModeling.ipynb :** Topic Modeling der Pressemitteilung.  

## Autor
Paul Moosmayer