---
title: "Vytvoření přepravního dokladu"
description: "Toto téma popisuje, jak vytvořit přepravní doklad při používání procesů pro řízení skladu."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ab5aa60198e442237fd85bb295589ae0ebe9c5f5
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-bill-of-lading"></a>Vytvoření přepravního dokladu

[!INCLUDE [banner](../includes/banner.md)]

Toto téma popisuje, jak vytvořit přepravní doklad při používání procesů pro řízení skladu.  

Přepravní doklad je právním dokumentem mezi společností, která dodává položky, a dopravcem. Dokument doprovází dodané položky a slouží jako potvrzení expedice při dodání položek do cílového umístění. Jestliže používáte řízení skladu, existují dva způsoby, jak přepravní doklad generovat:

  -   Vytvoření sestavy ručně pomocí stránky **Přepravní doklad**.
  -   Generování sestavy z **pracovní plochy plánování vytížení**.

Pokud generujete přepravní doklad z **pracovní plochy plánování vytížení**, stav vytížení musí být **Expedováno**. Pokud existuje více než jedna dodávka v nákladu, u každé dodávky dojde k vytvoření jednoho přepravního dokladu. Poté, co byl přepravní doklad vytvořen, můžete provést jeho změny na stránce **Přepravní doklad**.

## <a name="master-bill-of-lading"></a>Hlavní přepravní doklad
Pokud je ve vytížení více než jedna dodávka, můžete vygenerovat hlavní přepravní doklad. Ten má stejné rozvržení a obsahuje stejné informace jako přepravní doklad, ale obsahuje souhrnný obsah všech dodávek. Pokud možnost **Vytvořit hlavní přepravní doklad, když je ve vytížení více než jedna dodávka** nastavíte na **Ano** na stránce **Parametry správy přepravy**, hlavní přepravní doklad bude vygenerován automaticky po vytvoření přepravního dokladu z **pracovní plochy plánování vytížení**, existuje-li více než jedna dodávka. Seznam přepravních dokladů získáte rovněž kliknutím na **Související informace** &gt; **Přepravní doklad**. Pokud vytváříte přepravní doklad ručně, můžete hlavní přepravní doklad vytvořit na stránce **Přepravní doklad**.




