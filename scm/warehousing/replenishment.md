---
title: "Doplnění"
description: "Tento článek popisuje strategie doplnění, které jsou k dispozici pro sklady, které používají funkce, které jsou k dispozici v modulu Řízení skladu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSReplenishmentTemplates
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90043
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 77b895e7f7edd6f22ee960ba2ec4bdd2931c29f8
ms.lasthandoff: 03/31/2017


---

# <a name="replenishment"></a>Doplnění

[!include[banner](../includes/banner.md)]


Tento článek popisuje strategie doplnění, které jsou k dispozici pro sklady, které používají funkce, které jsou k dispozici v modulu Řízení skladu.

Tento článek popisuje strategie doplnění, které jsou k dispozici pro sklady, které používají funkce, které jsou k dispozici v modulu Řízení skladu. Informace se nevztahují na skladové řešení, které je k dispozici v modulu Řízení zásob. K dispozici jsou tři strategie doplnění:

-   **Doplnění na základě poptávky vlny** – Tato strategie doplnění vytvoří práci doplnění pro výstupní objednávky nebo vytížení, pokud zásoby nejsou k dispozici, pokud práce není vytvořena vlnou. Například je možné vytvořit proces doplnění, pokud množství, které je nutné pro prodejní objednávku, není k dispozici při zpracování vlny.
-   **Doplnění metodou min/max.** – Tato strategie používá minimální a maximální limity uskladnění k určení, kdy doplnit umístění. Položka a kritéria umístění definují zásoby, které jsou hodnoceny pro doplnění. Šablony doplnění metodou min/max. jsou primární mechanismus pro udržování optimální úrovně výdejních skladových míst. Aby bylo jisté, že je k dispozici k dostatek zásob pro vyskladnění pro uspokojení poptávky vlny, můžete použít doplnění v závislosti na poptávce mezi cykly doplnění metodou Min/Max.
-   **Doplnění poptávky nákladu** – Tato strategie využívá souhrn poptávky po několik nákladů a vytváří doplnění, které je nutné pro zásobování příslušných výdejních skladových míst. Tato strategie pomáhá zaručit, že náklad, který je vytvořen, bude možné vydávat ve skladu po jeho uvolnění.

Všechny tři strategie vytváří doplnění založené na šabloně doplnění.

## <a name="wave-demand-replenishment"></a>Doplnění na základě poptávky vlny
Doplnění na základě poptávky vlny vytvoří doplnění na základě poptávky, pokud množství požadované pro výstupní objednávky nebo vytížení není k dispozici, když vlna vytvoří práci. Šablona doplnění obsahuje informace o kritériích zboží, měrnou jednotku, přírůstek poptávky a umístění. 

Směrnice umístění se používají k určení umístění, které je třeba doplnit. Tyto směrnice umístění můžete propojit s šablonami doplnění pomocí pole **Kód směrnice**. Pokud pole **Kód směrnice** není zatím nastaveno, používají se dotazy k určení toho, která směrnice umístění by měla být použita. Všimněte si, že pokud v šabloně doplnění není zadán kód směrnice, a směrnice umístění obsahuje kód směrnice, tak směrnice umístění bude ignorována, a to i v případě, že dotaz na směrnici umístění je v pořádku. Směrnice výdejního umístění se používají k určení toho, kde získat zásoby pro doplnění. 

Kromě vytvoření šablony je nutné zadat určitá nastavení doplnění v šabloně vlny. Šablona vlny by měla obsahovat krok vlny pro doplnění, který se spustí pouze v případě, že přidělení zboží není úspěšné. V tomto kroku vlny doplnění se používá kód kroku vlny pro určení toho, která šablona doplnění by se měla použít. Kromě kroku vlny pro doplnění je nutné ujistit se, že je vybráno **doplnění** v části **Metody** u šablony vlny. 

Stránka **Šablona doplnění** obsahuje pole **Povolit u vlny poptávky použití nerezervovaných množství**. Toto pole by mělo být povoleno, pokud chcete povolit u doplnění poptávky odečtení nerezervovaného množství z práce vygenerované z vybrané šablony doplnění. Toto políčko je třeba použít pro každou existující šablonu doplnění, pokud chcete umožnit šablonám doplnění poptávky používat tuto logiku. Pokud práce pochází ze šablony doplnění s označeným polem **Povolit poptávku vlny pro použití nerezervovaného množství**, při spuštění doplnění poptávky ve skladu dojde k odečtení poptávky z existující práce doplnění pomocí nerezervovaného množství.

## <a name="minmax-replenishment"></a>Doplnění metodou min/max.
U doplnění metodou min/max. probíhá doplnění zásob tak, aby byly ve stanoveném minimálním a maximálním rozsahu. Obvykle tento proces probíhá jednou denně k zajištění toho, že jsou všechna výdejní skladová místa naplněna na maximální úroveň před zahájením výdeje. 

Minimální a maximální objemy jsou nastaveny v šabloně doplnění. Mnoho dalších nastavení v šabloně je podobné, jako v šablonách, které se používají u doplnění na základě poptávky vlny. Šablona by měla obsahovat jeden řádek pro každou položku a skladové místo. Při provádění doplnění pomocí dávkové úlohy Microsoft Dynamics 365 for Operations vyhodnotí, zda doplnění je vyžadovány v pořadí, ve kterém jsou uspořádány řádky. 

Všimněte si, že strategie doplnění metodou Min/Max. nedokáže doplnit prázdné místo, pokud není umístění nastaveno jako pevné umístění pro položku. Není-li umístění, které musí být doplněno, nastaveno jako pevné umístění, aplikace Dynamics 365 for Operations nedokáže určit, kterou položku je třeba doplnit. Proto je nutné před zahájením doplnění mít na skladě alespoň část množství.

## <a name="load-demand-replenishment"></a>Doplnění poptávky nákladu
Doplnění poptávky nákladu využívá souhrn poptávky po několik nákladů a vytváří doplnění, které je nutné pro zásobování příslušných výdejních skladových míst. Doplnění poptávky nákladu se velice podobá doplnění na základě poptávky vlny. Hlavní rozdíl je jak a kdy je Doplnění poptávky nákladu a Doplnění na základě poptávky vlny spouštěno. Stejně jako doplnění metodou Min/Max. je Doplnění poptávky nákladu spouštěno v rámci dávkové úlohy. Chcete-li nastavit dávkovou úlohu na stránce **Doplnění poptávky nákladu**, vyberte šablonu doplnění, kterou chcete používat, a nastavením dotazu filtru určete náklad, který se použije k určení poptávky. Dotaz na umístění definuje umístění, ze kterého se veškeré dostupné množství odečte, aby byla naplněna souhrnná poptávka nákladu.

## <a name="replenishment-prerequisites"></a>Předpoklady doplnění
| Předpoklad            | Popis                                                                                                                                                                                                                                        |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Položka                    | Položky musí být povoleny pro procesy správy skladu.                                                                                                                                                                                       |
| Sklad               | Sklad musí být povolen pro procesy správy skladu. Pokud chcete povolit sklad pro procesy správy skladu, vyberte na stránce **Sklady** sklad a poté označte možnost **Použít procesy řízení skladu**. |
| Šablony doplnění | Je nutné nastavit alespoň jednu šablonu pro Doplnění metodou min/max., Doplnění na základě poptávky vlny nebo Doplnění poptávky nákladu.                                                                                                             |
| Místa               | Umístění musí být vytvořeno a připojeno k profilu umístění.                                                                                                                                                                                     |
| Profily umístění       | Profily umístění jsou nutné k vytvoření umístění.                                                                                                                                                                                       |
| Směrnice skladového místa     | Směrnice umístění jsou nezbytné, aby bylo možné provést práci v umístění, které vyžaduje doplnění, a v umístění, ze kterého zásoby pochází.                                                                                     |
| Šablony práce          | Šablony práce typu **Doplnění** jsou nutné pro vytvoření doplnění, a aby bylo možné zásoby přenášet do požadovaného umístění.                                                                                           |





