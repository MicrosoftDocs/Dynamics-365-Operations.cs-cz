---
title: Přehled řešení nesrovnalostí během párování součtů faktur
description: Párování součtu faktur můžete použít k ověření toho, zda se celkové částky na faktuře neodlišují od očekávaných částek o větší než přijatelnou odchylku.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: roschlom
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8517e2725bab69d33cfd22b77575a6aa110dde44
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972049"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching-overview"></a>Přehled řešení nesrovnalostí během párování součtů faktur

[!include [banner](../includes/banner.md)]

Párování součtu faktur je jeden typ ověřování párování faktur. Chcete-li určit, že má systém provést součty spárovaných faktur, na stránce **Parametry závazků** na kartě **Ověření faktury**, nastavte možnost **Párování součtu faktur** na možnost **Ano**. 

Párování součtu faktur můžete použít k ověření toho, zda se celkové částky na faktuře neodlišují od očekávaných částek o větší než přijatelnou odchylku. Šest součtů je porovnáváno na stránce **Shodné podrobnosti o celkových součtech faktur**. Pokud některý z celkové částky se liší od očekávané odpovídající celkové nákupní objednávky, je označena odchylka párování. 

Ke kontrole faktury, která obsahuje odlišnosti v celkové spárované částce, v pracovním prostoru **Záznam faktury dodavatele** klepněte na dlaždici **Čekající faktury**. Poté v podokně akcí na kartě **Kontroly** klepněte na možnost **Párování – podrobnosti**. Pokud byly zjištěny odlišnosti v párování, zobrazí se varovné ikony vedle fakturované částky. Zobrazením podrobností o shodách součtů faktur lze o součtech zobrazit další podrobnosti. 

Poté, co jste identifikovali nesrovnalost, budete pravděpodobně muset kontaktovat dodavatele, jestliže se domníváte, že informace na faktuře není správná. V závislosti na výsledku dohody s dodavatelem můžete provést některou z následujících akcí:

-   Akceptovat cenovou odchylku a zaúčtovat fakturu s odlišností v párování. Pokud existují odlišnosti v párování, můžete systém nastavit požadovat schválení předtím, než ho lze zaúčtovat. V takovém případě musíte schválit odchylku párování a volitelně můžete zadat schvalovací komentář. Poté můžete vybrat zaúčtovat fakturu.
-   Opravte částku faktury na očekávanou částku a doklad zaúčtujte.
-   Požádat dodavatele o dobropis a o novou opravenou fakturu.

Další informace naleznete v tématu [Prozkoumání/vyřešení výjimek](tasks/research-resolve-exceptions.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]