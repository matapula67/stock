# Kitchen Stock (Stock ya Jikoni)

Web app ya kurecord stock na kutrack mauzo ya jikoni kwa wauzaji wa vyakula na vinywaji.

## Vipengele
- Register / Sign in (kila mtumiaji ana sheet yake)
- Sheet yenye columns: date, item, open, in, total, sales, closing, system, debt
- Hesabu automatic: `total = open + in`, `closing = total - sales`
- Save sheet (Hifadhi Zangu): fungua, pakua CSV, futa
- Ripoti ya bidhaa iliyouzika zaidi/kidogo kwa siku, wiki na mwezi, na mapendekezo
- Download sheet (CSV) na download report (PDF)
- Lugha: Kiswahili / English, Mode: dark / light

## Muundo wa folder
```
kitchen-stock/
├── index.html   # app nzima (HTML + CSS + JS)
├── README.md
├── .gitignore
└── .nojekyll
```
Hakuna build wala `npm install`. PDF inatumia jsPDF kutoka cdnjs (inahitaji internet).

## Kuiendesha kwenye kompyuta
Fungua `index.html` kwenye browser, au:
```bash
npx serve .
```

## Kuweka kwenye GitHub
1. Tengeneza repo mpya kwenye github.com (mfano `kitchen-stock`), bila README.
2. Kwenye folder hili:
```bash
git init
git add .
git commit -m "Initial commit: Kitchen Stock app"
git branch -M main
git remote add origin https://github.com/USERNAME/kitchen-stock.git
git push -u origin main
```
(badilisha `USERNAME` na jina lako la GitHub)

## Deploy
**GitHub Pages (bure, rahisi zaidi)**
Repo → Settings → Pages → Source: *Deploy from a branch* → Branch: `main` / `(root)` → Save.
Baada ya dakika 1-2 site itapatikana: `https://USERNAME.github.io/kitchen-stock/`

**Netlify**: netlify.com → Add new site → Import from Git (chagua repo). Build command acha wazi, Publish directory: `.`

**Vercel**: vercel.com → Add New Project → chagua repo → Framework: *Other* → Deploy.

## Kumbuka (kikwazo cha sasa)
Akaunti na data vinahifadhiwa kwenye browser ya kila kifaa (localStorage). Mtumiaji hataona data yake kwenye kifaa kingine, na nenosiri halina usalama wa server.
Ili iwe ya matumizi halisi kwa wauzaji wengi, hatua inayofuata ni backend (Node/Express + database, au Supabase/Firebase) kwa auth na cloud storage.
