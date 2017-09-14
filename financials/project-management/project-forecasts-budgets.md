---
title: "Prognózy projektu a rozpočty"
description: 
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 835a92a8f95c7d75b02f5991cc2528c6a209540a
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="project-forecasts-and-budgets"></a>Prognózy projektu a rozpočty

[!include[banner](../includes/banner.md)]




Aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition poskytuje dva způsoby, jak spravovat a řídit projekty: prognózy projektu a rozpočty projektu. 

Prognózu projektu můžete použít, má-li vaše organizace operační perspektivu a zaměřuje se na výnosy a náklady, které jsou odvozeny od specifických transakcí. Rozpočty projektu můžete použít, pokud se vaše organizace více zaměřuje na finanční částky. 

Prognózy projektu a rozpočty projektu se používají k předvídání modelů pro předpokládané částky transakcí. 

Každá metoda má své výhody. Měli byste zvážit následující body, než vyberete metodu pro vaši organizaci.

|                           |                                                                                                                                                                                                                                                         |                                                                                                                                                                         |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                           | **Prognóza projektu**                                                                                                                                                                                                                                 | **Rozpočty projektu**                                                                                                                                                   |
| **Přidělení období**     | Transakce nelze přidělit explicitně za fiskální období. Místo toho prognóza a řízení prognózy vychází z životního cyklu projektu. Vzhledem k tomu, že prognózy jsou založeny na konkrétním datu, musíte období odvodit z data. | Transakce lze přidělit za celý projekt nebo fiskální období. Pokud provedete přidělení za období, můžete přenést nevyužité částky do dalšího fiskálního období. |
| **Zobrazení transakcí**  | Transakce můžete zobrazit ve formulářích prognózy, kde uvidíte prognózy pro celou společnost a pro všechny projekty, bez ohledu na hierarchii. Chcete-li se zaměřit na určitý projekt, musíte filtrovat data.                                       | Můžete zobrazit rozpočtové transakce pro jedinou hierarchii projektů. Proto můžete zobrazit podrobnosti o transakcích pro nadřízený projekt a jeho dílčí projekty.                 |
| **Proměnné transakcí** | Po zadání transakcí prognózy můžete využít každý atribut, který existuje, pro skutečnou transakci. To umožňuje větší podrobnosti v prognóze. Například můžete zadat podrobnosti o množství, pracovnících, zboží nebo vlastnostech řádku.         | Když zadáte podrobnosti rozpočtu, můžete použít pouze částky, kategorie a aktivity.                                                                                    |
| **Zabezpečení**              | Prognóza je založena na transakcích, které zadáte ve formuláři prognózy, a nezahrnuje žádný mechanismus kontroly procesu. Jakýkoli pracovník, který má oprávnění pro formulář prognózy, může informace revidovat bez schválení.                                        | Rozpočtování využívá systém workflow, který umožňuje správu změn a zachování historie revizí.                                                       |
| **Typy položek**           | Položky transakcí prognózy jsou založeny na počtu jednotek a na nákladových a prodejních jednotkových cenách.                                                                                                                                                       | Podrobnosti rozpočtu jsou založeny na částkách, které jsou rozděleny mezi náklady a výnosy.                                                                                        |
| **Modely prognóz**       | Vzhledem k tomu, že každá prognóza musí být přidružena modelu, lze vytvořit několik modelů prognózy a rovněž nastavit dílčí modely.                                                                                                                               | Rozpočty projektu omezují modely prognózy, které se používají pro rozpočtování. Méně modelů prognózy může přispět ke zvýšení konzistence v projekcích.                           |
| **Překročení nákladů**         | Můžete povolit nebo zakázat pouze položky transakcí, které způsobí překročení nákladů.                                                                                                                                                                | Sestavování rozpočtu projektu poskytuje další možnosti kontroly pro uživatele. Můžete povolit upozornění a překročení.                                                                   |
| **Kontrola**               | Ovládací prvek prognózy se provádí pomocí snížení prognózy. Skutečné částky jsou odečteny od zůstatků transakcí prognózy bez jakéhokoli záznamu pro audit. Proto může být složitější sledovat, kde ke skutečným transakcím došlo.                   | V kontrole rozpočtu projektu jsou skutečné částky odečteny od částek ve zbývajícím rozpočtu. To umožňuje lepší sledování auditu.                                   |

## <a name="project-forecasts"></a>Prognózy projektu
Použijete-li prognózu projektu, můžete transakce prognóz zadat ve formulářích prognózy pro každý typ transakce. Každý atribut, který je k dispozici pro aktuální transakcím lze použít pro transakci prognóz, jako například ziskovosti řádku, atributy řádku, zaměstnance nebo popis. Můžete také projektovat, jak dlouho po výdeji nákladů bude odběrateli odeslána faktura. 

Transakce prognózy u projektu vycházejí z jednotek a částek. 

Každý projekt musí být přidružen k modelu prognózy. Při zadání transakce prognózy bude automaticky navržen model prognózy. Model prognózy se chová jako kontejner pro transakce prognózy. 

Modely prognózy můžete označit jako dílčí modely modelu. To vám umožňuje vytvořit prognózy podle regionu, časového období nebo oddělení. Můžete zkopírovat transakce prognózy v modelu a vytvořit tak nový model, nebo převést transakce do hlavní knihy. Protože neexistuje vztah jedna ku jedné mezi prognózami a modelem, každý model prognózy tvoří samostatný rozpočet projektu. 

Modely prognóz mohou využívat snížení prognózy jako ovládací prvek pro projekty. Při snížení prognózy způsobí skutečné transakce snížení zůstatku u transakce prognózy. Vzhledem k tomu, že je snížení prognózy použito u nejvyšších projektů v hierarchii, poskytuje omezenou viditelnost změn v prognóze. Například pokud je pracovník přidružen k dílčímu projektu, skutečné transakce pracovníka jsou zaúčtovány do nadřazeného projektu. Z tohoto důvodu může být obtížné sledovat změny, protože nelze jednoduše určit, která transakce v jakém dílčím projektu způsobila snížení výše prognózy. Je proto vhodné vytvořit kopii modelu prognózy pro použití snížení prognózy. Poté můžete sestavy použít k zobrazení původní prognózy. 

Prognózy projektu je možné opravit, kopírovat, odstraňovat nebo přenášet do rozpočtu hlavní knihy. Neexistuje však žádná kontrola procesů. Kterýkoli pracovník s oprávněním pro přístup k formuláři prognózy můžete provést jednotlivé opravy bez kontroly.

-   **Opravit ** – Umožňuje provést revizi transakcí prognóz ve stejných formulářích, kde byly vytvořeny původní záznamy.
-   **Kopírovat nebo odstranit** – Při kopírování transakcí prognóz můžete zkopírovat řádky transakce jednoho modelu prognóz do jiného modelu prognózy. Při odstraňování prognóz dochází k odstranění transakcí prognózy z modelu prognózy. Pokud chcete omezit transakce prognóz, které jsou zkopírovány nebo odstraněny, vyberte vhodné typy a data transakce. Tímto způsobem lze zkopírovat nebo odstranit pouze konkrétní části prognózy.
-   **Převod** – Při přenosu prognózy projektu do rozpočtu hlavní knihy přenášíte transakce prognózy modelu prognózy do rozpočtu hlavní knihy. Transakce, které byly dříve přeneseny do rozpočtu hlavní knihy, do kterého přenášíte prognózu projektu, je možné přepsat.

## <a name="project-budgets"></a>Rozpočty projektu
Sestavování rozpočtu projektu je jednodušší metodou než prognózy, ačkoli je lze integrovat s modely prognózy. Používá formulář s jednou položkou pro podrobnosti a revize původního rozpočtu a umožňuje projekce založené pouze na částce, kategorii nebo aktivitě. 

Při rozpočtování projektu musí být všechny původní rozpočty a revize zaslány ke schválení do workflow projektu. Workflowy vám poskytují lepší kontrolu nad procesy a vytváří záznam historie změn. 

Sestavování rozpočtu projektu se podobá sestavování rozpočtu v hlavní knize, ale je rychlejší a nabízí jednodušší nastavení. Řada možností v sestavování rozpočtu v hlavní knize, například číselné řady nebo měna, nemusí být nastaveny zvlášť pro projekty.

Rozpočty projektu jsou automaticky spojeny se dvěma modely prognózy, jedním pro původní rozpočet a druhým pro zbývající rozpočet. Z toho vyplývá, že sestavy, které jsou založeny na modelech prognóz, mohou používat data rozpočtu. Při potvrzení rozpočtu projektu systém vytvoří transakce prognózy založené na přidružených modelech, které se používají pro účely vytváření sestav a kontrolu.

## <a name="forecast-models"></a>Modely prognóz
Modely prognóz mají jednovrstvou hierarchii. To znamená, že jedna prognóza projektu musí být přidružena k jednomu modelu prognózy.

Pokud používáte prognózy projektu, můžete identifikovat modely jako dílčí modely. Pak můžete vytvářet prognózy podle oddělení, časového období nebo regionu. Můžete například vytvořit model prognózy pro rok a poté vytvořit dílčí modely pro regionální prognózy severovýchodu, jihovýchodu, severozápadu a jihovýchodu, které odešle regionální vedoucí. Výběrem různých možností v dostupných sestavách můžete zobrazit informace dle celkové prognózy nebo dílčího modelu.




