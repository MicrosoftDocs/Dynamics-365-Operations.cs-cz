---
title: Vytvoření přepravního dokladu
description: Toto téma popisuje, jak vytvořit přepravní doklad při používání procesů pro řízení skladu.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b79408e21e9acda12617cf35464007e58ae1b5fe
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573122"
---
# <a name="create-a-bill-of-lading"></a>Vytvoření přepravního dokladu

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vytvořit přepravní doklad při používání procesů pro řízení skladu.  

Přepravní doklad je právním dokumentem mezi společností, která dodává položky, a dopravcem. Dokument doprovází dodané položky a slouží jako potvrzení expedice při dodání položek do cílového umístění. Jestliže používáte řízení skladu, existují dva způsoby, jak přepravní doklad generovat:

  -   Vytvoření sestavy ručně pomocí stránky **Přepravní doklad**.
  -   Generování sestavy z **pracovní plochy plánování vytížení**.

Pokud generujete přepravní doklad z **pracovní plochy plánování vytížení**, stav vytížení musí být **Expedováno**. Pokud existuje více než jedna dodávka v nákladu, u každé dodávky dojde k vytvoření jednoho přepravního dokladu. Poté, co byl přepravní doklad vytvořen, můžete provést jeho změny na stránce **Přepravní doklad**.

## <a name="master-bill-of-lading"></a>Hlavní přepravní doklad
Pokud je ve vytížení více než jedna dodávka, můžete vygenerovat hlavní přepravní doklad. Ten má stejné rozvržení a obsahuje stejné informace jako přepravní doklad, ale obsahuje souhrnný obsah všech dodávek. Pokud možnost **Vytvořit hlavní přepravní doklad, když je ve vytížení více než jedna dodávka** nastavíte na **Ano** na stránce **Parametry správy přepravy**, hlavní přepravní doklad bude vygenerován automaticky po vytvoření přepravního dokladu z **pracovní plochy plánování vytížení**, existuje-li více než jedna dodávka. Seznam přepravních dokladů získáte rovněž kliknutím na **Související informace** &gt; **Přepravní doklad**. Pokud vytváříte přepravní doklad ručně, můžete hlavní přepravní doklad vytvořit na stránce **Přepravní doklad**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]