---
title: Sestavy výdajů v nové podobě
description: Toto téma obsahuje informace o přepracovaném a upraveném rozhraní pro zadávání sestavy výdajů v Microsoft Dynamics 365 for Finance and Operations. Nové rozhraní zjednodušuje proces dokončování sestav výdajů a snižuje požadovaný čas.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 9e87a61bd6dd7bc1c7ef569882daf2074c7cade9
ms.sourcegitcommit: 672c94704e9a2b0ec7ee3c111d4ceb1bb8597969
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/14/2019
ms.locfileid: "1631948"
---
# <a name="expense-reports-reimagined"></a>Sestavy výdajů v nové podobě

[!include[banner](../includes/banner.md)]

Zadávání sestavy výdajů bylo přepracováno za účelem zjednodušení procesu dokončení sestav výdajů a snížení požadovaného času. Zde jsou uvedeny hlavní komponenty nového rozhraní výdajů:

- Nový pracovní prostor správy výdajů, který vám umožňuje přístup k výdajům delegáta.
- Nová zkušenost s párováním účtenek pro lepší zobrazení účtenek na úrovni záhlaví a zjednodušení procesu připojení účtenek k řádkům výdajů
- Nová mřížka pouze pro čtení, která umožňuje zobrazit mnoho dalších řádků výdajů a další sloupce s daty. Nyní můžete zobrazit všechny rozepsané a rozdělené řádky spolu se svými nadřazenými výdaji.
- Zjednodušené podokno pro úpravy výdajů.
- Přepracování zpráv o chybách, upozorněních a zásadách, které vám pomohou zaručit, že máte správný kontext pro pochopení toho, jaký je problém a jak jej vyřešit. Společnost Microsoft odebrala mnoho zpráv, které se objevovaly předtím, než uživatelé mohli dokončit své úkoly a vyřešit problémy, jako je například nedokončená zpráva o rozpisu.
- Nová stránka pro určení polí vyžadovaných vaší organizací, volitelných polí a polí, která by neměla být zaznamenána. Na této stránce lze omezit počet polí, která musí uživatelé nastavit.
- Nový vzhled sestav výdajů, takže sestavy se již nejeví jako navržené pro osoby z účetního oddělení.

Chcete-li nové rozhraní zapnout, použijte pracovní prostor **Správa funkcí** a zapněte funkci **Sestavy výdajů v nové podobě**. Pokud tuto funkci zapnete, dojde k následujícím akcím:

- Existující pracovní prostor výdajů je nahrazen novým pracovním prostorem.
- Bude přidána nová položka nabídky pro viditelnost pole výdajů.
- Nejsou odebrány žádné položky nabídky pro sestavy výdajů (existující stránka) nebo pole sestavy výdajů.
- Pracovní postupy a jakákoliv schválení vás stále zavedou na existující stránku sestav výdajů.

## <a name="getting-started-video-for-new-users"></a>Začínáme s videem pro nové uživatele

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE2Y7gO]

Video [Rozhraní výdajů v aplikaci Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (zobrazené výše) je zahrnut do [playlistu Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), který je k dispozici na YouTube.

## <a name="new-features"></a>Nové funkce

| Nová funkce | Popis |
|---|----|
| Viditelnost pole výdajů | Nová stránka nastavení umožňuje určit, jaká pole by měla být pro organizaci zakázána, jaká pole mají být vyžadována a jaká pole se doporučují. |
| Požadovaná pole | Nová jednoduchá konfigurace umožňuje nastavit některá pole jako povinná, aniž by bylo nutné používat strukturu zásad. |
| Volitelná pole | Bude přidána druhá stránka pro volitelná pole. Tímto způsobem se zaměstnanci nebudou cítit tak, jako by si museli nastavit pole, ale pole jsou stále snadno dostupná. |
| Přidání nepřipojených účtenek | Možnost přidat nepřipojené účtenky do sestavy výdajů je viditelná z pracovního prostoru a na sestavě výdajů. |
| Vylepšené zasílání zpráv | Existují lepší přehled o řádcích výdajů, které obsahují upozornění nebo chyby. |
| Snížení počtu zpráv na panelu zpráv| Počet zpráv informačního protokolu byl snížen a bylo provedeno úsilí k zamezení zobrazení duplicitních zpráv v mnoha případech. |
| Seskupené společné akce | Rozhraní bylo vyčištěno pomocí přidání nového tlačítka akcí pro většinu akcí společných na úrovni řádku a přidání tlačítka se třemi tečkami (...) pro záhlaví a další méně časté akce. |
| Nový pracovní prostor ke zvýšení viditelnosti | Nový pracovní prostor sjednocuje funkce a odkazy, které umožňují uživatelům přesun do různých oblastí. |
| Přidání existujících výdajů a účtenek během vytváření výdajů | Při vytváření sestav výdajů můžete přidat všechny nebo vybrané výdaje a účtenky. |
| Kalkulačka směnných kurzů | Byla přidána kalkulačka kurzů, která umožňuje vypočítat směnný kurz pro kapesní transakce s více měnami. |
| Uložení a přidání nových řádků výdajů | Tlačítka **Uložit** a **Nový** jsou dispozici při zadání nových výdajů, aby vám pomohla rychle zadat řádky výdajů. |
| Lepší viditelnost rozdělených a rozepsaných řádků | Rozepsané a rozdělené řádky jsou přidány přímo do seznamu výdajů ke zvýšení viditelnosti a umožňují snadno určit, zda existují chyby zásad nebo jiné chyby. |
| Zobrazení účtenek během rozpisu | Účtenky lze zobrazit během rozpisu. |

Počáteční verze se zaměřuje na scénáře zadávání výdajů. Všechny scénáře kontroly nebo schválení sestavy výdajů budou nadále používat stávající stránku pro zadávání výdajů.

Následující funkce se nacházejí na existující stránce, ale dosud se nenacházejí na nové stránce. Tyto funkce budou znovu zahrnuty během následujících několika vydání:

- Schválení
- Schválení závazků a možnost upravovat účetnictví
- Body vícero zadání
- Integrace cestovních žádanek
- Datová entita pro viditelnost pole výdajů
- Zadání pro výdaje denních diet
- Workflow na úrovni řádku
- Podpora prozatímního schvalovatele
- Rozšířený rozpis
