---
title: Příslib objednávky
description: Tento článek poskytuje informace o příslibech objednávky. Příslib objednávky pomáhá spolehlivě přislíbit odběratelům data dodání a poskytuje vám flexibilitu, se kterou můžete tato data dodržet.
author: Henrikan
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesATP, SalesAvailableDlvDates, SalesCarrier
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c835e25348b937c1dd68d8fa45b0264bd6815c23
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228259"
---
# <a name="order-promising"></a>Příslib objednávky

[!include [banner](../includes/banner.md)]

Tento článek poskytuje informace o příslibech objednávky. Příslib objednávky pomáhá spolehlivě přislíbit odběratelům data dodání a poskytuje vám flexibilitu, se kterou můžete tato data dodržet.

Při příslibu objednávky se na základě metody řízení data dodání a počtu přepravních dnů vypočítá nejdřívější datum expedice a příjmu. Vybírat lze z následujících čtyř metod řízení data dodání:

- **Doba realizace prodeje** – doba realizace prodeje je doba mezi vytvořením prodejní objednávky a expedici položek. Výpočet data dodání je založen na výchozím počtu dnů a nezohledňuje skladovou dostupnost, známou poptávku ani plánovanou dodávku.
- **ATP (lze slíbit)**  – ATP je množství položky, které je k dispozici a může být odběrateli slíbeno k určitému datu. Výpočet množství ATP zahrnuje nepotvrzené zásoby, doby realizace, plánované příjmy a výdeje.
- **ATP + rezerva výdeje** – datum expedice odpovídá datu ATP navýšenému o rezervu výdeje pro položku. Rezerva výdeje je doba potřebná k přípravě položek na expedici.
- **CTP (příslib na základě ověření dostupné kapacity)**– dostupnost se počítá pomocí rozpadu. Pokud používáte optimalizaci plánování, metoda kontroly data dodání *CTP* není povolena, a pokud je vybrána, způsobí při spuštění výpočtu chybu. Další informace o způsobu nastavení a použití funkcí CTP získáte v části [Výpočet datum dodání prodejní objednávky pomocí CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).
- **CTP pro optimalizaci plánování** – Použijte výpočet CTP, který poskytuje Optimalizace plánování. Tato možnost nemá žádný efekt, pokud používáte integrovaný hlavní plánovací modul. Další informace o způsobu nastavení a použití funkcí CTP získáte v části [Výpočet datum dodání prodejní objednávky pomocí CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).

> [!NOTE]
> Když je prodejní objednávka aktualizována, informace o příslibu objednávky se aktualizují pouze v případě, že nelze splnit stávající datum slibné objednávky, jak je znázorněno v následujících příkladech:
>
> - **Příklad 1**: Aktuální datum příslibu objednávky je 20. července, ale kvůli zvýšenému množství ji budete moci doručit až 25. července. Protože již nelze splnit aktuální datum, spustí se příslib objednávky.
> - **Příklad 2**: Aktuální datum příslibu objednávky je 20. července, ale díky sníženému množství ji budete moci už až 15. července. Protože však aktuální datum lze stále splnit, příslib objednávky se nespustí a 20. červenec zůstává datem příslibu objednávky.

## <a name="atp-calculations"></a>Výpočty hodnoty ATP

Množství ATP se vypočítává pomocí metody „kumulativní hodnota ATP s dopředným vyhledáváním“. Hlavní výhodou této metody výpočtu hodnoty ATP je, že pomocí ní lze zpracovat případy, kdy součet výdejů mezi příjmy je větší než poslední příjem (například když je ke splnění požadavku nutné použít množství z předchozího příjmu). Metoda výpočtu „kumulativní hodnota ATP s dopředným vyhledáváním“ zahrnuje všechny výdeje až do té doby, než kumulativní množství k příjmu překročí kumulativní množství k vydání. Tato metoda výpočtu hodnoty ATP tedy vyhodnocuje, zda lze některé z množství z předchozího časového období použít v pozdějším období.

Množství ATP je nepřislíbený zůstatek zásob v prvním období. Obvykle se počítá pro každé období, ve kterém je plánován příjem. Dobu ATP program počítá ve dnech a aktuální datum přitom počítá jako první den pro množství ATP. V prvním období zahrnuje množství ATP zásobu na skladě, od níž jsou odečteny objednávky odběratelů, které jsou v termínu nebo po termínu.

Výpočet ATP vzniká pomocí následujícího vzorce:

ATP = ATP předchozího období + příjmy aktuálního období - výdeje aktuálního období – čisté vydané množství pro každé budoucí období až do období, kdy součet příjmů pro pro všechna budoucí období (včetně budoucího období) je větší než součet výdejů (včetně budoucího období).

Všimněte si, že výpočet ATP neobsahuje informace okolo data vypršení platnosti a mimo ochrannou dobu ATP, kterou systém očekává, když může být přislíbeno libovolné množství.

Pokud neexistují další výdeje nebo příjmy, které lze vzít v úvahu, je množství ATP v dalších dnech stejné jako poslední vypočítané množství ATP.

Nejsou-li při kontrole hodnoty ATP dokončeny všechny dimenze pro položku, mohou být i přesto zadány na výdejích nebo příjmech. V takovém případě musí být při výpočtu hodnoty ATP kvůli snížení počtu řádků příjmu a výdeje, které jsou použity při výpočtu hodnoty ATP, přičteny příjmy a výdeje ke stávajícím dimenzím.

Zobrazené množství ATP je vždy větší než nebo rovno 0 (nule). Pokud výpočet vrátí záporné množství ATP (například když dříve přislíbené množství překročí dostupné množství), množství je automaticky nastaveno na hodnotu 0.

### <a name="example"></a>Příklad

Pole **ATP – zpětná ochranná doba poptávky** řídí to, jak daleko zpět v čase se mají hledat zpožděné objednávky poptávky nebo skladové výdeje. Pole **ATP – zpětná ochranná doba dodávky** řídí to, jak daleko zpět v čase se mají hledat zpožděné objednávky dodávky nebo skladové příjmy. Pokud mají být při výpočtu hodnoty ATP například zohledněny objednávky, které jsou zpožděny pouze o sedm dní, musí být obě pole nastavena na hodnotu **7**.

Pole **ATP – čas kompenzace zpožděné poptávky** a **ATP – čas posunu zpožděné dodávky** řídí to, kdy mají být při výpočtu hodnoty ATP zahrnuty zpožděné poptávky nebo dodávky. Pokud mají být při výpočtu hodnoty ATP pozítří například zohledněny zpožděné dodávky a poptávky, musí být obě pole nastavena na hodnotu **2**. Hodnota **2** znamená, že množství položek na zpožděné nákupní objednávce, která by měla být zahrnutá ve výpočtu hodnoty ATP, se zobrazí jako dostupné dva dny po aktuálním datu.

V následujícím příkladu je do polí **ATP – zpětná ochranná doba poptávky** a **ATP – zpětná ochranná doba dodávky** zadána hodnota **7** a do polí **ATP – čas kompenzace zpožděné poptávky** a **ATP – čas posunu zpožděné dodávky** zadána hodnota **1**.

Nákupní objednávka na 200 kusů produktu, která měla být přijata před třemi dny, nebyla dosud přijata. Řádek prodejní objednávky pro 75 kusů stejného produktu, který měl být expedován včera, proto ještě nebyl expedován.

Odběratel zavolá a chce si objednat 150 kusů stejného produktu. Při ověřování dostupnosti produktu zjistíte, že další nákupní objednávka na 100 kusů produktu bude doručena o 10 dní později.

Vytvořte řádek prodejní objednávky pro daný produkt a jak množství zadejte hodnotu **150**.

Vzhledem k tomu, že metoda řízení data dodání je ATP, vypočítají se data ATP, aby se našlo nejbližší možné datum expedice. Na základě nastavení je zohledněna zpožděná nákupní objednávka a prodejní objednávka a výsledné množství ATP pro aktuální datum je 0. Zítra, kdy je očekáváno přijetí zpožděné nákupní objednávky, se množství ATP vypočítá jako větší než 0 (v tomto případě bude mít hodnotu 125). Nicméně za 10 dní od dneška, kdy je očekáváno přijetí další nákupní objednávky na 100 kusů, bude množství ATP větší než 150.

Proto je datum expedice na základě výpočtu hodnoty ATP nastaveno na 10 dní od tohoto okamžiku. Odběrateli tedy můžete sdělit, že požadované množství lze dodat za 10 dní od tohoto okamžiku.

## <a name="ctp-calculations"></a>Výpočty hodnoty CTP

Funkce CTP vám umožňuje poskytnout zákazníkům realistická data, kdy můžete slíbit konkrétní zboží. Pro každý prodejní řádek můžete zadat datum, které zohledňuje existující skladové zásoby, výrobní kapacitu a přepravní časy.

CTP rozšiřuje funkci ATP s ohledem na informace o kapacitě. Zatímco ATP bere v úvahu pouze dostupnost materiálu a předpokládá nekonečné kapacitní zdroje, CTP zvažuje dostupnost materiálů i kapacity. Poskytuje tedy realističtější obrázek o tom, zda lze poptávku uspokojit v daném časovém rámci.

CTP se chová trochu odlišně na základě toho, který modul plánování používáte (optimalizace plánování, nebo integrovaný modul). CTP pro optimalizaci plánování aktuálně podporuje pouze podmnožinu scénářů CTP, které jsou podporovány vestavěným modulem.

Podrobné informace o způsobu nastavení a použití funkcí CTP pro jednotlivé moduly získáte v části [Výpočet datum dodání prodejní objednávky pomocí CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
