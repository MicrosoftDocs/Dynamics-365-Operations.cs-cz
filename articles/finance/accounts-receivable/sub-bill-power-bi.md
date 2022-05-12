---
title: Obsah fakturace předplatného Power BI
description: Toto téma popisuje, co je součástí balíčku obsahu fakturace předplatného v Microsoft Power BI.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-04-13
ms.openlocfilehash: fad96bdaf60e7772e9ea1ff937435b0274303505
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645394"
---
# <a name="subscription-billing-power-bi-content"></a>Obsah fakturace předplatného Power BI

[!include[banner](../includes/banner.md)]

Toto téma popisuje, co je součástí balíčku obsahu fakturace předplatného v Microsoft Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu. 

## <a name="overview"></a>Přehled

Obsah Power BI pro fakturaci předplatného byl vytvořen pro pracovníky a manažery účtování předplatného. Poskytuje klíčové metriky vyúčtování předplatného, jako jsou měsíční opakující se příjmy (MRR) pro plány vyúčtování a informace o klesajícím zůstatku a vodopádu pro plány odkladu. Využívá údaje z rozpisů vyúčtování a rozpisů odkladů a poskytuje přehled o opakujících se příjmech a výnosech.

Obsah Power BI má následující tři karty, které poskytují celkem čtyři analytické sestavy: 

- **Analytika - MRR** – Tato karta poskytuje sestavu **Měsíční opakované vyúčtování** a **Podrobnosti rozvrhu fakturace**.
- **Analytika – Kaskáda** – Tato karta poskytuje sestavu **Kaskáda výnosů**.
- **Analytika – Klesající zůstatek** – Tato karta poskytuje sestavu **Klesající zůstatek**.

## <a name="view-data-on-the-analytical-reports"></a>Zobrazení dat v analytických sestavách

Než budete moci zobrazit data v analytických sestavách, musíte spustit pravidelný proces, který generuje data sestav pro každou sestavu. Tato data, která sestavy vyžadují, musí být generována, protože nejsou uložena přímo v databázi. 

1. Jděte na **Fakturace předplatného \> Opakované vyúčtování smlouvy \> Periodické úkoly \> Dávkové zpracování analytické sestavy MRR** a postupujte takto:

    1. Zadejte časové období ne delší než tři roky.
    2. Volitelné: Nastavte opakující se úlohu dávkového zpracování, aby se data pravidelně obnovovala.
    3. Vyberte **OK**.

2. Po dokončení dávkové úlohy přejděte na **Správa systému \> Nastavení \> Úložiště entit** a obnovte agregované měření **Sestava MRR**. 
3. Jděte na **Fakturace předplatného \> Časové rozlišení výnosů a výdajů \> Periodické úkoly \> Dávkové zpracování analytické sestavy kaskády** a postupujte takto:

    1. Zadejte počáteční a koncové datum, které nezahrnuje více než 26 období. 
    2. Pokud chcete zobrazit předpokládaný počet minulých období v aktuálním období, nastavte **Prognóza minulých částek v aktuálním období** na **Ano**.
    3. Volitelné: Nastavte opakující se úlohu dávkového zpracování, aby se data pravidelně obnovovala.
    4. Vyberte **OK**. 

4. Po dokončení dávkové úlohy přejděte na **Správa systému \> Nastavení \> Úložiště entit** a obnovte agregované měření **Sestava kaskády**.
5. Jděte na **Fakturace předplatného \> Časové rozlišení výnosů a výdajů \> Periodické úkoly \> Dávkové zpracování analytické sestavy klesajícího zůstatku** a postupujte takto:

    1. Zadejte počáteční a koncové datum, které nezahrnuje více než 26 období. 
    2. Pokud chcete zobrazit předpokládaný počet minulých období v aktuálním období, nastavte **Prognóza minulých částek v aktuálním období** na **Ano**.
    3. Volitelné: Nastavte opakující se úlohu dávkového zpracování, aby se data pravidelně obnovovala.
    4. Vyberte **OK**.

6. Po dokončení dávkové úlohy přejděte na **Správa systému \> Nastavení \> Úložiště entit** a obnovte agregované měření **Sestava klesajícího zůstatku**.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI

Obsah Power BI Fakturace předplatného je zobrazen v pracovním prostoru **Fakturace předplatného**.
