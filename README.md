### README für Discourse Connector Vergleich

#### Überblick

Mein Ansatz war, mithilfe eines kleinen Programms die Häufigkeit von Diskursmarkern ("discourse connectives") in Artikeln zu zählen, die durch das ChatGPT zugrundliegenden Sprachmodell vervollständigt wurden und diese mit dem Origialartikel zu vergleichen. Ziel war es, den Stil von ChatGPT mit dem von menschlichen Autor:innen abzugleichen, insbesondere in Bezug auf die Verwendung dieser Diskursmarker.

#### Anforderungen

- Python 3.x
- OpenAI Python-Paket und API-Key
- Ein TSV-Korpus mit Artikeln (abgelegt im data/ Ordner)

#### Verwendung

1. Installieren Sie das OpenAI-Paket: `pip3 install openai`.
2. Legen Sie Ihren OpenAI API-Schlüssel in der Variable `api_key` fest.
3. Führen Sie das Programm mit dem Pfad zum TSV-Korpus als Argument aus: `python script.py pfad/zum/korpus.tsv`.

#### Optionen

- `--anzahl_artikel`: Anzahl der zu vergleichenden Artikel (Standard: 10).

---

### Einschätzung des Outputs

Der Output zeigt, dass die durchschnittliche Anzahl von Diskursverbindern in den Artikeln bei 26,1 liegt, während sie im Text von ChatGPT bei 24,6 liegt. Obgleich diese Zahlen sehr ähnlich sind, fiel bei der wiederholten Ausführung des Programms auf, dass ChatGPT generell pro Artikel mindestens einen Diskursmarker weniger (normalisiert über min. 10 Artikel) verwendet als die ursprünglichen Autor:innen der Artikel. Zu beachten ist desweiteren, dass aufgrund des Aufbaus meines Programms in den verglichenen Texten in beiden Fällen die ersten zehn Sätze aus dem originalen Artikel entnommen sind, was die Ergebnisse verfälscht (im Sinne dessen, dass ein teilweise erheblicher Teil der Artikel exakt gleich ist / die relative Anzahl hingegen gleicht sich im Vergleich aus). 

Dies könnte bedeuten, dass ChatGPT nicht gleich gut wie menschliche Journalist:innen darin ist, die Struktur und den Fluss von Argumentation stilistisch auszugestalten. Es könnte jedoch auch spezifische Unterschiede geben, die eine detailliertere Analyse erfordern, wie z.B. die Art der verwendeten Diskursmarker oder die Kontexte, in denen sie verwendet werden.
