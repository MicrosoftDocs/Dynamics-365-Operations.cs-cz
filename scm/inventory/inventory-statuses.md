---
title: "Stavy zásob"
description: "Tento článek popisuje, jak lze použít stavy zásob rozdělení k řazení zásob do kategorií a jejich sledování."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 1fcdf262ee1e7e1fbbdd0a5fed46fb1867f8d8fd
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-statuses"></a>Stavy zásob

[!include[banner](../includes/banner.md)]


Tento článek popisuje, jak lze použít stavy zásob rozdělení k řazení zásob do kategorií a jejich sledování.

Stavy zásob lze použít ke kategorizaci zásob. Poté můžete zahájit příslušné akce, například doplňování nebo pracovní vyskladnění. 

Zde je několik příkladů způsobů použití stavů zásob:

-   Vytvořte stavy zásob na skladě pro množství na skladě, příchozí transakce a odchozí transakce.
-   Určete výchozí stav zásob pro transakce skladu.
-   Změna stavu zásob pro položky před doručením, při doručení nebo po vyskladnění položek při pohybu se zásobami.
-   Použijte stav zásob k ocenění vrácených položek a pro plánování pokrytí položek během hlavního plánování.

Stav zásob je jednou z dimenzí ve skupině dimenzí úložiště. Stavy zásob mohou být rozděleny do kategorií „dostupné” a „nedostupné” a lze použít parametr **blokování zásob** k blokování položek, které jsou ve stavu „nedostupné”. Položky ve stavu blokované jsou považovány za fyzické zásoby a nelze je použít ve výrobní zakázce, prodejní objednávce, převodním příkazu ani výstupní transakci. 

Položky na skladu ve stavu zásob „dostupné“ či „nedostupné“ můžete použít v rámci příchozí práce. Například lze vytvořit stav „dostupné” s názvem **Připraveno**, stav „nedostupné” s názvem **Poškozeno** a stav „blokované” s názvem **Blokováno**. Při vytvoření nákupní objednávky pro přijaté nebo vrácené položky a pokud jsou položky poškozené nebo zničené, můžete změnit stav zásob těchto položek na **Poškozeno **na řádku nákupní objednávky. Poté, co byly položky přijaty, je automaticky nastaven stav **Blokováno**. Kontrolujete-li poškozené položky pomocí mobilního zařízení, aplikace Microsoft Dynamics 365 for Operations může použít směrnice skladových míst a šablony práce k zobrazení informací o odpovídajícím místě nebo rozsahu míst, kde jsou položky odloženy. Pro vrácené položky se vytvoří typ výdeje **Rezervace** na stránce **Skladové transakce**. 

Pro výstupní práci používejte položky, které mají stav zásob „dostupné“. Pokud máte položky se stavem **„Zničené“** a použijete u nich hlavní plánování, položky budou považovány za chybějící a sklad se automaticky doplní. 

Poté, co jste nastavili stavy zásob, můžete nastavit také výchozí stav zásob pro pracoviště, položku a sklad. Můžete také nastavit výchozí stav pro prodej, převod a nákupní objednávky. Výchozí stav pro prodejní objednávky a odchozí převodní příkaz nemůže mít volbu **Blokování zásob** nastavenu na hodnotu **Ano**. Stav zásob, který je zděděn z výchozího nastavení pracoviště, skladu, položky, nákupní objednávky, převodního příkaz nebo prodejní objednávky, lze změnit pomocí mobilního zařízení nebo na nákupní objednávce, prodejní objednávce nebo řádku převodního příkazu. 

Pro plánování disponibility pro položek, které jsou ve stavu zásob „Dostupné”, vyberte možnost **Plán disponibility podle dimenzí** u dimenze úložiště na stránce **Skupiny dimenze úložiště**. Když otevřete průvodce **Disponibilita položky **, položky, které jsou ve stavu dostupné, se zobrazí na stránce **Stav**. Pro nastavení disponibility pro tyto položky vyberte ID stavu zásob u „dostupného“ stavu zásob. Na základě nastavení disponibility můžete vypočítat požadavky na položky a prognózy nabídky a poptávky u dostupných položek během hlavního plánování. Nelze vytvořit nastavení disponibility položky, která má blokovaný stav zásob. Také můžete použít stránku **Disponibilita položky** a vytvořit nebo upravit parametry disponibility položky.




