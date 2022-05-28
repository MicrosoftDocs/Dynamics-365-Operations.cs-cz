---
title: Zobrazení transakcí závazků, majetku a nákladů
description: Toto téma vysvětluje, jak zobrazit transakce s pronajatým majetkem. Tyto transakce zahrnují transakce odpovědnosti za leasing a transakce prováděcích výdajů, které byly zaúčtovány.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: be11250a85d160aa71ab76af9cfdb0258fd7bf11
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727475"
---
# <a name="view-liability-asset-and-expense-transactions"></a>Zobrazení transakcí závazků, majetku a nákladů

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak zobrazit transakce s pronajatým majetkem. Tyto transakce zahrnují transakce odpovědnosti za leasing a transakce prováděcích výdajů, které byly zaúčtovány. Účetní hodnoty závazku a používaného majetku jsou použity v několika zprávách. Používají se také k výpočtu hodnot vyrovnání.

## <a name="liability-transactions"></a>Transakce pasiv

Chcete-li zobrazit transakce odpovědnosti za leasing, vyberte leasing na stránce **Souhrn pronájmu** a poté vyberte **Knihy** k otevření knih, které jsou připojeny k záznamu o leasingu. Po počátečním uznání byla zaúčtována faktura nebo deník úroků, vyberte **Transakce závazku**.

Stránka **Odpovědnost za transakce** zobrazuje transakce, které zvyšují nebo snižují odpovědnost za leasing. Záporné částky na této stránce představují kreditní transakce ve standardní aplikaci. Případné úroky se zobrazují jako záporné hodnoty a zvyšují celkový závazek z leasingu. Jakékoli úpravy leasingu se zobrazují jako kladné nebo záporné hodnoty v závislosti na povaze a dopadu knihy leasingu. Aktuální čistý celkový zůstatek leasingového závazku pro vybraný leasing je uveden v levé dolní části stránky.

## <a name="asset-transactions"></a>Transakce majetku

Chcete-li zobrazit majetkové leasingové transakce, vyberte leasing na stránce **Souhrn pronájmu** a poté vyberte **Knihy** k otevření leasingových knih, které jsou připojeny k záznamu o leasingu. Pak vyberte **Majetkové transakce**.

Na stránce **Majetkové transakce** se zobrazují transakce, které buď zvyšují nebo snižují majetek na leasing a účty akumulovaných odpisů. Debety se zobrazují jako kladné hodnoty a kredity se zobrazují jako záporné hodnoty, jako na stránce **Odpovědnost za transakce**. Zaúčtované počáteční uznání a další akumulované odpisy jsou zobrazeny v levém dolním rohu stránky jako zůstatek aktiv. 

## <a name="expenses-transactions"></a>Výdajové transakce

Chcete-li zobrazit výdajové leasingové transakce, vyberte leasing na stránce **Souhrn pronájmu** a poté vyberte **Knihy** k otevření leasingových knih, které jsou připojeny k záznamu o leasingu. Pak vyberte **Výdajové transakce**.

Na stránce **Výdajové transakce** se zobrazují všechny výdaje, které byly zaúčtovány oproti leasingu, jako jsou úrokové náklady, výdaje na odpisy a jakékoli zachraňovací náklady.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
