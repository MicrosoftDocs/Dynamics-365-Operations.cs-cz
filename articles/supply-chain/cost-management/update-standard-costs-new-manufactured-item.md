---
title: Aktualizace standardních nákladů pro nově vyrobené položky
description: Tento článek obsahuje pokyny pro aktualizaci standardních nákladů pro nově vyrobenou položku.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79693
ms.assetid: ba64b70f-3f4c-4373-9a7d-8fd07c45a8cf
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6af1c88aee878e0ab1e28fc0247d4c184f8b9d21
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983869"
---
# <a name="update-standard-costs-for-a-new-manufactured-item"></a>Aktualizace standardních nákladů pro nově vyrobené položky

[!include [banner](../includes/banner.md)]

Tento článek obsahuje pokyny pro aktualizaci standardních nákladů pro nově vyrobenou položku. 

Tyto pokyny předpokládají, že používáte pro aktualizaci standardních nákladů metodou s použitím dvou verzí. V tomto přístupu jedna nákladová verze obsahuje původně definované standardní náklady pro nastavené období a druhá nákladová verze obsahuje vzestupné aktualizace, které se týkají nově vyrobených položek. Přírůstkové aktualizace budou zadány jako záznamy o nákladech do druhé nákladové verze a nakonec budou aktivovány. Metoda s použitím dvou verzí vyžaduje určení druhé nákladové verze. Uvádíme pokyny k definování této nákladové verze:

-   Přiřaďte nákladový typ **Standardní náklady**.
-   Přiřazení platného popisného identifikátoru značícího obsah nákladové verze, jako je například **2016-AKTUALIZACE**.
-   Ve skupině polí **Povolit typy cen** se ujistěte, že je **Nákladová cena** nastavena na **Ano**.
-   Povolte zadání záznamy nákladů pro všechna pracoviště (tj. ponechte pole **Pracoviště** prázdné). Pokud určíte pracoviště, záznamy nákladů lze zadat pouze pro dané pracoviště.
-   Použití principu zálohy **Aktivní**.

Chcete-li přidat nově vyrobené položky v průběhu zmrazeného období, proveďte následující kroky.

1.  Pomocí stránky **Nastavení nákladové verze** povolte zadání záznamy nákladů do druhé nákladové verze, která obsahuje přírůstkové aktualizace. Zabraňte aktivaci čekajících nákladů, protože tato aktivace bude povolena po úplném a přesném definování těchto nákladů. V nákladové verzi vytvořte zásadu, ve které ponechte počáteční datum prázdné a potom zadejte počáteční datum při zadání každého záznamu o nákladech. Počáteční datum by mělo být starší, než bude datum nákupu nebo výroby nových položek.
2.  Stránku **Cena položky** použijte k zadání záznamů o cenách nově nakoupených položek. Pro každý záznam o ceně zadejte nákladovou verzi, která obsahuje přírůstkové aktualizace, a použijte počáteční datum, které je před očekávaným datem výroby nových položek.
3.  Vypočítejte náklady nově vyrobených položek s použitím stránky **Výpočet**. Otevře stránku **Výpočet** na stránce **Údržba nákladové verze** a poté vyberte nákladovou verzi, která obsahuje přírůstkové aktualizace. Kritéria výběru lze použít k výběru nově vyrobených položek, respektive jejich součástí. Ve víceúrovňové struktuře produktů je také třeba zadat nadřazené položky, které obsahují jako součásti nově vyrobené položky. Pro výpočet kusovníku zadejte počáteční datum, které odpovídá zahájení výroby nových položek. Počáteční datum by mělo být v intervalu platnosti verze kusovníku a technologického postupu. **Poznámka:** Chybějící záznam o nákladech může znamenat nově vyrobenou položku. Výpočty kusovníku lze omezit na položky s chybějícími náklady.
4.  Ověřte vypočtené náklady u nově vyrobených položek z hlediska úplnosti a přesnosti. Pomocí stránky **Dokončit** zkontrolujte vypočtené náklady pro každý záznam nákladů položek a ověřte případné varovné zprávy Informačního protokolu. Případně pomocí stránky **Výpočet** zkontrolujte vypočtené náklady.
5.  Pomocí stránky **Nastavení nákladové verze** upravte příznak blokování a umožnit tak aktivaci záznamů čekajících nákladů ve druhé nákladové verzi.
6.  Pomocí stránky **Aktivovat ceny** (kterou otevřete ze stránky **Údržba nákladové verze**) povolte všechny čekající záznamy nákladů ve druhé nákladové verzi. Čekající záznamy nákladů pro jednotlivé položky lze také povolit klepnutím na tlačítko **Aktivovat** na stránce **Cena položky**.
7.  Pomocí stránky **Nastavení nákladové verze** upravte příznaky blokování ve druhé nákladové verzi pro zabránění další údržby dat. Zásady blokování zabraňují zadávání nových čekajících nákladů a aktivaci čekajících nákladů.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]