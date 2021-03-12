---
title: Kontrola stavu periferních zařízení a služeb POS
description: V tomto tématu je uveden přehled operace kontroly stavu v pokladním místě (POS).
author: rubendel
manager: AnnBe
ms.date: 03/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 59e2505345d82f47efebfba6cc6f3403d03acc84
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000527"
---
# <a name="health-check-for-pos-peripherals-and-services"></a>Kontrola stavu periferních zařízení a služeb POS

[!include [banner](includes/banner.md)]

Tohle téma popisuje operaci kontroly stavu v pokladním místě (POS).

## <a name="overview"></a>Přehled

Maloobchody mohou být složitými prostředími, ve kterých se používá mnoho aplikací a zařízení. Při rostoucím počtu operací může být obtížné zajistit, aby operace probíhaly svižně, protože závisí například na periferních zařízeních, která se mohou během dne porouchat nebo mohou být odpojena. Řešení problémů, které souvisejí se zařízeními a službami, může být nákladné pro větší obchodníky a zároveň frustrující pro menší provozy.

Řešení Microsoft Dynamics 365 Commerce verze 10.0.10 a novější zahrnují operaci kontroly stavu, která vám může pomoci zabránit některým z těchto nákladů a frustraci. Tato operace poskytuje metodu pro testování zařízení přímo z POS mimo normální provoz. Proto může maloobchodníkovi pomoci při zjišťování problémů dříve, než k nim dojde.

## <a name="key-terms"></a>Klíčové podmínky

| Termín | popis |
|---|---|
| Periferní zařízení | Jakékoli zařízení, které aplikace POS používá pro usnadnění transakcí a dalších operací v obchodě. Jedná se například o zásuvky s hotovostí, snímače čárových kódů a platební terminály. |
| Služby | V tomto tématu je služba pomocnou aplikací, na níž aplikace POS závisí, aby prováděla transakce a každodenní operace. Jako příklady uveďme aplikace, které pomáhají při výpočtech daní nebo expedičních nákladů. |

## <a name="health-check-operation"></a>Operace kontroly stavu

Operace kontroly stavu je operace 717 na stránce **Operace POS** v Commerce Headquarters. Lze ji použít, když je POS v režimu bez zásuvky. Hardwarová stanice však musí být aktivní.

Ve výchozím nastavení testuje kontrola stavu pouze zařízení konfigurovaná v hardwarovém profilu pro hardwarovou stanici, která je aktuálně aktivní pro registrační pokladnu. Pokud registrační pokladna využívá více hardwarových stanic v průběhu jednoho dne, musí se vždy připojit pouze k jedné hardwarové stanici. Neexistuje kontrola stavu na úrovni obchodu. Tento typ kontroly však může probíhat prostřednictvím rozšířených funkcí serveru Commerce.

### <a name="out-of-box-health-checks"></a>Přednastavené kontroly stavu

| Typ | Spojení | Podrobnosti |
|---|---|---|
| Tiskárna | OPOS | Tato kontrola testuje základní funkce propojení a vkládání objektů pro funkce POS (OPOS). Několik příkladů:<ul><li>Otevření: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Uzavření: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| Řádkový displej | OPOS | Tato kontrola testuje základní funkce OPOS. Několik příkladů:<ul><li>Otevření: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Uzavření: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| Duální displej | Windows | Tato kontrola zajišťuje, že operační systém rozpozná druhý displej systému Windows. | 
| MSR | OPOS | Tato kontrola testuje základní funkce OPOS. Několik příkladů:<ul><li>Otevření: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Uzavření: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| Výstavce | OPOS | Tato kontrola testuje základní funkce OPOS. Několik příkladů:<ul><li>Otevření: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Uzavření: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> | 
| Skener | OPOS | Tato kontrola testuje základní funkce OPOS. Několik příkladů:<ul><li>Otevření: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Uzavření: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> | 
| Rozsah | OPOS | Tato kontrola testuje základní funkce OPOS. Několik příkladů:<ul><li>Otevření: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Uzavření: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| Klávesnice pro kód PIN | OPOS | Tato kontrola testuje základní funkce OPOS. Několik příkladů:<ul><li>Otevření: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Uzavření: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| Platební terminál | Sada SDK plateb | Tato kontrola provede test základních funkcí platebních terminálů poskytnutých sadou SDK pro platby. <ul><li>Uzamknout</li><li>BeginTransaction</li><li>EndTransaction</li><li>ReleaseDevice</li><li>Zavřít</li></ul> |

### <a name="using-the-health-check-operation-in-the-pos"></a>Použití operace kontroly stavu v POS

Je-li operace kontroly stavu zahájena v POS, v podokně vpravo se zobrazí seznam konfigurovaných zařízení a stav jednotlivých zařízení. Chcete-li provést kontrolu stavu jednoho zařízení, vyberte zařízení a pak vyberte volbu **Testovat vybrané**. Chcete-li provést kontrolu stavu pro všechna zařízení, vyberte možnost **Testovat vše**. Funkce **Testovat vše** testují všechna zařízení po jednom a aktualizují stav každého zařízení ve sloupci **Stav**.

Sloupec **Poslední kontrola** ukazuje, kdy byla u každého zařízení naposledy provedena kontrola stavu.

Pokud zařízení projde kontrolou stavu (tj. nedojde-li k chybám), bude stav zařízení **OK**. Pokud se kontrola stavu nezdaří, ze stavu bude zřejmé, že došlo k chybě. V tomto případě podokno na pravé straně poskytuje podrobné informace, které se týkají chyby, nebo dává uživateli pokyny, aby se obrátil na správce systému.

U některých zařízení, jako je například zámek OPOS, neexistují přednastavené testy kontroly. Není-li pro některé použité zařízení detekován test kontroly stavu, stav bude **Nepodporováno**.

### <a name="extending-health-checks"></a>Rozšíření kontroly stavu

Přednastavené testy kontroly stavu jsou nakonfigurovány tak, aby pro typické chyby poskytovaly srozumitelné zprávy. Nejsou však zahrnuty všechny scénáře. Prostřednictvím rozšiřitelnosti mohou obchodníci namapovat zprávy srozumitelné uživateli na chyby, které mohou být specifické pro jejich prostředí.

Vlastní kontroly stavu lze rovněž vytvořit, pokud chcete testovat zařízení, která nejsou předem podporována výrobcem, nebo testovat libovolné služby, na nichž závisí POS.

## <a name="related-articles"></a>Související články

[Spouštěče Modern POS (MPOS) a tisk](dev-itpro/pos-trigger-printing.md)
