---
title: "Příslib objednávky"
description: "Tento článek poskytuje informace o příslibech objednávky. Příslib objednávky pomáhá spolehlivě přislíbit odběratelům data dodání a poskytuje vám flexibilitu, se kterou můžete tato data dodržet."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesATP, SalesAvailableDlvDates
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2c0b31f6e51de4489a35dbd91a6e9886e620f421
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="order-promising"></a>Příslib objednávky

[!include[banner](../includes/banner.md)]


Tento článek poskytuje informace o příslibech objednávky. Příslib objednávky pomáhá spolehlivě přislíbit odběratelům data dodání a poskytuje vám flexibilitu, se kterou můžete tato data dodržet.

Při příslibu objednávky se na základě metody řízení data dodání a počtu přepravních dnů vypočítá nejdřívější datum expedice a příjmu. Vybírat lze ze čtyř metod řízení data dodání:

-   **Doba realizace prodeje** – doba realizace prodeje je doba mezi vytvořením prodejní objednávky a expedici položek. Výpočet data dodání je založen na výchozím počtu dnů a nezohledňuje skladovou dostupnost, známou poptávku ani plánovanou dodávku.
-   **ATP (lze slíbit)** – ATP je množství položky, které je k dispozici a může být odběrateli slíbeno k určitému datu. Výpočet množství ATP zahrnuje nepotvrzené zásoby, doby realizace, plánované příjmy a výdeje.
-   **ATP + rezerva výdeje**– datum expedice odpovídá datu ATP navýšenému o rezervu výdeje pro položku. Rezerva výdeje je doba potřebná k přípravě položek na expedici.
-   **CTP (příslib na základě ověření dostupné kapacity)**– dostupnost se počítá pomocí rozpadu.

## <a name="atp-calculations"></a>Výpočty hodnoty ATP
Množství ATP se vypočítává pomocí metody „kumulativní hodnota ATP s dopředným vyhledáváním“. Hlavní výhodou této metody výpočtu hodnoty ATP je, že pomocí ní lze zpracovat případy, kdy součet výdejů mezi příjmy je větší než poslední příjem (například když je ke splnění požadavku nutné použít množství z předchozího příjmu). Metoda výpočtu „kumulativní hodnota ATP s dopředným vyhledáváním“ zahrnuje všechny výdeje až do té doby, než kumulativní množství k příjmu překročí kumulativní množství k vydání. Tato metoda výpočtu hodnoty ATP tedy vyhodnocuje, zda lze některé z množství z předchozího časového období použít v pozdějším období.  

Množství ATP je nepřislíbený zůstatek zásob v prvním období. Obvykle se počítá pro každé období, ve kterém je plánován příjem. Dobu ATP program počítá ve dnech a aktuální datum přitom počítá jako první den pro množství ATP. V prvním období zahrnuje množství ATP zásobu na skladě, od níž jsou odečteny objednávky odběratelů, které jsou v termínu nebo po termínu.  

Výpočet ATP vzniká pomocí následujícího vzorce:  

ATP = ATP předchozího období + příjmy aktuálního období - výdeje aktuálního období – čisté vydané množství pro každé budoucí období až do období, kdy součet příjmů pro pro všechna budoucí období (včetně budoucího období) je větší než součet výdejů (včetně budoucího období).  

Pokud neexistují další výdeje nebo příjmy, které lze vzít v úvahu, je množství ATP v dalších dnech stejné jako poslední vypočítané množství ATP.  

Nejsou-li při kontrole hodnoty ATP dokončeny všechny dimenze pro položku, mohou být i přesto zadány na výdejích nebo příjmech. V takovém případě musí být při výpočtu hodnoty ATP kvůli snížení počtu řádků příjmu a výdeje, které jsou použity při výpočtu hodnoty ATP, přičteny příjmy a výdeje ke stávajícím dimenzím.  

Zobrazené množství ATP je vždy větší než nebo rovno 0 (nule). Pokud výpočet vrátí záporné množství ATP (například když dříve přislíbené množství překročí dostupné množství), program automaticky nastaví množství na hodnotu **0**.

### <a name="example"></a>Příklad

Pole **ATP – zpětná ochranná doba poptávky** řídí to, jak daleko zpět v čase se mají hledat zpožděné objednávky poptávky nebo skladové výdeje. Pole **ATP – zpětná ochranná doba dodávky** řídí to, jak daleko zpět v čase se mají hledat zpožděné objednávky dodávky nebo skladové příjmy. Pokud mají být při výpočtu hodnoty ATP například zohledněny objednávky, které jsou zpožděny pouze o sedm dní, musí být obě pole nastavena na hodnotu **7**.  

Pole **ATP – čas kompenzace zpožděné poptávky** a **ATP – čas posunu zpožděné dodávky** řídí to, kdy mají být při výpočtu hodnoty ATP zahrnuty zpožděné poptávky nebo dodávky. Pokud mají být při výpočtu hodnoty ATP pozítří například zohledněny zpožděné dodávky a poptávky, musí být obě pole nastavena na hodnotu **2**. Hodnota **2** znamená, že množství položek na zpožděné nákupní objednávce, která by měla být zahrnutá ve výpočtu hodnoty ATP, se zobrazí jako dostupné dva dny po aktuálním datu.  

V následujícím příkladu je do polí **ATP – zpětná ochranná doba poptávky** a **ATP – zpětná ochranná doba dodávky** zadána hodnota **7** a do polí **ATP – čas kompenzace zpožděné poptávky** a **ATP – čas posunu zpožděné dodávky** zadána hodnota **1**.  

Nákupní objednávka na 200 kusů produktu, která měla být přijata před třemi dny, nebyla dosud přijata. Řádek prodejní objednávky pro 75 kusů stejného produktu, který měl být expedován včera, proto ještě nebyl expedován.  

Odběratel zavolá a chce si objednat 150 kusů stejného produktu. Při ověřování dostupnosti produktu zjistíte, že další nákupní objednávka na 100 kusů produktu bude doručena o 10 dní později.  

Vytvořte řádek prodejní objednávky pro daný produkt a jak množství zadejte hodnotu **150**.  

Vzhledem k tomu, že metoda řízení data dodání je ATP, vypočítají se data ATP, aby se našlo nejbližší možné datum expedice. Na základě nastavení je zohledněna zpožděná nákupní objednávka a prodejní objednávka a výsledné množství ATP pro aktuální datum je 0. Zítra, kdy je očekáváno přijetí zpožděné nákupní objednávky, se množství ATP vypočítá jako větší než 0 (v tomto případě bude mít hodnotu 125). Nicméně za 10 dní od dneška, kdy je očekáváno přijetí další nákupní objednávky na 100 kusů, bude množství ATP větší než 150.  

Proto je datum expedice na základě výpočtu hodnoty ATP nastaveno na 10 dní od tohoto okamžiku. Odběrateli tedy můžete sdělit, že požadované množství lze dodat za 10 dní od tohoto okamžiku.




