---
title: Stavy zásob
description: Tento článek popisuje, jak lze použít stavy zásob rozdělení k řazení zásob do kategorií a jejich sledování.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus, WHSWarehouseStatusChange
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db15ad94355823c699e83c9e3f47660f813e1c9a
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103456"
---
# <a name="inventory-statuses"></a>Stavy zásob

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak lze použít stavy zásob rozdělení k řazení zásob do kategorií a jejich sledování.

## <a name="set-up-and-use-inventory-statuses"></a>Nastavení a použití stavů zásob

Stavy zásob lze použít ke kategorizaci zásob. Poté můžete zahájit příslušné akce, například doplňování nebo pracovní vyskladnění.

Zde je několik příkladů způsobů použití stavů zásob:

- Vytvořte stavy zásob na skladě pro množství na skladě, příchozí transakce a odchozí transakce.
- Určete výchozí stav zásob pro transakce skladu.
- Změna stavu zásob pro položky před doručením, při doručení nebo po vyskladnění položek při pohybu se zásobami.
- Použijte stav zásob k ocenění vrácených položek a pro plánování pokrytí položek během hlavního plánování.

Stav zásob je jednou z dimenzí ve skupině dimenzí úložiště. Stavy zásob mohou být rozděleny do kategorií „dostupné” a „nedostupné” a lze použít parametr **blokování zásob** k blokování položek, které jsou ve stavu „nedostupné”. Položky ve stavu blokované jsou považovány za fyzické zásoby a nelze je použít ve výrobní zakázce, prodejní objednávce, převodním příkazu ani výstupní transakci.

Položky na skladu ve stavu zásob „dostupné“ či „nedostupné“ můžete použít v rámci příchozí práce. Například lze vytvořit stav „dostupné” s názvem *Připraveno*, stav „nedostupné” s názvem *Poškozeno* a stav „blokované” s názvem *Blokováno*. Při vytvoření nákupní objednávky pro přijaté nebo vrácené položky a pokud jsou položky poškozené nebo zničené, můžete změnit stav zásob těchto položek na *Poškozeno* na řádku nákupní objednávky. Poté, co byly položky přijaty, je automaticky nastaven stav *Blokováno*. Kontrolujete-li poškozené položky pomocí mobilního zařízení, aplikace Supply Chain Management může použít směrnice skladových míst a šablony práce k zobrazení informací o odpovídajícím místě nebo rozsahu míst, kde jsou položky odloženy. Pro vrácené položky se vytvoří typ výdeje *Rezervace* na stránce **Skladové transakce**.

Můžete určit, jaké stavy zásob jsou stavy blokování, pomocí zaškrtávacího políčka **Blokování zásob** na stránce **Stavy zásob**. Stavy zásob nelze použít jako stavy blokování pro prodejní objednávky, převodní příkazy, nebo integrace projektu.

U odchozí práce můžete pomocí různých neblokujících stavů zásob určit, proti kterým zásobám se má rezervovat. Pokud máte položky se stavem *„Blokování“* a použijete u nich hlavní plánování, položky budou považovány za chybějící a sklad se automaticky doplní. U objednávek kvality přidružených k odchozí práci navíc není možné aktualizovat **Stav zásob** jako součást ověření objednávky kvality.

> [!NOTE]
> Na místech, kde existuje otevřená práce, nemůžete změnit stav zásob. Například pokud jste provedli příjem nákupu pro položku, ale neprovedli jste krok vyskladnění, pak by pro přijímající místo existovala otevřená práce a při pokusu o změnu stavu zásob v daném místě by se zobrazila chyba. Dokončení nebo zrušení související práce vám umožní změnit stav.
>
> Obvykle stav zásob na skladě související s otevřenou prací skladu mění pouze pracovníci používající mobilní aplikaci Řízení skladu, například při provádění procesu přesunu.

Poté, co jste nastavili stavy zásob, můžete nastavit také výchozí stav zásob pro pracoviště, položku a sklad. Můžete také nastavit výchozí stav pro prodej, převod a nákupní objednávky. Výchozí stav pro prodejní objednávky a odchozí převodní příkaz nemůže mít volbu **Blokování zásob** nastavenu na hodnotu *Ano*. Stav zásob, který je zděděn z výchozího nastavení pracoviště, skladu, položky, nákupní objednávky, převodního příkaz nebo prodejní objednávky, lze změnit pomocí mobilního zařízení nebo na nákupní objednávce, prodejní objednávce nebo řádku převodního příkazu.

Pro plánování disponibility pro položek, které jsou ve stavu zásob „Dostupné”, vyberte možnost **Plán disponibility podle dimenzí** u dimenze úložiště na stránce **Skupiny dimenze úložiště**. Když otevřete průvodce **Disponibilita položky**, položky, které jsou ve stavu dostupné, se zobrazí na stránce **Stav**. Pro nastavení disponibility pro tyto položky vyberte ID stavu zásob u „dostupného“ stavu zásob. Na základě nastavení disponibility můžete vypočítat požadavky na položky a prognózy nabídky a poptávky u dostupných položek během hlavního plánování. Nelze vytvořit nastavení disponibility položky, která má blokovaný stav zásob. Také můžete použít stránku **Disponibilita položky** a vytvořit nebo upravit parametry disponibility položky.

## <a name="change-inventory-statuses"></a>Změna stavů zásob

Stavy zásob můžete změnit buď pomocí stránky **Množství na skladě podle místa** stránku nebo pomocí periodického úkolu *Změna stavu zásob*.

- Při použití periodického úkolu *Změna stavu zásob* můžete vybrat, které záznamy mají být zahrnuty, a nastavit úkol, který má být spuštěn v dávce v požadovaném intervalu.
- Chcete-li změnit stav zásob jako proces ad-hoc, přejděte na stránku **Množství na skladě podle místa**, vyberte příslušné záznamy a poté vyberte tlačítko **Změna stavu zásob**.

> [!NOTE]
> Funkce *Změnit stav zásob položek kontrolovaných sledovacími dimenzemi* umožňuje změnit stav zásob položek ovládaných sledováním dimenzí, včetně možnosti aktualizovat pouze vybrané záznamy. Od verze Supply Chain Management 10.0.25 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.25, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Změnit stav zásob položek kontrolovaných sledovacími dimenzemi* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Když je funkce povolena, budete moci provést následující:
>
> - Na stránce **Množství na skladě podle místa** můžete seskupit řádky podle zobrazených dimenzí pomocí tlačítka **Zobrazit dimenze** a změnit stav vybraných řádků.
> - Na stránce **Množství na skladě podle místa** můžete vybrat více záznamů a poté použít tlačítko **Změna stavu zásob** pro změnu všech najednou.
> - V periodickém úkolu **Změna stavu zásob** budete moci filtrovat podle sledovacích dimenzí.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
