---
title: Vytvoření schémat časového rozlišení
description: Toto téma vysvětluje, jak vytvořit schéma časového rozlišení.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a83870c4cec4de2e51e90ff1889d4beff6c23f95
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441234"
---
# <a name="create-accrual-schemes"></a>Vytvoření schémat časového rozlišení

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit schéma časového rozlišení. Tento úkol využívá ukázkovou společnost USMF.

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