---
title: "Řešení nesrovnalostí během párování součtů faktur"
description: "Párování součtu faktur můžete použít k ověření toho, zda se celkové částky na faktuře neodlišují od očekávaných částek o větší než přijatelnou odchylku."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 18250a735d0421daa90b923504aeb94b5003a6a7
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>Řešení nesrovnalostí během párování součtů faktur

[!INCLUDE [banner](../includes/banner.md)]

Párování součtu faktur je jeden typ ověřování párování faktur. Chcete-li určit, že má systém provést součty spárovaných faktur, na stránce **Parametry závazků** na kartě **Ověření faktury**, nastavte možnost **Párování součtu faktur** na možnost **Ano**. 

Párování součtu faktur můžete použít k ověření toho, zda se celkové částky na faktuře neodlišují od očekávaných částek o větší než přijatelnou odchylku. Šest součtů je porovnáváno na stránce **Shodné podrobnosti o celkových součtech faktur**. Pokud některý z celkové částky se liší od očekávané odpovídající celkové nákupní objednávky, je označena odchylka párování. 

Ke kontrole faktury, která obsahuje odlišnosti v celkové spárované částce, v pracovním prostoru **Záznam faktury dodavatele** klepněte na dlaždici **Čekající faktury**. Poté v podokně akcí na kartě **Kontroly** klepněte na možnost **Párování – podrobnosti**. Pokud byly zjištěny odlišnosti v párování, zobrazí se varovné ikony vedle fakturované částky. Zobrazením podrobností o shodách součtů faktur lze o součtech zobrazit další podrobnosti. 

Poté, co jste identifikovali nesrovnalost, budete pravděpodobně muset kontaktovat dodavatele, jestliže se domníváte, že informace na faktuře není správná. V závislosti na výsledku dohody s dodavatelem můžete provést některou z následujících akcí:

-   Akceptovat cenovou odchylku a zaúčtovat fakturu s odlišností v párování. Pokud existují odlišnosti v párování, můžete systém nastavit požadovat schválení předtím, než ho lze zaúčtovat. V takovém případě musíte schválit odchylku párování a volitelně můžete zadat schvalovací komentář. Poté můžete vybrat zaúčtovat fakturu.
-   Opravte částku faktury na očekávanou částku a doklad zaúčtujte.
-   Požádat dodavatele o dobropis a o novou opravenou fakturu.

Další informace naleznete v tématu [Prozkoumání nebo vyřešení výjimek](tasks/research-resolve-exceptions.md).



