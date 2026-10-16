# Ukemi Listening Test (Study 2) — deploy

Ίδια διαδικασία με το ερωτηματολόγιο, αλλά με ΝΕΟ Google Sheet και ΝΕΟ repo,
για να μη μπερδευτούν τα δεδομένα των δύο μελετών.

1. Νέο Google Sheet: «Ukemi Study 2 responses». Αντέγραψε το ID από το link
   (docs.google.com/spreadsheets/d/ΑΥΤΟ/edit).
2. Extensions → Apps Script → επικόλληση του Code.gs → βάλε το ID στη γραμμή SHEET_ID → Save.
3. Run → doGet (για να δώσεις άδεια). Deploy → New deployment → Web app → Anyone → Deploy.
   Αντέγραψε το URL που τελειώνει σε /exec.
4. index.html → βάλε το URL στη γραμμή SUBMIT_URL.
5. Νέο repo στο GitHub (π.χ. ukemi-listening-test) → upload index.html → Settings → Pages → main.

Ρυθμίσεις στην αρχή του script του index.html:
- VERSION: "s2-pilot" για το pilot, άλλαξέ το σε "s2-v1" όταν παγώσεις την έκδοση.
- CONDITIONS: βγάλε το "m7" για 4 συνθήκες (το Code.gs το υποστηρίζει ήδη).

Στο Sheet: μία γραμμή ανά συμμετέχοντα, με ανά στρατηγική d′, criterion, ακρίβεια
τεστ, αναγνώριση λάθους, εκμάθηση (πρώτες/τελευταίες 4 δοκιμές), χρόνο απόκρισης,
βαθμολογίες και κατάταξη, και όλες τις δοκιμές στη στήλη trials_json για ανάλυση
σε επίπεδο δοκιμής.
