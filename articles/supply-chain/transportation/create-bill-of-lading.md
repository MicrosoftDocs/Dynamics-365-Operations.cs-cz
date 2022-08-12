---
title: Vytvoření přepravního dokladu
description: Tento článek popisuje, jak vytvořit přepravní doklad při používání procesů pro řízení skladu (WMS).
author: Weijiesa
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
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68a703475191255ff6ceaee25ef8e2bdf33ba0c2
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069689"
---
# <a name="create-a-bill-of-lading"></a>Vytvoření přepravního dokladu

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak vytvořit přepravní doklad při používání procesů pro řízení skladu (WMS).  

Přepravní doklad je právním dokumentem mezi společností, která dodává položky, a dopravcem. Dokument doprovází dodané položky a slouží jako potvrzení expedice při dodání položek do cílového umístění. Jestliže používáte řízení skladu, existují dva způsoby, jak přepravní doklad generovat:

  -   Vytvoření sestavy ručně pomocí stránky **Přepravní doklad**.
  -   Generování sestavy z **pracovní plochy plánování vytížení**.

Pokud generujete přepravní doklad z **pracovní plochy plánování vytížení**, stav vytížení musí být **Expedováno**. Pokud existuje více než jedna dodávka v nákladu, u každé dodávky dojde k vytvoření jednoho přepravního dokladu. Poté, co byl přepravní doklad vytvořen, můžete provést jeho změny na stránce **Přepravní doklad**.

## <a name="master-bill-of-lading"></a>Hlavní přepravní doklad
Pokud je ve vytížení více než jedna dodávka, můžete vygenerovat hlavní přepravní doklad. Ten má stejné rozvržení a obsahuje stejné informace jako přepravní doklad, ale obsahuje souhrnný obsah všech dodávek. Pokud možnost **Vytvořit hlavní přepravní doklad, když je ve vytížení více než jedna dodávka** nastavíte na **Ano** na stránce **Parametry správy přepravy**, hlavní přepravní doklad bude vygenerován automaticky po vytvoření přepravního dokladu z **pracovní plochy plánování vytížení**, existuje-li více než jedna dodávka. Seznam přepravních dokladů získáte rovněž kliknutím na **Související informace** &gt; **Přepravní doklad**. Pokud vytváříte přepravní doklad ručně, můžete hlavní přepravní doklad vytvořit na stránce **Přepravní doklad**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]