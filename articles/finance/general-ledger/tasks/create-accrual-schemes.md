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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457be741dfd3b44cb963db37857d6a7bceecc14e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994658"
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

