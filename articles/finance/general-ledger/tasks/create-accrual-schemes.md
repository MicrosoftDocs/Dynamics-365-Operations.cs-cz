---
title: Vytvoření schémat časového rozlišení
description: Tento článek vysvětluje, jak vytvořit schéma časového rozlišení.
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8974eed40a60aeee5a32932ac070a870289ec20a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858414"
---
# <a name="create-accrual-schemes"></a>Vytvoření schémat časového rozlišení

[!include [banner](../../includes/banner.md)]

Tento článek vysvětluje, jak vytvořit schéma časového rozlišení. Tento úkol využívá ukázkovou společnost USMF.

1. Přejděte na **Navigační podokno > Moduly > Hlavní kniha > Nastavení deníku > Schémata časového rozlišení**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Identifikace časového rozlišení**.
4. Do pole **Popis schématu časového rozlišení** zadejte hodnotu.
5. Zadejte požadované hodnoty do pole **Má dáti**. Definovaný hlavní účet nahradí hlavní účet Má dáti v řádku dokladu deníku také bude použit pro stornování časově rozlišených položek na základě transakcí časového rozlišení hlavní knihy.  
6. Zadejte požadované hodnoty do pole **Dal**. Definovaný hlavní účet nahradí kreditní hlavní účet řádku dokladu deníku a také bude použit pro stornování časově rozlišených položek podle transakcí časového rozlišení hlavní knihy.  
7. V poli **Doklad** vyberte způsob určení dokladu, když jsou transakce zaúčtovány.
8. V poli **Popis** zadejte hodnotu k popisu transakcí, které mají být zaúčtovány.
9. V poli **Frekvence období** vyberte, jak často by transakce měla být zaznamenána.
10. Do pole **Počet výskytů podle období** zadejte číslo.
11. V poli **Zaúčtovat transakce** vyberte, kdy transakce mají být zaúčtovány – například **měsíčně**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
