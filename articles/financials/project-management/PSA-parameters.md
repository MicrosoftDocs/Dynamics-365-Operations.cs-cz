---
title: Parametry integrace Project Service Automation
description: "Můžete nakonfigurovat, jak mají být nastavena data ve výchozím nastavení při integraci Project Service Automation s aplikací Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 32f7f70c5b1071cef5a3360ccc09fa2d95fbf9a9
ms.contentlocale: cs-cz
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation-integration-parameters"></a>Parametry integrace Project Service Automation

Na stránce **Parametry integrace Project Service Automation** lze konfigurovat způsob, jaká mají být výchozí data při integraci aplikace Project Service Automation s aplikací Finance and Operations. Následující parametry musí být nastaveny pro projekty, aby byly synchronizovány úspěšně z aplikace Project Service Automation do aplikace Finance and Operations.

> [!NOTE]
> Integrace úkolů projektu, kategorie transakce výdajů, odhady hodin, odhady výdajů a uzamykání funkcí jsou k dispozici v aplikaci Dynamics 365 for Finance and Operations verze 8.0.




| **Karta**                      | **Pole**                          | **Popis**                    |
|------------------------------|------------------------------------|--------------------------------|
| **Obecné**                  | **Výchozí typ projektu**               | Vyberte výchozí pro **Typ projektu**, pokud se projekty synchronizují z aplikace Project Service Automation, když jste nezadali výchozí hodnotu v šabloně integrace. Během synchronizace budou mít nové projekty nastavený **Typ projekt** na tuto hodnotu a mohou být aktualizovány, když jsou řádky smlouvy projektu synchronizovány z aplikace Project Service Automation.               |
| **Obecné**                  | **Kategorie času**                      | Vyberte výchozí pro **Kategorie času**, když jsou synchronizovány odhady hodin z aplikace Project Service Automation. Během synchronizace prognóza hodin nového projektu v aplikaci Finance and Operations bude mít položku **Kategorie** nastavenou na tuto hodnotu, když odhady hodin a skutečné hodiny jsou synchronizovány z aplikace Project Service Automation.   |
| **Obecné**                  | **Kategorie poplatku**                       | Vyberte výchozí pro **Kategorie poplatku**, když jsou skutečné hodnoty poplatků synchronizovány z aplikace Project Service Automation. Během synchronizace nové transakce poplatků v aplikaci Finance and Operations budou mít položku **Kategorie** nastavenou na tuto hodnotu, když skutečné poplatky jsou synchronizovány z aplikace Project Service Automation.          |
| **Výchozí hodnoty skupiny projektu**   | **Typ projektu** | Klikněte na **Nový** a přidejte řádek, kde můžete vybrat typ projektu, pro který chcete nastavit výchozí skupiny projektů. Konkrétní typ projektu lze vybrat pouze jednou v konfiguraci.              
|                              | **Skupina projektu**          | Vyberte výchozí skupinu projektů pro konkrétní typ projektu. Když se z aplikace Project Service Automation. synchronizují nové projekty, **Skupina projektu** bude výchozí na základě typu projektu, pokud jste nezadali výchozí hodnotu v šabloně integrace.  |
| **Výchozí hodnoty typu účtování**    | **Typ účtování** | Klikněte na **Nový** a přidejte řádek, kde můžete vybrat typ účtování, pro který chcete nastavit výchozí vlastnost řádku. Konkrétní typ účtování lze vybrat pouze jednou v konfiguraci.          |
|                              | **Vlastnost řádku**| Vyberte výchozí vlastnost řádku pro konkrétní typ účtování. Když jsou synchronizovány nové odhady hodin, nové odhady výdajů nebo nové skutečné hodnoty z Project Service Automation, **Vlastnost řádku** bude výchozí na základě typu účtování.          |
| **Uzamčení funkce**    |                   | Vyberte tuto funkci pro zakázání projektů a smluv v aplikaci Finance and Operations, pocházejících z Project Service Automation. Například je možné vypnout možnost upravit smlouvy a projekty, vytvořit struktury rozpisu práce a zadávat časové rozvrhy v aplikaci Finance and Operations. Pole související s účetnictví budou nadále povolena, i v případě, že nejsou k dispozici podle nastavení parametrů. Standardně budou všechny funkce povoleny.           |

