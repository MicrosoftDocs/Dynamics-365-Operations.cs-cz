---
title: Aktualizace standardních nákladů v nevýrobním prostředí
description: V tomto článku jsou pokyny k tomu, jak aktualizovat standardní náklady v nevýrobním prostředí.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 548955f544842ea5f60fd2d800c8c11cb459ee4c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679072"
---
# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a>Aktualizace standardních nákladů v nevýrobním prostředí

[!include [banner](../includes/banner.md)]

V tomto článku jsou pokyny k tomu, jak aktualizovat standardní náklady v nevýrobním prostředí.

Tyto pokyny předpokládají, že používáte pro aktualizaci standardních nákladů metodou s použitím dvou verzí. V tomto přístupu jedna nákladová verze obsahuje původně definované standardní náklady pro nastavené období a druhá nákladová verze obsahuje vzestupné aktualizace. Každá aktualizace je zadána jako záznam o nákladech do druhé nákladové verze a nakonec bude aktivována. Alternativní řešení používá přístup s použitím jedné verze pomocí původně definované sady standardních nákladů. Metoda s použitím dvou verzí vyžaduje určení druhé nákladové verze. Uvádíme pokyny k definování této nákladové verze:

-   Přiřaďte nákladový typ **Standardní náklady**.
-   Přiřazení platného popisného identifikátoru značícího obsah nákladové verze, jako je například **2016-AKTUALIZACE**.
-   Ověřte, že obsah zahrnuje záznamy o nákladech.
-   Povolte zadávání záznamů nákladů pro všechna pracoviště. Pokud určíte pracoviště, záznamy nákladů lze zadat pouze pro dané pracoviště.
-   Určete pro princip zálohy hodnotu **Žádný**. Princip zálohy se vztahuje pouze na výpočty nákladů vyráběných položek.

Chcete-li opravit, upravit nebo aktualizovat standardní náklady nových položek, postupujte podle následujících kroků.

1.  Pomocí stránky **Nastavení** **nákladové verze** povolte zadání záznamy nákladů do druhé nákladové verze. Případně zabraňte aktivaci čekajících nákladů, protože tato aktivace bude povolena po úplném a přesném definování těchto nákladů. Můžete také volitelně zadat datum do pole **Od data**. Obecné platí, že používejte data, pokud chcete aktivovat přírůstkové aktualizace. Případně ponechte pole **Od data** prázdné pro nákladovou verzi, a pak zadejte datum v poli **Od data** pro každý záznam o nákladech.
2.  Pomocí stránky **Cena položky** zadejte aktualizuje jako záznamy nákladů na položky, které se nacházejí v druhé nákladové verzi.
3.  Pomocí sestavy **Ceny položek** ověřte úplnost a přesnost záznamů nákladů položek v druhé nákladové verzi.
4.  Pomocí stránky **Údržba nákladové verze** upravte příznak blokování a umožnit tak aktivaci záznamů čekajících nákladů ve druhé nákladové verzi.
5.  Pomocí stránky **Aktivovat ceny** (kterou otevřete ze stránky **Údržba nákladové verze**) povolte všechny čekající záznamy nákladů položek ve druhé nákladové verzi. Čekající záznamy nákladů pro jednotlivé položky lze také povolit klepnutím na tlačítko **Aktivovat nezpracované ceny** na stránce **Cena položky**.
6.  Pomocí stránky **Nastavení nákladové verze** upravte příznaky blokování ve druhé nákladové verzi pro zabránění další údržby dat. Zásady blokování zabraňují zadávání nových čekajících nákladů a aktivaci čekajících nákladů.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]