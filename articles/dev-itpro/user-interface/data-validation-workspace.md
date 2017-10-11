---
title: "Pracovní prostor ověření dat"
description: "Pracovní prostor Kontrolní seznam ověřování dat umožňuje sledování procesů ověřování dat mezi společnostmi, oblastmi a osobami. Kontrolní seznam lze použít během nové implementace, po upgradu nebo po migraci."
author: bking
manager: AnnBe
ms.date: 05/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: 
ms.assetid: 
ms.search.region: Global
ms.author: bking
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: e105c4b171979a03c20718c1fa9d558c921cd704
ms.contentlocale: cs-cz
ms.lasthandoff: 06/20/2017

---

# <a name="data-validation-workspace"></a>Pracovní prostor ověření dat

[!include[banner](../includes/banner.md)]


Toto téma poskytuje přehled pracovního prostoru **Kontrolní seznam ověřování dat** a přidružené konfigurace.

## <a name="data-validation-checklist-workspace"></a>Pracovní prostor kontrolního seznamu ověřování dat

Pracovní prostor **Kontrolní seznam ověřování dat** umožňuje sledování procesů ověřování dat mezi společnostmi, oblastmi a osobami. Kontrolní seznam lze použít během nové implementace, po upgradu nebo po migraci. V závislosti na zobrazení pracovního prostoru **Kontrolní seznam ověřování dat** se zobrazí buď všechny úkoly a stavy pro projekt ověřování dat, nebo pouze úkoly, které vám byly přiřazeny.

Nejprve je nutné vybrat projekt ověřování dat v horní části pracovního prostoru. Všechna data, která jsou zobrazena v pracovním prostoru, jsou pak filtrována podle vybraného projektu ověřování dat.

### <a name="summary-tiles"></a>Dlaždice souhrnu

Dlaždice **Souhrn** poskytují přehled procesu a ukazatelé vám pomohou udržet proces ověřování dat podle plánu. Pro proces můžete zobrazit všechny zbývající úlohy, dokončené úlohy, probíhající úlohy a nezahájené úlohy. Tyto informace jsou pro všechny společnosti, které jsou zahrnuté do vybraného projektu ověřování dat.

### <a name="tasks-and-status-section"></a>Úkoly a výběr stavu

V části **Úkoly a stav** se zobrazí celkový stav projektu ověřování dat různými způsoby: stav podle právnické osoby, oblasti a seznamu úloh. Můžete vybrat filtr pro zobrazení stavu pro konkrétní společnost. Každá karta stavu poskytuje rozpis podle procenta, které bylo dokončeno, a počtu úkolů, které zbývají.

Poslední karta je určená pro seznam podrobných úkolů. Tento seznam zobrazuje úplný seznam úkolů.
Můžete filtrovat seznam úkolů v několika způsoby. Chcete-li změnit stav úkolu nebo přiřadit úkol, klikněte na možnost **Upravit úkol**. Chcete-li zobrazit přílohy úkolu, klikněte na možnost **Přílohy**.

Název úkolu je hypertextový odkaz na stránku Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, nebo jinou webovou stránku, kam uživatel musí přejít k dokončení práce. Tento hypertextový odkaz lze nastavit pomocí pole **Název položky nabídky** při úpravě nebo vytváření úkolu z formuláře **Konfigurace projektu ověřování dat**.

Soubory, poznámky, obrázky a adresy URL můžete připojit k úkolu pomocí akce **Přílohy**. Například můžete připojit soubor sestavy, který byl vytištěn pro úkol. Ikona se zobrazí ve sloupci **Přílohy** pro úkol, pokud je příloha k dispozici.

Možnost **Vyplnil/a** bude automaticky doplněna po dokončení úkolu jménem pracovníka, který úkol dokončil. Pokud je úkol označen jako dokončený, pole **Datum dokončení** je automaticky aktualizováno na aktuální datum a čas.

### <a name="configure-data-validation-project-page"></a>Konfigurace stránky projektu ověřování dat

Před použitím pracovního prostoru **Kontrolní seznam ověřování dat** je nutné nakonfigurovat proces s použitím stránky **Konfigurace stránky projektu ověřování dat**. (Klikněte na tlačítko **Pracovní prostory** \> **Kontrolní seznam ověřování dat** \> **Konfigurace projektu ověřování dat**.)

### <a name="task-areas"></a>Oblasti úkolů

Pomocí oblastí úkolů seskupte úkoly ověřování dat do logických oblastí vlastnictví ve vaší organizaci. Například závazky, pohledávky a hlavní kniha mohou být použity jako oblasti úkolu.

**Název položky nabídky** je spojen s pracovním úsilím úkolu a lze ho použít k přechodu přímo na přidruženou stránku z odkazu na úkol v pracovním prostoru. Například úloha ověřování dat pro spuštění sestavy **sledování splatnosti závazků** pro závazky lze spojit se stránkou **Sestava sledování splatnosti závazků**.
