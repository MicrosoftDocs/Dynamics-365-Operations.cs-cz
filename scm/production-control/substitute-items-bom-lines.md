---
title: "Nahrazení materiálů ve výrobě"
description: "Toto téma popisuje nahrazení materiálů během výrobního procesu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdBOM
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70171
ms.assetid: ce3b11ef-550e-49b7-8942-2607c2ec3c5c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5bd0c12ace98cf7d3c04ad4fdb5b2da72907dbf0
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="material-substitution-in-manufacturing"></a>Nahrazení materiálů ve výrobě

[!include[banner](../includes/banner.md)]


Toto téma popisuje nahrazení materiálů během výrobního procesu. 

Nahrazení materiálů během výrobního procesu lze provést třemi způsoby:

-   Podle data, kdy je jeden materiál nahrazen jiným po zadaném datu
-   Během hlavního plánování, když je materiál v receptuře nahrazena jiným, protože není na skladě
-   Během výroby, když materiál neočekávaně dojde a je nahrazen jiným materiálem

## <a name="substituting-material-by-date"></a>Nahrazení materiálu podle data
Zvažte následující scénář: počítač, který společnost vyrábí obsahuje součást, která vyprší za dva měsíce z katalogu dodavatele. Od data vypršení platnosti dále dodavatel navrhne novou komponentu, která může nahradit starou komponentu. Data platnosti Od a Do lze nastavit na řádcích kusovníku. V tomto příkladu nastavíte konec platnosti staré komponenty zadáním data vypršení platnosti v poli **Do data**. Poté pro kusovník nastavíte novou náhradní komponentu tak, aby byla platná od dne po konci platnosti staré komponenty. Chcete-li to provést, zadejte počáteční datum v poli **Od data**.

## <a name="substituting-material-by-planning"></a>Nahrazení materiálu pomocí plánování
Materiál lze nahradit při plánování, pouze pokud používáte receptury, ne když používáte kusovník. Zvažte následující situaci: Výrobce potravin vyrábí omáčku z receptury, která má 20 přísad. Jednu přísadu v receptuře lze nahradit jednou ze dvou jiných přísad. Vzhledem k tomu, že tyto dvě přísady jsou dražší než upřednostňovaná přísada, nahrazení se použijí pouze v případě, že upřednostňovaná přísada není na skladě. Materiál, který lze nahradit, se nazývá A, zatímco dva materiály, které jej nahrazují, jsou označeny písmeny B a C. Nahrazení materiálu při plánování je poli **Skupin plánu** a **Priorita** na řádcích receptury. V tomto příkladu vytvoříte řádky receptury pro tři materiály a přidružíte řádky receptury ke stejné skupině plánu. V nastavení má řádek receptury pro materiál A nejvyšší prioritu (nejnižší číslo), řádek receptury pro materiál C má nejnižší prioritu a řádek receptury pro materiál B má prioritu, která je mezi prioritami těchto dvou jiných řádků. Pokud máte poptávku pro dokončené položce, hlavní plánování nejprve určí, zda lze poptávku po materiálu A pokrýt. Pokud nelze poptávku pokrýt, hlavní plánování se zaměří na materiál B a C podle priority. Je-li materiál B na skladě, použije se po potvrzení plánované dávkové objednávky pro recepturu. Pokud není žádný z těchto materiálů na skladě, hlavní plánování vytvoří plánovanou objednávku pro materiál A. **Poznámka:** Když nastavíte řádky receptury ve skupině plánu, měli byste zadat množství pouze u materiálu, který má nejvyšší prioritu. Toto množství bude použito k výpočtu poptávky pro všechny materiály v plánu, a to i materiálů, které mají nižší prioritu. Ve skupině plánu nelze určit různá množství u položek s nižší prioritou.

## <a name="substituting-material-during-production"></a>Nahrazení materiálu během výroby
Předpokládejme následující situaci: Kovová destička je vyžadována u svařovací operace. V průběhu operace pracovník skladu informuje operátora stroje, že destička není na skladě. Je však rozhodnuto, že destička bude nahrazena jinou, která je o trochu silnější. Díky tomu může být operace dokončena. Materiál lze přidat do kusovníku pro otevřenou výrobní zakázku. Je-li výrobní zakázka ve stavu **Zahájeno**, uživatelé jsou vyzváni k opětovnému odhadu objednávky při přidání nové položky do výrobního Kusovníku. Poté, co je přidán materiál, lze vytvořit novou výdejku pro novou položku. Nemusíte přidávat nový materiál do výrobního kusovníku. Namísto toho je možné jej přímo přidat na výrobní výdejku. Při zaúčtování výdejky systém materiál přidá do výrobního kusovníku.




