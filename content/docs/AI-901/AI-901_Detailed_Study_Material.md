---
title: Részletes Tananyag
weight: 1
---
# 📘 AI-901: Azure AI Fundamentals Részletes Tananyag

## 1. Modul: Mesterséges Intelligencia Alapfogalmak (AI Fundamentals)

Az MI célja az emberi képességek szimulálása szoftverek segítségével.

### Alapvető munkaterhelések (AI Workloads)
*   **Machine Learning (Gépi tanulás):** Minden MI alapja. Olyan algoritmusok, amelyek adatokból tanulnak, és predikciókat (jóslatokat) készítenek.
*   **Computer Vision (Számítógépes látás):** Képi információk feldolgozása.
    *   *Image Classification:* Mi van a képen?
    *   *Object Detection:* Hol van a tárgy a képen? (Bounding box-ok használata).
    *   *Optical Character Recognition (OCR):* Szöveg kinyerése képekből.
*   **Natural Language Processing (NLP):** Szöveges és beszélt nyelv értelmezése.
    *   *Sentiment Analysis:* Pozitív vagy negatív a szöveg hangvétele?
    *   *Entity Recognition:* Nevek, dátumok, helyszínek azonosítása.
*   **Speech (Beszédfeldolgozás):**
    *   *Speech-to-Text (STT):* Diktálás, leiratozás.
    *   *Text-to-Speech (TTS):* Felolvasás.
*   **Generative AI (Generatív MI):** Új adatok (szöveg, kép, hang) létrehozása meglévő minták alapján.

---

## 2. Modul: Felelősségteljes MI (Responsible AI)

A Microsoft 6 alapelve, amely a etikus MI fejlesztést irányítja. **Ez a vizsga egyik legfontosabb része!**

1.  **Fairness (Méltányosság):** Az MI nem diszkriminálhat nem, kor, rassz vagy egyéb csoportszempont alapján (pl. egy hitelbíráló rendszer ne legyen elfogult).
2.  **Reliability & Safety (Megbízhatóság és biztonság):** A rendszernek hiba nélkül kell működnie váratlan helyzetekben is (pl. önvezető autó).
3.  **Privacy & Security (Adatvédelem és biztonság):** A személyes adatok védelme és a rendszer ellenállóképessége a támadásokkal szemben.
4.  **Inclusiveness (Befogadás):** Mindenki számára elérhető megoldások (pl. képernyőolvasó látássérülteknek).
5.  **Transparency (Átláthatóság):** A felhasználónak értenie kell, miért hozott az MI egy adott döntést.
6.  **Accountability (Elszámoltathatóság):** Mindig van egy emberi felelőse a rendszernek.

---

## 3. Modul: Gépi Tanulás (Machine Learning) alapok

### Hogyan működik?
*   **Features (Jellemzők):** A bemeneti adatok (pl. ház mérete, szobák száma). Jelölése általában: **X**.
*   **Label (Címke):** Amit meg akarunk jósolni (pl. a ház ára). Jelölése általában: **y**.

### ML Típusok
1.  **Regression (Regresszió):** Folytonos számértéket jósolunk (pl. hőmérséklet, részvényárfolyam).
2.  **Classification (Osztályozás):** Kategóriákat jósolunk.
    *   *Binary:* Igen/Nem (pl. spam-e az email?).
    *   *Multiclass:* Több kategória (pl. kutya, macska vagy madár?).
3.  **Clustering (Klaszterezés):** Felügyelet nélküli tanulás (Unsupervised). Hasonló adatpontok csoportosítása címkék nélkül (pl. ügyfélszegmentáció).

### Tanítási folyamat (Lifecycle)
1.  **Data Ingestion:** Adatok begyűjtése.
2.  **Data Preparation:** Tisztítás, hiányzó értékek pótlása.
3.  **Train & Validate:** Modell tanítása és ellenőrzése.
4.  **Model Deployment:** A modell közzététele végpontként (Endpoint).

---

## 4. Modul: Generatív MI és Large Language Models (LLM)

### Mi az az LLM?
Hatalmas szövegmennyiségen tanított neurális hálózatok, amelyek képesek megérteni az emberi nyelvet.
*   **Tokenization (Tokenizálás):** A modell nem szavakat, hanem "tokeneket" (szórészleteket) lát.
*   **Transformers:** Az architektúra, ami lehetővé teszi a szövegrészek közötti összefüggések (Attention) megértését.

### Prompt Engineering (Prompt tervezés)
*   **Prompt:** Az utasítás, amit az MI-nek adunk.
*   **Zero-shot learning:** Példa nélkül adunk feladatot.
*   **Few-shot learning:** Néhány példát is adunk a promptban a várt formátumról.
*   **System Message:** A modell viselkedésének, stílusának alapvető meghatározása (pl. "Te egy szakmai segéd vagy").

### Fontos fogalmak
*   **Hallucination (Hallucináció):** Amikor az MI magabiztosan állít valótlanságot.
*   **Grounding (Horgonyzás):** A modell válaszainak valós adatokhoz kötése (pl. egy dokumentum alapján válaszoljon).
*   **Temperature (Hőmérséklet):** A válasz kreativitásának szabályozása (0 = precíz, 1 = kreatív).

---

## 5. Modul: Azure MI Megoldások

### Szolgáltatások csoportosítása
*   **Azure Machine Learning (AML):** Adattudósoknak. Saját modellek építése, Python kódok futtatása.
*   **Azure AI Services (korábban Cognitive Services):** Fejlesztőknek. Kész modellek API-n keresztül.
    *   *Azure AI Vision*
    *   *Azure AI Language*
    *   *Azure AI Speech*
*   **Azure OpenAI Service:** Enterprise szintű hozzáférés a GPT, DALL-E modellekhez, beépített biztonsági szűrőkkel (Content Filtering).
*   **Azure Content Understanding:** Kifejezetten dokumentumokból, videókból való információ-kinyerésre (Layout, Key-value pairs).

### Új fogalom az AI-901-ben: AI Agents (Ágensek)
*   Olyan rendszerek, amelyek képesek önállóan tervezni és eszközöket (pl. keresőt, számológépet) használni egy komplex cél elérése érdekében.
*   **Microsoft Foundry:** Az a környezet, ahol ezeket az ágenseket és modelleket menedzselhetjük.

---

## Vizsgafelkészülési Tippek
1.  **Tudd a különbséget:** Regresszió (szám) vs. Osztályozás (kategória).
2.  **Felelősségteljes MI:** Mindenképpen tanuld meg a 6 alapelv nevét és jelentését.
3.  **Azure Portál:** Ismerd fel a szolgáltatások ikonjait és nevét.
4.  **JSON ismeret:** Tudd értelmezni egy API válaszát (pl. hol van benne a `confidence score` vagy a `label`).
