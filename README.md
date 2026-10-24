# Tokentakarékos munkavégzés

Újrahasználható AI-skill a felesleges kontextus és az ismételt modellmunka csökkentésére, a kért eredmény, részletesség és szükséges ellenőrzések megőrzésével.

A skill nem állítja át a modellt, a gondolkodási beállítást vagy a szolgáltatót. Nem tartalmaz API-kapcsolatot, háttérfolyamatot vagy ütemezést.

## Mit csinál

- Újrahasználja a még érvényes eredményeket.
- Célzott keresést és elegendő környezet beolvasását írja elő.
- Ismétlődő mechanikus munkához meglévő programokat részesít előnyben.
- Kerüli a megismételt elemzést és az indokolatlan újraellenőrzést.
- Megőrzi a szükséges kutatást, frissességet, bizonyítékot és ellenőrzést.
- Egyszerű kérdéshez nem indít külön optimalizálási kört.

Nincs garantált megtakarítási százalék. A skill betöltése is használ tokeneket; a tényleges hatást azonos célú és azonos minőségi követelményű feladatok teljes szolgáltatói tokenadataival lehet összehasonlítani.

## Letöltés

- [Önálló skill ZIP](dist/token-takarek-skill-1.0.0.zip?raw=true)
- [ChatGPT-kompatibilis plugin ZIP](dist/token-takarek-plugin-1.0.0.zip?raw=true)
- [SHA-256 ellenőrzőösszegek](dist/SHA256SUMS)

## Codex

Másold a [skills/token-takarek](skills/token-takarek) mappát a saját `~/.agents/skills/` könyvtáradba vagy a projekt `.agents/skills/` mappájába.

Explicit meghívás:

```text
$token-takarek

Végezd el a feladatot a kért minőség és szükséges ellenőrzések megtartásával.
```

Az automatikus kiválasztás engedélyezett; a készség leírásához illő többfájlos, többlépéses és ismétlődő feladatoknál használható. Minden jövőbeli feladat automatikus kiválasztása nem garantált.

## Claude Code

Ugyanezt a skillmappát másold a saját `~/.claude/skills/` vagy a projekt `.claude/skills/` mappájába.

Explicit meghívás:

```text
/token-takarek
```

A Claude alkalmazásban a támogatott fiókoknál az önálló skill ZIP tölthető fel a Skills felületen.

## ChatGPT

A támogatott felületen válaszd a saját plugin archívumának feltöltését, és add meg a plugin ZIP-et. Telepítés után a készség az `@` menüből választható ki.

A helyi skillmappa önmagában nem kerül át automatikusan a webes vagy felhős fiókba. Az elérhetőség a fióktól, felülettől és futtatókörnyezettől függ.

## Állandó alapelv

A [BASELINE-INSTRUCTIONS.hu.txt](BASELINE-INSTRUCTIONS.hu.txt) egy rövid, opcionális alaputasítás. A meglévő személyes vagy projektutasítások mellé illeszthető; azokat ne cseréld le vele. Egyszerű kérdésnél az alapelv alkalmazható a teljes skill külön betöltése nélkül.

## Ellenőrzési állapot

A megosztott skill megegyezik a korábban helyben validált változattal. A csomagolásnál a fájlegyezést, a YAML- és JSON-adatokat, a ZIP-ek CRC-jét és a SHA-256 ellenőrzőösszegeket vizsgáltuk.

Ez nem minden környezetre szóló viselkedési teszt, nem általános minőségazonossági bizonyíték, és nem mért tokenmegtakarítás.

## Dokumentáció

- [OpenAI: skillek készítése](https://learn.chatgpt.com/docs/build-skills)
- [OpenAI: plugin csomagolása](https://developers.openai.com/plugins/build/plugins)
- [Anthropic: skillek használata](https://support.claude.com/en/articles/12512180-use-skills-in-claude)
