---
title: Pracovní prostor kontrolního seznamu ověřování dat
description: Pracovní prostor Kontrolní seznam ověřování dat umožňuje sledování procesů ověřování dat mezi společnostmi, oblastmi a osobami.
author: bking
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: bking
ms.assetid: ''
ms.search.form: DataValidationWorkspace
ms.openlocfilehash: fb8999815e96c0aa7d1a054073de77a382c14263
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272475"
---
# <a name="data-validation-checklist-workspace"></a>Pracovní prostor kontrolního seznamu ověřování dat

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Tento článek poskytuje přehled pracovního prostoru **Kontrolní seznam ověřování dat** a přidružené konfigurace.

Pracovní prostor **Kontrolní seznam ověřování dat** umožňuje sledování procesů ověřování dat mezi společnostmi, oblastmi a osobami. Kontrolní seznam lze použít během nové implementace, po upgradu nebo po migraci. V závislosti na zobrazení pracovního prostoru **Kontrolní seznam ověřování dat** se zobrazí buď všechny úkoly a stavy pro projekt ověřování dat, nebo pouze úkoly, které vám byly přiřazeny.

Nejprve je nutné vybrat projekt ověřování dat v horní části pracovního prostoru. Všechna data, která jsou zobrazena v pracovním prostoru, jsou pak filtrována podle vybraného projektu ověřování dat.

## <a name="summary-tiles"></a>Dlaždice souhrnu

Dlaždice **Souhrn** poskytují přehled procesu a indikátory vám pomohou udržet proces ověření dat podle plánu. Zobrazí se vám všechny zbývající úlohy, dokončené úlohy, probíhající úkoly a nezahájené úkoly procesu. Tyto informace jsou pro všechny společnosti, které jsou zahrnuté do vybraného projektu ověřování dat.

## <a name="tasks-and-status-section"></a>Úkoly a výběr stavu

V části **Úkoly a stav** se zobrazí celkový stav projektu ověřování dat různými způsoby: stav podle právnické osoby, oblasti a seznamu úloh. Můžete vybrat filtr pro zobrazení stavu pro konkrétní společnost. Každá karta stavu poskytuje rozpis podle procenta, které bylo dokončeno, a počtu úkolů, které zbývají.

Poslední karta je určená pro seznam podrobných úkolů. Tento seznam zobrazuje úplný seznam úkolů. Můžete filtrovat seznam úkolů v několika způsoby. Chcete-li změnit stav úkolu nebo přiřadit úkol, klikněte na možnost **Upravit úkol**. Chcete-li zobrazit přílohy úkolu, klikněte na možnost **Přílohy**.

Název úkolu je hypertextový odkaz na stránku nebo jinou webovou stránku, kam uživatel musí přejít k dokončení práce. Tento hypertextový odkaz lze nastavit pomocí pole **Název položky nabídky** při úpravě nebo vytváření úkolu z formuláře **Konfigurace projektu ověřování dat**.

Soubory, poznámky, obrázky a adresy URL můžete připojit k úkolu pomocí akce **Přílohy**. Například můžete připojit soubor sestavy, který byl vytištěn pro úkol. Ikona se zobrazí ve sloupci **Přílohy** pro úkol, pokud je příloha k dispozici.

Možnost **Vyplnil/a** bude automaticky doplněna po dokončení úkolu jménem pracovníka, který úkol dokončil. Pokud je úkol označen jako dokončený, pole **Datum dokončení** je automaticky aktualizováno na aktuální datum a čas.

## <a name="configure-data-validation-project-page"></a>Konfigurace stránky projektu ověřování dat

Před použitím pracovního prostoru **Kontrolní seznam ověřování dat** je nutné nakonfigurovat proces s použitím stránky **Konfigurace stránky projektu ověřování dat**. (Klikněte na tlačítko **Pracovní prostory** \> **Kontrolní seznam ověřování dat** \> **Konfigurace projektu ověřování dat**.)

## <a name="task-areas"></a>Oblasti úkolů

Pomocí oblastí úkolů seskupte úkoly ověřování dat do logických oblastí vlastnictví ve vaší organizaci. Například závazky, pohledávky a hlavní kniha mohou být použity jako oblasti úkolu.

**Název položky nabídky** je spojen s pracovním úsilím úkolu a lze ho použít k přechodu přímo na přidruženou stránku z odkazu na úkol v pracovním prostoru. Například úloha ověřování dat pro spuštění sestavy **sledování splatnosti závazků** pro závazky lze spojit se stránkou **Sestava sledování splatnosti závazků**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
