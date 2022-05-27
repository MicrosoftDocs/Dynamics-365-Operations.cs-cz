---
title: Přehled servisních úloh
description: Servisní úlohy lze použít k popisu úloh, které mají být dokončeny v průběhu servisní zakázky. Tyto informace mohou vidět technici a zákazníci.
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76eba18fb9228c3b9c2accf17cb938e7f2a12dbe
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671695"
---
# <a name="service-tasks-overview"></a>Přehled servisních úloh

[!include [banner](../includes/banner.md)]

Servisní úlohy lze použít k popisu úloh, které mají být dokončeny v průběhu servisní zakázky.
Tyto informace mohou vidět technici a zákazníci.

K vytváření servisních úloh slouží stránka **Servisní úlohy** lze přidružit k určité servisní smlouvě nebo servisní zakázce pomocí vztahů servisních úloh. Při vytváření vztahu servisní úlohy můžete vytvořit:

-  interní poznámky k úloze, například podrobné technické požadavky, o nichž by měli vědět technici;

-  externí poznámky, které mohou vidět zákazníci. Zde je možné uvést méně technické vysvětlení prováděné úlohy v závislosti na smlouvě mezi zákazníkem a servisní společností.

Když vytvoříte vztah servisní úlohy mezi servisní úlohou a servisní zakázkou nebo servisní smlouvou, můžete tuto servisní úlohu zadat při vytváření řádků servisní zakázky nebo servisní smlouvy pro aktuální servisní zakázku či smlouvu.

Pokud na základě servisní smlouvy generujete servisní zakázky, můžete použít servisní úlohy přiřazené k jednotlivým řádkům servisní smlouvy k seskupení řádků servisní zakázky do servisních zakázek.

## <a name="create-a-service-task"></a>Vytvoření servisní úlohy

1. Klikněte **Správa servisu** \> **Nastavení** \> **Servisní úlohy**.
2. Vytvořit nový řádek.
3. Zadejte ID servisu a popis.

## <a name="example"></a>Příklad

Technik má za úkol dokončit dvě práce na převodovce (předmět servisu GB-1234), a to u zákazníka. Pro daného zákazníka je vytvořena servisní smlouva a k uvedeným pracím je přidruženo několik transakcí. Servisní smlouva a řádky servisní smlouvy pro tyto dvě práce jsou uvedeny dále:

### <a name="service-agreement"></a>Servisní smlouva

| Project | Servisní smlouva | popis                                  | Seskupit   |
|---------|-------------------|----------------------------------------------|---------|
| 9012    | 000008\_001       | Kontrola a rutinní výměna – GB-1234 | Prémiové |

### <a name="service-agreement-lines"></a>Řádky servisní smlouvy

| popis             | typ transakce | Předmět servisu | Servisní úloha |
|-------------------------|------------------|----------------|--------------|
| Prohlídka a čištění | Hodina             | GB-1234        | I/C - GB1234 |
| Cestovné                  | Expense          | GB-1234        | I/C - GB1234 |
| Materiály               | Zboží             | GB-1234        | I/C - GB1234 |
| Rutinní výměna     | Hodina             | GB-1234        | RR - GB1234  |
| GR-1                    | Zboží             | GB-1234        | RR - GB1234  |
| GR-5                    | Zboží             | GB-1234        | RR - GB1234  |

K řádkům servisní smlouvy pro tyto dvě práce jsou připojeny dvě servisní úlohy. Servisní úlohy definují transakce, které náleží k jednotlivým pracím. V prvním případě servisní úloha I/C - GB1234 identifikuje všechny řádky servisní smlouvy související s kontrolou a čištěním předmětu GB-1234. V druhém případě servisní úloha RR - GB1234 identifikuje všechny řádky servisní smlouvy související s provedením rutinní výměny.

Servisní úlohy jsou se specifickou smlouvou propojeny pomocí následujících vztahů servisních úloh:

### <a name="service-tasks"></a>Servisní úlohy

| Servisní úloha | Popis                             | Interní poznámka                                                                                                                 | Externí poznámka                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| I/C - GB1234 | Kontrola převodovky GB-1234           | Vizuální a mechanická kontrola a čištění převodovky GB-1234.                                                              | Rutinní kontrola převodovky |
| RR - GB1234  | Rutinní výměna dílů v převodovce GB-1234 | Rutinní výměna součástí GR-1 a GR-5 (u převodovek vyrobených před rokem 2002 také výměna součásti GR-2) | Rutinní výměna dílů  |

## <a name="group-service-orders"></a>Seskupení servisních zakázek

Při automatickém vytváření servisních zakázek můžete použít servisní úlohy jako kritéria seskupení. Chcete-li seskupit servisní zakázky podle servisních úloh, uveďte v servisní smlouvě, že k seskupení servisních zakázek založených na této servisní smlouvě má být jako počáteční kritérium seskupení použito ID servisní úlohy.

**Seskupení podle servisní úlohy**

1. Klikněte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**.
2. Na kartě **Nastavení** zvolte **Podle servisní úlohy** v poli **Kombinace servisních zakázek**.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]