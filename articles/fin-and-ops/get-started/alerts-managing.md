---
title: Dávkové zpracování výstrah
description: Toto téma poskytuje informace o dávkovém zpracování výstrah v Microsoft Dynamics 365 for Finance and Operations.
author: tjvass
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 482cf30b4f82e8801ebc12e3925c1efb09f7eb1e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "341918"
---
# <a name="batch-processing-of-alerts"></a>Dávkové zpracování výstrah

[!include [banner](../includes/banner.md)]

Výstrahy jsou v aplikaci Microsoft Dynamics 365 for Finance and Operations zpracovávány pomocí funkce dávkového zpracování. Než mohou být výstrahy doručeny, musíte nastavit dávkové zpracování.

Finance and Operations podporuje dva typy událostí:

- Události, které byly vyvolány událostmi založenými na změně. Tyto události jsou označovány jako události vytvoření/odstranění a aktualizace.
- Události spouštěné podle dat splatnosti.

Dávkové zpracování lze nastavit pro každý typ událostí.
        
## <a name="batch-processing-for-change-based-events"></a>Dávkové zpracování událostí založených na změně

Finance and Operations načítá všechny události založené na změně, které se vyskytly od posledního spuštění dávkového zpracování. Události založené na změně zahrnují aktualizace polí, odstranění záznamů a vytváření záznamů. Tyto události jsou porovnány s podmínkami nastavenými v pravidlech výstrah. Když událost odpovídá podmínkám v pravidlu, dávkové zpracování vygeneruje výstrahu.

### <a name="frequency-for-change-based-events"></a>Četnost dávek pro události založené na změně

Úlohu dávky, která spustí zpracování události, lze pro události založené na změně nastavit brzy po zaznamenání události systémem. Pokud nastavíte dávkovou úlohu na opakování častěji, uživatelé dostanou své výstrahy dříve po provedení změn. Vysoká četnost dávkového zpracování však může nepříznivě ovlivnit výkonnost systému.

Na druhé straně dávková úloha, která se vrací méně často a která je naplánována pro situace, kdy je nízké zatížení systému, může zvýšit výkon systému. Nízká frekvence provádění dávkového zpracování však nemusí splňovat požadavky uživatelů na aktuální výstrahy.

Při nastavování četnosti dávkového zpracování pro události založené na změně tedy dbejte na rovnováhu mezi včasností výstrah a výkonem celého systému. Čím více je uživatelů, kteří vytvářejí pravidla výstrah, tím důležitější jsou tato hlediska. Četnost nemá žádný vliv na počet událostí, které je nutné zpracovat. Pokud však pravidla vytváří více uživatelů, je nutné provést další kontroly. Tento typ výměny dat může ovlivnit výkonnost systému.

#### <a name="the-risks-of-low-batch-frequency"></a>Rizika nízké četnosti dávek

Pokud nastavíte dávkové zpracování s nízkou četností pro události založené na změnách, může dojít ke ztrátě výstrah, protože data důležitá pro podmínky pravidel výstrah se změní před zpracováním dávky. Může tedy dojít ke ztrátě výstrah.

Může například existovat pravidlo výstrahy, které je nastaveno tak, že spustí výstrahu za předpokladu, že událostí je **změna kontaktní adresy zákazníka** a podmínkou je **zákazník = BB**. Jinak řečeno, pokud se kontakt odběratele pro BB zákazníka změní, zaznamená se událost. Systém dávkového zpracování je však nastaven tak, aby dávkové zpracování bylo méně časté než zadávání dat. Pokud se jméno zákazníka změní z **BB** na **AA** předtím, než se událost zpracuje, data v databázi neodpovídají podmínce pravidla, **zákazník = BB**. Proto když je nakonec událost zpracována, nevygeneruje se žádná výstraha.

### <a name="set-up-processing-for-change-based-alerts"></a>Nastavení zpracování výstrahy na základě změny

1. Přejděte na **Správa systému** &gt; **Pravidelné úlohy** &gt; **Výstrahy** &gt; **Výstrahy založené na změně**.
2. V dialogovém okně **Výstrahy založené na změně** zadejte příslušné informace.

## <a name="batch-processing-for-due-date-events"></a>Dávkové zpracování pro události termínu splnění

Finance and Operations rozpozná všechny události způsobené termíny plnění a tyto události jsou porovnány s podmínkami nastavenými v pravidlech výstrah. Pokud událost odpovídá podmínkám v pravidlu, dávkové zpracování vygeneruje výstrahu.

### <a name="frequency-for-due-date-events"></a>Četnost dávek pro události termínu splnění

V případě událostí termínu splnění je vhodné nastavit úlohy dávky, které budou vykonávány v noci nebo v určeném čase během dne, aby se vyrovnalo zatížení systému. Doporučujeme nastavit dávkovou úlohu tak, aby se spouštěla alespoň jednou denně. Pokud mají být výstrahy zasílány co nejdříve, nastavte dávkové zpracování, aby se provedlo okamžitě po změně systémového data. Pokud chcete generovat výstrahy pro události termínu splnění, ke kterým dojde poté, co dávka termínu splnění zpracovala výstrahy, můžete dávku spustit týž den ještě jednou.

Na určitý den byla spuštěna například dávková úloha. Poté vytvoříte nákupní objednávku s datem splnění, které má spustit výstrahu ve stejný den. Chcete-li dostat výstrahu v tento den, musíte spustit dávkovou úlohu znovu po vytvoření nákupní objednávky. Pokud ale v daném dni dávkovou úlohu znovu nespustíte, následující dávka dne převezme všechny nezpracované události z předchozích dní.

> [!NOTE]
> I když se dávkové zpracování provádí více než jednou denně, výstrahy se pro tutéž událost a podmínky termínu splnění neduplikují. Výstrahy jsou generovány pouze pro data, která se na základě změn vzniklých v systému po provedení minulé dávky stala termíny splnění.

### <a name="batch-processing-window"></a>Okno dávkového zpracování

Zpracování pravidel výstrah ve společnosti může být zastaveno z několika důvodů. Tyto důvody zahrnují prázdniny, chyby systému nebo jiné problémy, které brání po určitou dobu spuštění dávkové úlohy.

Pokud chcete zabránit, aby výstrahy data platnosti zastarala, vzhledem k tomu, že dávková úloha nebyla spuštěna několik dní, můžete nastavit okno dávkového zpracování. Okno dávkového zpracování lze použít, aby se zabránilo spouštění dávkové úlohy po zadaný počet dní.

Pokud nastavíte okno dávkového zpracování, odešle se výstraha po zpracování pravidla výstrahy, přestože výstraha překročí časový limit určený v kritériích data splatnosti. Výstrahy jsou odesílány tak dlouho, dokud nebude překročeno období, které je definováno podle této lhůty plus okno dávkového zpracování. Výstrahy se přestanou odesílat, až bude překročeno období, které je definováno podle této lhůty plus okno dávkového zpracování.

### <a name="set-up-processing-for-due-date-alerts"></a>Nastavení zpracování výstrahy na datum splatnosti

1. Přejděte na **Správa systému** &gt; **Pravidelné úlohy** &gt; **Výstrahy** &gt; **Výstrahy založené na datu plnění**.
2. V dialogovém okně **Výstrahy data plnění** zadejte příslušné informace.
