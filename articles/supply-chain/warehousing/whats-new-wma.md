---
title: Co je nového nebo změněného v mobilní aplikaci Warehouse Management
description: Toto téma uvádí nové a změněné funkce pro každou vydanou verzi mobilní aplikace Warehouse Management pro Microsoft Dynamics 365 Supply Chain Management.
author: ivanv-microsoft
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 6d98cea29f4c25319caed6680966f61c660778f0
ms.sourcegitcommit: 3d05bb2a423fe130700686ff73daa355d15b0e09
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386092"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a>Co je nového nebo změněného v mobilní aplikaci Warehouse Management

[!include [banner](../includes/banner.md)]

Toto téma uvádí nové funkce, opravy, vylepšení a známé problémy pro každou vydanou verzi mobilní aplikace Warehouse Management pro Microsoft Dynamics 365 Supply Chain Management.

## <a name="version-2090"></a>Verze 2.0.9.0

Tato verze řeší problém, kdy aplikace mohla přestat reagovat, pokud se uživatelé dostanou na začátek seznamu.

## <a name="version-2080"></a>Verze 2.0.8.0

Tato verze představuje následující nové funkce, opravy a vylepšení:

- Přidána podpora pro [funkce krokových pokynů](mobile-app-titles-instructions.md), která byla představena v Supply Chain Management verze 10.0.21.
- Přidána animace nápovědy, která uživatelům ukazuje, že překrytí mohou zavírat přejetím dolů.
- Přidána podpora pro funkční klávesy v seznamech akcí a nabídkách. Uživatelé mohou podržením libovolné funkční klávesy po dobu tří sekund získat seznam dostupných příkazů.
- Opravený problém, který způsoboval, že se na některých zařízeních zobrazovala následující chybová zpráva: „Nelze najít vhodné zobrazení pro zadanou velikost.“
- Opraven problém, kdy režim celé obrazovky nefungoval vždy, když byla použita klávesnice na obrazovce.
- Opravený problém, kdy přejíždění stránky nefungovalo na zařízeních Windows.
- Byly opraveny různé problémy, které způsobily, že systém přestal reagovat.

## <a name="version-2070"></a>Verze 2.0.7.0

### <a name="new-features-fixes-and-improvements-in-version-2070"></a>Nové funkce, opravy a vylepšení ve verzi 2.0.7.0

- Přidána část do stránky **O aplikaci**, která kontroluje nejnovější vydanou verzi aplikace.
- Usnadňuje pohyb mezi stránkami.
- Změněna ikona tlačítka řazení vzestupně/sestupně v pracovním seznamu.
- Zkrácené marže na kartě **Podrobnosti**, aby se do ní vešlo více informací.
- Byla použita různá vylepšení výkonu, aby se aplikace v průběhu času nezpomalovala.
- Pokud je na obrazovce více ovládacích prvků, než kolik se tam vejde, což má za následek nutnost stránkování, ovládací prvek číselníku se již neposouvá stejným způsobem jako stránka.
- Upřednostňuje se zobrazení poslední naskenované hodnoty před zobrazením názvu úkolu, takže pokud se překrývají, bude název úkolu zkrácen.
- Byly opraveny různé problémy, které způsobily, že systém přestal reagovat.
- Text na různých místech již není v některých jazycích oříznut.
- Aplikace nyní běží ve výchozím nastavení v režimu celé obrazovky.
- Byl opraven problém, který občas způsoboval ignorování skenů na hlavní stránce u určitých zařízení.

### <a name="known-issues-in-version-2070"></a>Známé problémy ve verzi 2.0.7.0

- Na některých zařízeních se při spuštění aplikace nebo zahájení úkolu zobrazí následující chybová zpráva: „Nelze najít vhodné zobrazení pro zadanou velikost.“ Pokud se vám tato chybová zpráva zobrazí na kterémkoli z vašich zařízení, musíte na tomto zařízení downgradovat mobilní aplikaci Warehouse Management na verzi 2.0.6.0 a počkat na upgrade, dokud nebude vydána další verze aplikace.

## <a name="version-2060"></a>Verze 2.0.6.0

### <a name="new-features-fixes-and-improvements-in-version-2060"></a>Nové funkce, opravy a vylepšení ve verzi 2.0.6.0

Tato verze představuje následující nové funkce, opravy a vylepšení:

- Ukázkový režim nyní zobrazuje všechny štítky v jazyce zařízení.
- Je méně pravděpodobné, že se zobrazí následující chybová zpráva: „Nelze najít vhodné zobrazení pro zadanou velikost.“
- Minimální výška pro pracovní karty byla zvýšena (pro případy, kdy jsou v pracovním seznamu nakonfigurována tři nebo méně polí).
- Okraje (vyblednutí) ve spodní části karet podrobností byly vylepšeny.
- S neplatnými symboly v souborech XML, které jsou vyměňovány se serverem, se nyní pracuje elegantně. (Například netisknutelné znaky jsou nyní řešeny elegantně a již nezpůsobují, že aplikace přestane reagovat.)
- Chyby HTTP (například „chyba 503“), když je odeslán požadavek serveru, jsou nyní řešeny elegantně.
- Během zobrazování chyby se seznam možností pro ovládací prvky se seznamem již automaticky nezobrazuje.
- Aplikace již nepřestává reagovat kvůli orientaci displeje, která je vybrána v uživatelském nastavení.
- Obrázky produktů se nyní zobrazují v samoobslužných prostředích. (Tato změna se týká pouze verzí s nízkým rozlišením. Služba správy souborů nepodporuje obrázky v plné velikosti v samoobslužných prostředích.)
- Problém, který zahrnoval krátké výběry nulového množství, byl opraven.
- Aplikace již nepřestane reagovat, když se na kartě podrobností zobrazí více identických polí.

### <a name="known-issues-in-version-2060"></a>Známé problémy ve verzi 2.0.6.0

V této verzi existují následující známé problémy:

- Aplikace (zejména pracovní seznam) se časem zpomalí.
- **Verze pro Windows:** Pokud se pro skenování v systému Windows používá pistole USB, nekonzistentní výsledky způsobí, že budou naskenované symboly smíchány.

## <a name="version-2050"></a>Verze 2.0.5.0

Tato verze představuje následující nové funkce, opravy a vylepšení:

- Tajný kód klienta již není v nastavení připojení skryt.
- Nyní můžete dlouhým stisknutím libovolného textu zobrazit celý text.
- Chybová zpráva, když chybí oprávnění úložiště, byla vylepšena.
- Pro některé toky byly přidány nové kontrolní sekvence.
- Tlačítko Odeslat již není nesprávně dostupné kvůli velikosti okna.
- Posuvníky nyní mohou pokračovat na menších obrazovkách, když se použijí větší velikosti tlačítek.
- Překrytí čtyřmi tlačítky již není oříznuto.
- Klávesnice nyní podporuje tlačítko mazání.
- Byl vyřešen problém s jasem, ke kterému mohlo dojít při stisknutí klávesnice.
- Byly opraveny různé problémy s demo daty.
- Problém, který ovlivnil číselná pole na stránce podrobností, byl opraven.
- Na některých zařízeních již klávesnice na obrazovce občas nezmizí.
- Byly opraveny různé chyby uživatelského rozhraní (UI), například chyby, které ovlivnily barvu pozadí a umístění.
- Vylepšeno uživatelské rozhraní v ruštině.
- Byly opraveny různé problémy, které způsobily, že systém přestal reagovat.
- Problém související s opětovným otevřením kalkulačky byl opraven.
- **Verze Android:** Problém, který způsobil, že Android 4.4 přestal reagovat při spuštění, byl opraven.
- **Verze Android:** Minimální měřítko bylo sníženo na 50 procent.

## <a name="version-2040"></a>Verze 2.0.4.0

Verze 2.0.4.0 byla první obecně dostupnou verzí mobilní aplikace Warehouse Management.

### <a name="new-features-fixes-and-improvements-in-version-2040"></a>Nové funkce, opravy a vylepšení ve verzi 2.0.4.0

Tato verze zavádí následující nové funkce, opravy a vylepšení, které nebyly k dispozici ve verzi náhledu:

- Pokud karta s podrobnostmi obsahuje dva štítky, které mají stejná data, jeden z štítků je skrytý.
- Ve výchozím nastavení se nyní zobrazují speciální znaky a možnost jejich skrytí byla z uživatelského nastavení odstraněna.
- Zakázaná tlačítka pro odeslání se nyní zobrazují jako nedostupná v kompaktním pohledu z ruky.
- Změna logiky sekvenování pro ovládací prvky zajišťuje plynulejší škálování napříč zařízeními. Proto není nutné upravovat měřítko písem nebo tlačítek.
- Výchozí barevný motiv byl změněn na *Tmavý*.
- V zobrazení pásu karet byla přidána chybějící ikona pro deaktivované tlačítko Odeslat.
- Výjimky vypršení časového limitu vás nyní místo zobrazení in-line chyby přenesou na stránku připojení.
- Pokud není k dispozici žádná akce pro odeslání (např **OK**, **Ano**, **Akceptovat**, **Hotovo** nebo **Dokončeno**), tlačítko Odeslat bude deaktivováno.
- Byla vylepšena stabilita aplikace.
- Je opravena chyba zabezpečení [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).
- **Verze pro Windows:** Problém ve Windows, kdy nabídky nereagovaly po změně velikosti okna, byl opraven.

### <a name="known-issue-in-version-2040"></a>Známý problém ve verzi 2.0.4.0

V této verzi existuje následující známý problém:

- Tato verze má problém se zařízeními, která používají Android 4.4. Při používání aplikace s touto verzí Android se mohou vyskytnout problémy.
